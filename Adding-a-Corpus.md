NLTK comes with a [collection of corpora](http://www.nltk.org/nltk_data/). All corpora are freely redistributable. They live in the `gh-pages` branch of the nltk_data repository.

## Corpus Readers

Each corpus requires a [corpus reader](https://github.com/nltk/nltk/tree/develop/nltk/corpus/reader), plus an entry in the [corpus package](https://github.com/nltk/nltk/blob/develop/nltk/corpus/__init__.py) that allows the corpus to be imported (this entry associates an importable name with a corpus reader and a data source).

If there is not yet a suitable corpus reader, you will need to create one, and submit that as a pull request to the [nltk repository](https://github.com/nltk/nltk).

## Adding a Corpus

We welcome contributions of new corpora to NLTK. Each new corpus imposes a maintenance burden and a possible risk of copyright infringement. So before contributing we ask that you:

1. Only contribute corpora that have obtained a basic level of notability (e.g. there is a publication that describes it, and a community of people who are using it)
2. Ensure that you have permission to redistribute the data, and can document this (e.g. there is an external website where the data is already posted with a licence)
3. Use existing NLTK corpus readers where possible, or else contribute a well-documented corpus reader to NLTK

To add a corpus to NLTK, please follow these steps:

1. Test that you can access the corpus using NLTK:
  * put a copy in your local nltk_data directory. The default system location on Windows is `C:\nltk_data\corpora`; and on Mac and Unix is `/usr/share/nltk_data/corpora`.
  * modify NLTK to support the corpus (see step 4 below)
  * open a Python interpreter and check that you can access the corpus, e.g. `from nltk.corpus import corpus_name`

2. Post a new entry to the nltk_data issue tracker:
  * https://github.com/nltk/nltk_data/issues/new
  * include the corpus name in the title
  * identify the source of the corpus (e.g. a URL)
  * suggest an NLTK name for the corpus (a short string, use underscore to separate multiple words, cf [existing names](https://github.com/nltk/nltk_data/tree/gh-pages/packages/corpora))
  * identify an existing corpus reader for the corpus, or else explain how you plan to create one
  * document the fact that the corpus is freely redistributable (e.g. available under a Creative Commons ShareAlike license; or invite its creator to add a comment via the issue tracker).
  * wait for approval from someone in the [NLTK team](https://github.com/orgs/nltk/teams/team-nltk).

3. Prepare a pull request to the nltk_data repository:
  * fork the nltk_data repository: https://github.com/nltk/nltk_data/fork
  * clone the repository and check out the `gh-pages` branch
  * `mkdir packages/corpora/corpus_name` (using the corpus name agreed in step 1 above)
  * include a `README` file (text file with no extension) at the top level, with the corpus name and source URL for the corpus at the top
  * make sure there are no extraneous files like `.svn`, `.DS_store` or `README~`. 
  * `zip -r corpus_name corpus_name` (NB you can use the `-x` option to exclude unwanted files, e.g., `zip -r corpus_name corpus_name -x "*.DS_Store"`)
  * create `corpus_name.xml` using the metadata template (see below); specify `unzip="1"` if the corpus reader requires the data to be unzipped after being installed (usually not necessary).
  * add the corpus name to `/collections/all.xml`
  * push this to your fork and submit a pull request, referencing the issue from step 1

 (In response to this pull request, an NLTK developer needs to review the request, before running `make` in the top level of the nltk_data repository (gh-pages branch), and then pushing the changes).

4. If necessary, prepare a corpus reader:
  * fork the nltk repository: https://github.com/nltk/nltk/fork
  * clone the repository (make sure you are on the `develop` branch)
  * add the corpus reader in `nltk/nltk/corpus/reader`
  * add an entry in `nltk/corpus/__init__.py` and `nltk/corpus/reader/__init__.py`
  * push this to your fork and submit a pull request, referencing the issue from step 1

### Metadata Template

```
<package id="<corpus_name>" name="<Corpus Name>"
         copyright="Copyright (C) <YEAR> <NAME>"
         author="<NAME>"
         license="<LICENSE NAME OR URL>"
         webpage="<URL FOR CORPUS>"
         unzip="0"
         />
```
