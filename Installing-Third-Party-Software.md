## How NLTK Discovers Third Party Software

NLTK finds third party software through environment variables or via path arguments through api calls. This page will list installation instructions & their associated environment variables.

## Java
Java is not required by nltk, however some third party software may be dependent on it. NLTK finds the java binary via the system `PATH` environment variable, or through `JAVAHOME` or `JAVA_HOME`.

To search for java binaries (jar files), nltk checks the java `CLASSPATH` variable, however there are usually independent environment variables which are also searched for each dependency individually.

### Windows
* Download & Install the jdk on java's official website: http://www.oracle.com/technetwork/java/javase/downloads/index.html?ssSourceSiteId=otnjp

### Linux
It is best to use the package manager to install java.

## Stanford Tagger, NER, Tokenizer and Parser. 

To install:
* Make sure java is installed
* Download & extract the stanford tokenizer package (contains the stanford tagger): http://nlp.stanford.edu/software/lex-parser.shtml
* Download & extract the stanford NER package http://nlp.stanford.edu/software/CRF-NER.shtml
* Download & extract the stanford POS tagger package http://nlp.stanford.edu/software/tagger.shtml
* Download & extract the stanford Parser package: http://nlp.stanford.edu/software/lex-parser.shtml
* Add the directories containing `stanford-postagger.jar`, `stanford-ner.jar` and `stanford-parser.jar` to the `CLASSPATH` environment variable
* Point the `STANFORD_MODELS` environment variable to the directory containing the stanford tokenizer models, stanford pos models, stanford ner models, stanford parser models e.g (`arabic.tagger`, `arabic-train.tagger`, `chinese-distsim.tagger`,`stanford-parser-x.x.x-models.jar` ...)
* e.g. `export STANFORD_MODELS=/usr/share/stanford-postagger-full-2015-01-30/models:/usr/share/stanford-ner-2015-04-20/classifier`

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
* Download & extract the hunpos tagger and a model file: https://code.google.com/p/hunpos/downloads/list
* Set the environment variable `HUNPOS_TAGGER` to point to the directory containing the `hunpos-tag` binary
* NLTK also searches for the model files using the same environment variable, so you can put the model file in the same location (NB the model file path can also be passed to the `nltk.tag.hunpos.HunposTagger` class via the `path_to_model` argument)

## Senna for Various NLP Tasks
To install 
* Download & extract the Senna files: http://ml.nec-labs.com/senna/
* Set the environment variable `SENNA` to point to the senna directory. NLTK searches for the binary executable files via this environment variable, but the directory path can also be passed to the `nltk.tag.senna.SennaTagger` class via the `senna_path` argument.

## CRFSuite for CRF Tagger
To install 
* Download & compile : http://www.chokkan.org/software/crfsuite/
* Set the environment variable `CRFSUITE` to point to the directory containing `crfsuite` (for Linux) or `crfsuite.exe` for Window. NLTK searches for the binary executable files via this environment variable, but the executable file path can also be passed to the `nltk.tag.crfsuite.CRFTagger` class via the `file_path` argument.