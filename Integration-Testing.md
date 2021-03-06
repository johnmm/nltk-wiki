Installation and Configuration
------------------------------

First of all, install [Jenkins](http://jenkins-ci.org/). See the web site for installation instructions.

Once Jenkins is up and running, install the following plugins.
 * ShiningPanda Plugin (for python supports)
 * GitHub Plugin (for github supports)
 * Jenkins Cobertura Plugin (for publishing coverage result)
 * Jenkins Violations Plugin (for publishing pylint result)
 * Environment Injector Plugin (for custom shell environment variables)

Jenkins plugins can be installed from the following menu:

    Jenkins -> Manage Jenkins -> Manage Plugins

Create a new Jenkins job using the configuration file included in nltk. The configuration file is called `jenkins-job-config.xml`. This file can be imported using a REST API. For example,

    curl --user USER:PASS -H "Content-Type: text/xml" -s \
         --data "@jenkins-job-config.xml" \
         "https://your_jenkins_url/createItem?name=newjobname"

Replace `your_jenkins_url` and `newjobname` with appropriate values above. The `--user` option can be omitted if Jenkins user and password are not configured.

Now, configure the created job. Open the configuration menu by clicking on the hyperlink for the new job, and then clicking on the `Configure` menu on the left side. In the configuration page, make sure that it is pointing to the right branch/repository. Also, unless you are using Macports, you might want to turn off the following check box:

    Inject environment variables to the build process

That's it. Jenkins will run the job in 5 minutes because the configuration files is set up to check the repository every 5 minutes. If it finds any new commits, it will download the changes and run the job. The job's workspace is initially empty, so at first poll, Jenkins will download the entire repository and run the job.

How It Works
------------

Here's the list of files that are involved in the setup.

* `jenkins-job-config.xml`

 The Jenkins job configuration file that is imported to create a new job.

* `jenkins.sh`

 This is executed by the Jenkins job (via Tox) to install dependencies, run doctest (`nltk/test/runtests.py`), compute coverage, and run pylint. Other tasks can be added to this later.

* `pip-req.txt`

 This is a pip requirements file. It lists NLTK dependencies.

* `tox.ini`

 This is a configuration file for [Tox](http://tox.readthedocs.org/en/latest/). Tox is used to enable multi-python test environments. For example, it allows to run tests with python 2.7, python 3.2, pypy, etc. This config file lists many test environments. Our Jenkins job is configured to use three of them: `py27-jenkins`, `py34-jenkins` and `py35-jenkins`. These environments are set up to execute `jenkins.sh`, which in turn executes `nltk/test/runtests.py`.

* `nltk/test/runtests.py`

 This is the official test runner for NLTK. To run tests, `jenkins.sh` executes this file.
Every 5 minutes, the Jenkins job checks the repository and branch specified in the job config file for any new commits.

If new commits are found, the Jenkins job pulls the new commits and run `tox` at the top level directory of NLTK source code.

For each Tox test environment specified in the Jenkins config file, Tox creates a [virtualenv](http://www.virtualenv.org/) instance. Created virtual environments are reused instead of being re-created every time Tox runs.

For each of the virtual environments, Tox runs `jenkins.sh`, which is the only command in the `commands` variable of the `tox.ini` file.

`jenkins.sh` is a shell script that performs several tasks. It
 * installs any python dependencies,
 * downloads NLTK corpora,
 * installs any third party dependencies,
 * runs doctests & unit tests via `nltk/test/runtests.py`,
 * generates test results
