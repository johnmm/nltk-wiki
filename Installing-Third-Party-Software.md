## How NLTK Discovers Third Party Software

NLTK finds third party software through environment variables or via path arguments through api calls. This page will list installation instructions & their associated environment variables.

## Java
Java is not required by nltk, however some third party software may be dependent on it. NLTK finds the java binary via the system `PATH` environment variable, or through `JAVAHOME` or `JAVA_HOME`.

To search for java binaries (jar files), nltk checks the java `CLASSPATH` variable, however there are usually independent environment variables which are also searched for each dependency individually.

### Windows
* Download & Install the jdk on java's official website: http://www.oracle.com/technetwork/java/javase/downloads/index.html?ssSourceSiteId=otnjp

### Linux
It is best to use the package manager to install java.

## Stanford Parser

To install:
* Make sure java is installed
* Download & extract the stanford parser package: http://nlp.stanford.edu/software/lex-parser.shtml
* Point the `STANFORD_PARSER` or java `CLASSPATH` environment variable to the directory containing `stanford-parser.jar`.
* Point the `STANFORD_MODELS` environment variable to the directory containing `stanford-parser-x.x.x-models.jar`.

## Stanford Tagger & Tokenizer

To install:
* Make sure java is installed
* Download & extract the stanford tokenizer package (contains the stanford tagger): http://nlp.stanford.edu/software/lex-parser.shtml
* Download & extract the stanford NER package http://nlp.stanford.edu/software/CRF-NER.shtml
* Point the java `CLASSPATH` environment variable to the directory containing `stanford-postagger.jar` and `stanford-ner.jar`.
* Point the `STANFORD_MODELS` environment variable to the directory containing the stanford tokenizer models (`arabic.tagger`, `arabic-train.tagger`, `chinese-distsim.tagger`, ...)

## Tadm (Toolkit for Advanced Discriminative Modeling)

To install
* Download & compile TADM: http://tadm.sourceforge.net/
* Set the environment variable `TADM` to point to the tadm binaries directory.

## Megam (MEGA Model Optimization Package)

To install
* Download & compile MEGAM's source: http://www.umiacs.umd.edu/~hal/megam/index.html
* Set the environment variable `MEGAM` to point to the MEGAM directory.
* If using macports version of ocaml, modify the MEGAM Makefile to specify the following:
  `WITHCLIBS =-I /opt/local/lib/ocaml/caml` and `WITHSTR =str.cma -cclib -lcamlstr`

## C&C Tools/Boxer

To install
* Checkout & compile the latest SVN revision http://svn.ask.it.usyd.edu.au/trac/candc/wiki/Subversion
* Set the environment variable `CANDC` to point to the C&C directory.

## Prover9 & Mace4

To install
* Download & extract Prover9 & Mace4: http://www.cs.unm.edu/~mccune/mace4/
* Set the environment variable `PROVER9` to point to the binaries directory.

## Malt Parser

To install
* Make sure java is installed
* Download & extract the Malt Parser: http://www.maltparser.org/download.html
* Set the environment variable `MALT_PARSER` to point to the directory containing `malt.jar`.

## Hunpos Tagger

To install
* Download & extract the hunpos tagger files: https://code.google.com/p/hunpos/downloads/list
* Set the environment variable `HUNPOS_TAGGER` to point to the directory containing the `hunpos-tag` binary. NLTK also searches for the model files via these environment variables, but their paths can also be passed to the `nltk.tag.hunpos.HunposTagger` class via the `path_to_model` argument.
