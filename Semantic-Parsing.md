Semantic parsing is the extension of broad-coverage probabilistic parsers to represent the meaning of a sentence. We are reviewing options for incorporating a semantic parser into NLTK.

# Proposed Approach

+ A broad-coverage probabilistic CCG parser that parses input sentences into meaning representations using FOL + lambda-calculus.

+ Grounding of the predicates in the meaning representations in an open-domain ontology, e.g. [Freebase] or [:BaseKB].

# To do
Planned phases of development, in order:

1. Extend the existing [ccg package] to include:
  * probabilistic chart parsing with beam search.
  * construction of logical forms from syntactic parses.
3. Create example lexicons.
4. Develop a method for querying the chosen ontology using the output logical forms, e.g. by converting logical forms into SPARQL queries.

[Freebase]: http://www.freebase.com
[:BaseKB]: http://www.basekb.com
[ccg package]: https://github.com/nltk/nltk/tree/develop/nltk/ccg
