Semantic parsing is the extension of broad-coverage probabilistic parsers to represent sentence meaning. We are reviewing options for incorporating a semantic parser into NLTK.

## Option 1

A probabilistic CCG parser that parses input sentences into meaning representations using semantically annotated lexicons.

### Pros

In recent work on semantic parsing, CCG is one of the most popular choices for the syntactic component, in part because it offers a simple interface between syntax and semantics. Moreover, there is already an implementation in NLTK.

### Cons

CCG is still somewhat 'niche' as a grammar framework, and the existing NLTK implementation would require significant work to be made probabilistic.


## Option 2

A probabilistic dependency grammar, together with a method for mapping dependency trees into meaning representations.

### Pros

Dependency grammars are well-established as a framework for probabilistic parsing and there is a implementation in NLTK.

### Cons

There doesn't seem to be a widely-agreed approach for converting dependency trees into meaning representations. Existing approaches tend to use either domain-specific query languages or get trained on pairings of sentences and meaning representations (which are not widely available).  


## Semantics

In order to illustrate the effectiveness of semantic parsing, it's useful to have one or more a specific tasks to accomplish. Most approaches have used some variant of knowledge base query, and it would be desirable to target an existing KB which is widely used. This would involve grounding of the semantic predicates in an open-domain ontology/knowledge base, e.g. [Freebase]/[Wikidata] (see [Freebase is shutting down],  [:BaseKB] or [DBpedia].



[Freebase]: http://www.freebase.com
[Freebase is shutting down]: https://plus.google.com/109936836907132434202/posts/3aYFVNf92A1
[:BaseKB]: http://www.basekb.com
[DBpedia]: http://dbpedia.org
[Wikidata]: http://www.wikidata.org/
[ccg package]: https://github.com/nltk/nltk/tree/develop/nltk/ccg