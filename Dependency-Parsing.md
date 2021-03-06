Dependency parsing is a popular approach to natural language parsing. NLTK includes some basic algorithms, but we need more reference implementations and more corpus readers.

## Existing functionality

Existing functionality is in the [parse package](https://github.com/nltk/nltk/tree/develop/nltk/parse). It includes:

* projective dependency parser (similar to Eisner 1996) and probabilistic projective dependency parser (Eisner 1996 Model C), [projectivedependencyparser.py](https://github.com/nltk/nltk/blob/develop/nltk/parse/projectivedependencyparser.py)
* non-projective dependency parser and probabilistic non-projective dependency parser (still includes diagnostic print statements?), [nonprojectivedependencyparser.py](https://github.com/nltk/nltk/blob/develop/nltk/parse/nonprojectivedependencyparser.py)
* interface to the MaltParser, [malt.py](https://github.com/nltk/nltk/blob/develop/nltk/parse/malt.py)
* corpus reader for the CoNLL 2007 shared task, and for a 10% sample of the dependency version of the Penn Treebank, [dependency.py](https://github.com/nltk/nltk/blob/develop/nltk/corpus/reader/dependency.py)
* corpus reader for the Universal Dependency Treebank
* Labeled and unlabeled attachment scores
* [Nivre's arc-eager and arc-standard algorithms](https://github.com/nltk/nltk/blob/develop/nltk/parse/transitionparser.py)
* [Visualization of dependency trees](https://github.com/nltk/nltk/blob/develop/nltk/parse/dependencygraph.py#L140)

## Planned functionality

* [Add interface to Universal Dependencies Dataset](https://github.com/nltk/nltk/issues/875)
* [Adapt Honnibal's shift-reduce dependency parser](https://github.com/nltk/nltk/issues/694#issuecomment-69795719)


