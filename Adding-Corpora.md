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
  * identify an existing corpus reader for the corpus, or else explain how you plan to create one
  * document the fact that the corpus is freely redistributable (e.g. available under a Creative Commons ShareAlike license; or invite it's creator to add a comment via the issue tracker).
  * wait for approval from someone in the [NLTK team](https://github.com/orgs/nltk/teams/team-nltk).
2. Prepare a pull request to the nltk_data repository:
  * fork the nltk_data repository: https://github.com/nltk/nltk_data/fork
  * clone the repository and check out the `gh-pages` branch
  * `mkdir packages/corpora/corpus_name` (using the corpus name agreed in step 1 above)
  * include a `README.txt` file at the top level, with the corpus name and source URL at the top
  * make sure there are no extraneous files like `.svn` or `README.txt~`
  * `zip -r corpus_name corpus_name`
  * push this to your fork and submit a pull request, referencing the issue
3. If necessary, prepare a corpus reader:
  * fork the nltk_data repository: https://github.com/nltk/nltk/fork
  * clone the repository (make sure you are on the `develop` branch)
  * add the corpus reader in `nltk/nltk/corpus/reader`
  * add an entry in `nltk/corpus/__init__.py`
