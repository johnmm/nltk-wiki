Installation and Configuration
------------------------------

Install [Jenkins](http://jenkins-ci.org/).

Once jenkins is up and running, install the following plugins.
  * ShiningPanda Plugin (for python supports)
  * GitHub plugin (for github supports)
  * Jenkins Cobertura Plugin (for publishing coverage result)
  * Jenkins Violations plugin (for publishing pylint result)
  * Environment Injector Plugin (for custom shell environment variables)

Jenkins plugins can be installed from the following menu:

    Jenkins -> Manage Jenkins -> Manage Plugins

Create a new jenkins job from the configuration file included in nltk. Jenkins provides rest api for this. (Replace "your_jenkins_url" and "newjobname" with appropriate values below.)

    curl --user USER:PASS -H "Content-Type: text/xml" -s \
         --data "@jenkins-jon-config.xml" \
         "https://your_jenkins_url/createItem?name=newjobname"

Open the configuration for the new job by clicking on the hyper link for the new job, and then clicking on the Configure menu on the left side. In the configuration page, make sure that it is pointing to the right branch/repository. Also, unless you are using macports, you might want to turn off the following check box:

    Inject environment variables to the build process

That's it. Jenkins will run the job in 5 minutes because the configuration files is set up to check the repository every 5 minutes. If it finds any new commits, it will download the changes and run the job. The job's workspace is initially empty, so at first poll, jenkins will download the entire repository and run the job.


How It Works
------------

Here's the list of files that play a role in the setup described above:

*   jenkins-job-config.xml

    The jenkins job configuration file that was installed above.

*   jenkins.sh

    This is what the jenkins execute to install dependencies, run doctest (nltk/test/runtests.py), compute coverage, and run pylint. Other tasks can be added to this later.

*   pip-req.txt

    This is a pip requirements file. It lists nltk dependencies.

*   pip-install.py

    This is a small utility program to read pip-req.txt and to iterate and install dependencies one by one.

*   tox.ini

    This setup uses tox to configure jenkins for multiple environments. Tox allows to specify multiple python environments, e.g. python 2.7, python 3.2, pypy, etc. For each environment, it creates a virtualenv session and runs the specified commands (which is jenkins.sh in our case) under the virtualenv.

*   nltk/test/runtests.py

    This is the official test runner for nltk.


Every 5 munites, the jenkins job checks the master branch of the nltk github repository for any new commits.

If new commits are found, the jenkins job pulls the new commits and run tox at the top level directory of nltk source code.

For each python versions specified in the tox.ini file, tox creates a [virtualenv](http://www.virtualenv.org/) instance. By default, created virtual environments are reused instead of being re-created every time tox runs.

For each virtual environment, tox runs jenkins.sh, which is the only command in the commands variable of the tox.ini file.

Jenkins.sh is a shell script that performs several tasks. It
  * runs pip-install.py,
  * runs doctest via nltk/test/runtests.py,
  * generates test results,

Pip-install.py is a simple program that loops through python packages specified in the pip-req.txt file and install them one at a time using pip. This is a workaround for an issue with the "pip install -r" command, where pip refuses to install anything in the requirements list if the setup.py of a package requires another package in the list to have been installed already. See this [issue tracker](https://github.com/pypa/pip/issues/25) for details.