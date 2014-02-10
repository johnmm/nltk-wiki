## How NLTK Discovers Third Party Software

NLTK finds third party software through environment variables or via path arguments through api calls. This page will list installation instructions & their associated environment variables.

## Java
Java is not required by nltk, however some third party software may be dependent on it. NLTK finds the java binary via the system path environment variable, or through `JAVAHOME` or `JAVA_HOME`.

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
