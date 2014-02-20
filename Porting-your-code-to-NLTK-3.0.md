NLTK 3.0 contains a number of interface changes. These are being incorporated into a new version of the [NLTK book](http://nltk.org/book3), updated for Python 3 and NLTK 3.

Here are some changes you may need to make:

* `Tree.node` &rarr; `Tree.label()` / `Tree.set_label()`
* Chunk parser: `top_node` &rarr; `root_label`; `chunk_node` &rarr; `chunk_label`
* WordNet properties are now access methods, e.g. `Synset.definition` &rarr; `Synset.definition()`
* relextract: `show_raw_rtuple()` &rarr; `rtuple()`, `show_clause()` &rarr; `clause()`
* `corpusname.tagged_words(simplify_tags=True)` &rarr; `corpusname.tagged_words(tagset='universal')`
* `clean_html()` &rarr; `BeautifulSoup.get_text()` (`clean_html()` is now dropped, install & use BeautifulSoup or some other html parser instead)
* `nltk.util.ibigrams()` &rarr; `nltk.util.bigrams()`
* `nltk.util.ingrams()` &rarr; `nltk.util.ngrams()`
* `nltk.util.itrigrams()` &rarr; `nltk.util.trigrams()`

Changes in `nltk.probability.FreqDist`:

* `fdist.keys()` &rarr; `sorted(fdist)`
* `fdist.inc(x)` &rarr; `fdist[x] += 1`
* `fdist.samples()` &rarr; `sorted(fdist.keys())`
* `fdist.Nr(r)` &rarr; `fdist.Nr()[r]`
* `fdist.Nr_nonzero()` &rarr; `fdist.Nr().items()`
* `cfdist.conditions()` &rarr; `sorted(cfdist.conditions())`

Removed modules and classes:

* `nltk.classify.svm` was removed. For classification based on support vector machines (SVMs) use `nltk.classify.scikitlearn` or [scikit-learn](http://scikit-learn.org) directly. See https://github.com/nltk/nltk/issues/450.
* `nltk.corpus.reader.wordnet._lcs_by_depth` was removed. See https://github.com/nltk/nltk/issues/422.
* `nltk.probability.GoodTuringProbDist` class is removed. See https://github.com/nltk/nltk/issues/381.
* `HiddenMarkovModelTaggerTransformI` and its subclasses are removed. See https://github.com/nltk/nltk/issues/374.
* `nltk.classify.maxent` no longer support algorithms backed by `scipy.maxentropy`. See https://github.com/nltk/nltk/issues/321.
* `nltk.misc.babelfish` is removed. See https://github.com/nltk/nltk/issues/265.
* `nltk.sourcedstring` is removed. See https://github.com/nltk/nltk/issues/322.
* `nltk.yamltags` is removed. JSON is now preferred instead. See https://github.com/nltk/nltk/issues/540
* `nltk.mallet` is removed, including the `nltk.tag.crf` module. See https://github.com/nltk/nltk/issues/104

Porter stemmer changes:

* `nltk.stem.porter.PorterStemmer.adjust_case` made private
* `nltk.stem.porter.PorterStemmer.cons` made private
* `nltk.stem.porter.PorterStemmer.cvc` made private
* `nltk.stem.porter.PorterStemmer.doublec` made private
* `nltk.stem.porter.PorterStemmer.m` made private
* `nltk.stem.porter.PorterStemmer.step1ab` made private
* `nltk.stem.porter.PorterStemmer.step1c` made private
* `nltk.stem.porter.PorterStemmer.step2` made private
* `nltk.stem.porter.PorterStemmer.step3` made private
* `nltk.stem.porter.PorterStemmer.step4` made private
* `nltk.stem.porter.PorterStemmer.step5` made private
* `nltk.stem.porter.PorterStemmer.vowelinstem` made private
* `nltk.stem.porter.PorterStemmer.ends` removed
* `nltk.stem.porter.PorterStemmer.r` removed
* `nltk.stem.porter.PorterStemmer.setto` removed

Miscellaneous changes:

* `nltk.probability.ConditionalProbDist.default_factory` now inherits from `dict` instead of `defaultdict`
* `nltk.probability.ConditionalProbDistI.default_factory` now inherits from `dict` instead of `defaultdict`
* `nltk.probability.DictionaryConditionalProbDist.default_factory` now inherits from `dict` instead of `defaultdict`

The way NLTK works with unicode is changed: NLTK3 requires all text input to be unicode and always return text as unicode. Previously, some functions and classes worked on unicode and others required encoded bytestrings. Please make sure you're passing unicode to NLTK and expecting unicode output from NLTK - existing code that assumes bytestrings may start to fail.

More background on Python 3 and NLTK 3:

* http://docs.python.org/2/library/2to3.html
* http://docs.python.org/dev/whatsnew/3.0.html
* http://nltk.org/dev/python3porting.html