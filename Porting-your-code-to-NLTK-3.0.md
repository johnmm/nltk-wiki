NLTK 3.0 contains a number of interface changes. These are being incorporated into a new version of the [NLTK book](http://nltk.org/book3), updated for Python 3 and NLTK 3.

The way NLTK works with unicode is changed: NLTK3 requires all text input to be unicode and always return text as unicode. Previously, some functions and classes worked on unicode and others required encoded bytestrings. Please make sure you're passing unicode to NLTK and expecting unicode output from NLTK - existing code that assumes bytestrings may start to fail.

Here are some changes you may need to make:

* `nltk.grammar`: `ContextFreeGrammar` &rarr; `CFG`, `WeightedGrammar` &rarr; `PCFG`, `StatisticalDependencyGrammar` &rarr; `ProbabilisticDependencyGrammar`, `WeightedProduction` &rarr; `ProbabilisticProduction`
* `nltk.draw.tree`: `TreeSegmentWidget.node()` &rarr; `TreeSegmentWidget.label()`, `TreeSegmentWidget.set_node()` &rarr; `TreeSegmentWidget.set_label()`
* `nltk.ccg.parse.chart`: `EdgeI.next()` &rarr; `EdgeI.nextsym()`
* Chunk parser: `top_node` &rarr; `root_label`; `chunk_node` &rarr; `chunk_label`
* WordNet properties are now access methods, e.g. `Synset.definition` &rarr; `Synset.definition()`
* `nltk.sem.relextract`: `mk_pairs()` &rarr; `_tree2semi_rel()`, `mk_reldicts()` &rarr; `semi_rel2reldict()`, `show_clause()` &rarr; `clause()`, `show_raw_rtuple()` &rarr; `rtuple()`
* `corpusname.tagged_words(simplify_tags=True)` &rarr; `corpusname.tagged_words(tagset='universal')`
* `nltk.util.clean_html()` &rarr; `BeautifulSoup.get_text()`. `clean_html()` is now dropped, install & use BeautifulSoup or some other html parser instead.
* `nltk.util.ibigrams()` &rarr; `nltk.util.bigrams()`
* `nltk.util.ingrams()` &rarr; `nltk.util.ngrams()`
* `nltk.util.itrigrams()` &rarr; `nltk.util.trigrams()`
* `nltk.metrics.windowdiff` &rarr; `nltk.metrics.segmentation.windowdiff()`, `nltk.metrics.windowdiff.demo()` was removed.
* `nltk.parse.generate2` was re-written and merged into `nltk.parse.generate`

Creating objects from strings:

* Many objects now support a `fromstring()` method
* `nltk.tree.Tree.parse()` &rarr; `nltk.tree.Tree.fromstring()`
* `nltk.tree.Tree()` &rarr; `nltk.tree.Tree.fromstring()`
* `nltk.chunk.RegexpChunkRule.parse()` &rarr; `nltk.chunkRegexpChunkRule.fromstring()`
* `nltk.grammar.parse_cfg()` &rarr; `nltk.ContextFreeGrammar.fromstring()` (same for other types of grammar)

Operations on lists of sentences or other items:
* `nltk.tokenize.batch_tokenize()` &rarr; `nltk.tokenize.tokenize_sents()`
* `nltk.tag.batch_tag()` &rarr; `nltk.tag.tag_sents()`
* `nltk.parse.batch_parse()` &rarr; `nltk.parse.parse_sents()`
* `nltk.classify.batch_classify()` &rarr; `nltk.classify.classify_many()`
* `nltk.sem.batch_interpret()` &rarr; `nltk.sem.interpret_sents()`
* `nltk.sem.batch_evaluate()` &rarr; `nltk.sem.evaluate_sents()`

Changes in `nltk.probability.FreqDist`:

* `fdist.keys()` &rarr; `sorted(fdist)`
* `fdist.inc(x)` &rarr; `fdist[x] += 1`
* `fdist.samples()` &rarr; `sorted(fdist.keys())`
* `fdist.Nr(r)` &rarr; `fdist.Nr()[r]`
* `fdist.Nr_nonzero()` &rarr; `fdist.Nr().items()`
* `cfdist.conditions()` &rarr; `sorted(cfdist.conditions())`

Porter stemmer changes:

* `adjust_case()`, `cons()`, `cvc()`, `doublec()`, `m()`, `step1ab()`, `step1c()`, `step2()`, `step3()`, `step4()`, `step5()`, `vowelinstem()` made private
* `ends()`, `r()`, `setto()` removed

Removed modules, classes and functions:

* `nltk.classify.svm` was removed. For classification based on support vector machines (SVMs) use `nltk.classify.scikitlearn` or [scikit-learn](http://scikit-learn.org) directly. See https://github.com/nltk/nltk/issues/450.
* `nltk.probability.GoodTuringProbDist` class was removed. See https://github.com/nltk/nltk/issues/381.
* `HiddenMarkovModelTaggerTransformI` and its subclasses are removed. See https://github.com/nltk/nltk/issues/374.
* `nltk.classify.maxent` no longer support algorithms backed by `scipy.maxentropy`. See https://github.com/nltk/nltk/issues/321.
* `nltk.misc.babelfish` was removed. See https://github.com/nltk/nltk/issues/265.
* `nltk.sourcedstring` was removed. See https://github.com/nltk/nltk/issues/322.
* `nltk.yamltags` was removed. JSON is now preferred instead. See https://github.com/nltk/nltk/issues/540
* `nltk.mallet` was removed, including the `nltk.tag.crf` module. See https://github.com/nltk/nltk/issues/104
* `nltk.tag.simplify` was removed. See https://github.com/nltk/nltk/issues/483
* `nltk.model` was removed. See https://github.com/nltk/nltk/issues?labels=model
* `nltk.corpus.reader.wordnet._lcs_by_depth` was removed. See https://github.com/nltk/nltk/issues/422.

Miscellaneous changes:

* `nltk.probability.ConditionalProbDist.default_factory` now inherits from `dict` instead of `defaultdict`
* `nltk.probability.ConditionalProbDistI.default_factory` now inherits from `dict` instead of `defaultdict`
* `nltk.probability.DictionaryConditionalProbDist.default_factory` now inherits from `dict` instead of `defaultdict`

More background on Python 3 and NLTK 3:

* http://docs.python.org/2/library/2to3.html
* http://docs.python.org/dev/whatsnew/3.0.html
* http://nltk.org/dev/python3porting.html