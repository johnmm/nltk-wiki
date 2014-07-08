Dependency parsing is a popular approach to natural language parsing. NLTK includes some basic algorithms, but we need more reference implementations and more corpus readers.

## Existing functionality

Existing functionality is in the [parse package](https://github.com/nltk/nltk/tree/develop/nltk/parse). It includes:

* projective dependency parser (similar to Eisner 1996)
* probabilistic projective dependency parser (Eisner 1996 Model C)
* non-projective dependency parser (still includes diagnostic print statements?)
* probabilistic non-projective dependency parser (still includes diagnostic print statements?)
* interface to the MaltParser
* corpus reader for the CoNLL 2007 shared task, and for a 10% sample of the dependency version of the Penn Treebank

## Planned functionality

* [corpus reader for the Universal Dependency Treebank](https://github.com/nltk/nltk/issues/693)
* [Nivre's arc-eager and arc-standard algorithms](https://github.com/nltk/nltk/issues/694)
