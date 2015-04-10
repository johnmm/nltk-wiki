Semantic parsing is the extension of broad-coverage probabilistic parsers to represent sentence meaning. We are reviewing options for incorporating a semantic parser into NLTK.

# Proposed Approach

+ A broad-coverage probabilistic CCG parser that parses input sentences into meaning representations using FOL + lambda-calculus.

+ Grounding of the predicates in the meaning representations in an open-domain ontology/knowledge base, e.g. [Freebase],  [:BaseKB] or [DBpedia].

# Rationale

* In recent work on semantic parsing, CCG is one of the most popular choices for the syntactic component, in part because it offers a simple interface between syntax and semantics. Moreover, there is already an implementation in NLTK, although this will need to be made more efficient.
* FOL + lambda-calculus is an adequately expressive meaning representation language. Although a number of approaches to semantic parsing have used domain-specific languages, these suffer from lack of portability. Again, there is support for FOL + lambda-calculus in NLTK.
* In order to illustrate the effectiveness of semantic parsing, it's useful to have one or more a specific tasks to accomplish. Most approaches have used some variant of knowledge base query, and it would be desirable to target an existing KB which is widely used.

# To do
Planned phases of development, in order:

1. Extend the existing [ccg package] to include:
  * probabilistic chart parsing with beam search.
  * construction of NLTK-compatible logical forms from syntactic parses.
3. Create example lexicons.
4. Develop a method for querying the chosen ontology/KB using the output logical forms, e.g. by converting logical forms into SPARQL queries.

[Freebase]: http://www.freebase.com
[:BaseKB]: http://www.basekb.com
[DBpedia]: http://dbpedia.org
[ccg package]: https://github.com/nltk/nltk/tree/develop/nltk/ccg