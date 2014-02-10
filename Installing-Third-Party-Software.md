## How NLTK Discovers Third Party Software

NLTK finds third party software through environment variables or via path arguments through api calls. This page will list installation instructions & their associated environment variables.

## Java
Java is not required by nltk, however some third party software may be dependent on it. NLTK finds the java binary via the system `PATH` environment variable, or through `JAVAHOME` or `JAVA_HOME`.

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

## Mallet (MAchine Learning for LanguagE Toolkit)
Currently only MALLET v0.4 is supported, but there is work in progress ([#104](https://github.com/nltk/nltk/issues/104)) to update the MALLET interface.

To install:
* Make sure java is installed
* Download & extract MALLET: http://mallet.cs.umass.edu/download.php
* Set the environment variable `MALLET_HOME` or `MALLET` to point to the MALLET directory.

## TADM (Toolkit for Advanced Discriminative Modeling)

To install
* Download & compile TADM: http://tadm.sourceforge.net/
* Set the environment variable `TADM_DIR` to point to the tadm binaries directory.

## Megam (MEGA Model Optimization Package)

To install
* Download & compile MEGAM's source: http://www.umiacs.umd.edu/~hal/megam/index.html
* Set the environment variable `MEGAM` or `MEGAMHOME` to point to the MEGAM directory.

## C&C Tools/Boxer

To install
* Checkout & compile the latest SVN revision http://svn.ask.it.usyd.edu.au/trac/candc/wiki/Subversion
* Set the environment variable `CANDCHOME` to point to the C&C directory.

