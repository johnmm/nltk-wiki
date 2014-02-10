Third Party Software
--------------------
NLTK finds third party software through environment variables by default, but arguments to paths containing them can also be specified in api calls. This page will list installation instructions & their associated environment variables.

Stanford Parser
---------------
To install:
* Download & extract the stanford parser package: http://nlp.stanford.edu/software/lex-parser.shtml
* Point the `STANFORD_PARSER` or java `CLASSPATH` environment variable to the directory containing `stanford-parser.jar`.
* Point the `STANFORD_MODELS` environment variable to the directory containing `stanford-parser-x.x.x-models.jar`.

Stanford Tagger & Tokenizer
---------------------------
To install:
* Download & extract the stanford tokenizer package (contains the stanford tagger): http://nlp.stanford.edu/software/lex-parser.shtml
* Download & extract the stanford NER package http://nlp.stanford.edu/software/CRF-NER.shtml
* Point the java `CLASSPATH` environment variable to the directory containing `stanford-postagger.jar` and `stanford-ner.jar`.
* Point the `STANFORD_MODELS` environment variable to the directory containing the stanford tokenizer models (`arabic.tagger`, `arabic-train.tagger`, `chinese-distsim.tagger`, ...)
