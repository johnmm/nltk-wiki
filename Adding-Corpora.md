NLTK comes with a [collection of corpora](http://www.nltk.org/nltk_data/). All corpora are freely redistributable. They live in the `gh-pages` branch of the nltk_data repository.

## Corpus Readers

Each corpus requires a [corpus reader](https://github.com/nltk/nltk/tree/develop/nltk/corpus/reader), plus an entry in the [corpus package](https://github.com/nltk/nltk/blob/develop/nltk/corpus/__init__.py) that allows the corpus to be imported (this entry associates an importable name with a corpus reader and a data source).

If there is not yet a suitable corpus reader, you will need to create one, and submit that as a pull request to the [nltk repository](https://github.com/nltk/nltk).

## Adding a Corpus

To add a corpus to NLTK, please follow these steps:

1. Post a new entry to the nltk_data issue tracker:
  * https://github.com/nltk/nltk_data/issues/new
  * include the corpus name in the title
  * identify the source of the corpus (e.g. a URL)
  * suggest an NLTK name for the corpus (a short string, use underscore to separate multiple words, cf [existing names](https://github.com/nltk/nltk_data/tree/gh-pages/packages/corpora))
  * document the fact that the corpus is freely redistributable (e.g. available under a Creative Commons ShareAlike license; or invite it's creator to add a comment via the issue tracker).
  * wait for approval from someone in the [NLTK team](https://github.com/orgs/nltk/teams/team-nltk).
2. Prepare a pull request:
  * fork the nltk_data repository: https://github.com/nltk/nltk_data/fork
  * clone the repository and check out the `gh-pages` branch
  * open the `packages/corpora` directory
  * create a new subdirectory, using the corpus name agreed in step 1
  * include 
