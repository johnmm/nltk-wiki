NLTK 3.0 contains a number of interface changes. These are being incorporated into a new version of the [NLTK book](http://nltk.org/book3), updated for Python 3 and NLTK 3.

The way NLTK works with unicode is changed: NLTK3 requires all text input to be unicode and always return text as unicode. Previously, some functions and classes worked on unicode and others required encoded bytestrings. Please make sure you're passing unicode to NLTK and expecting unicode output from NLTK - existing code that assumes bytestrings may start to fail.

Here are some changes you may need to make:
* `grammar`: `ContextFreeGrammar` &rarr; `CFG`, `WeightedGrammar` &rarr; `PCFG`, `StatisticalDependencyGrammar` &rarr; `ProbabilisticDependencyGrammar`, `WeightedProduction` &rarr; `ProbabilisticProduction`
* `draw.tree`: `TreeSegmentWidget.node()` &rarr; `TreeSegmentWidget.label()`, `TreeSegmentWidget.set_node()` &rarr; `TreeSegmentWidget.set_label()`
* parsers: `nbest_parse()` &rarr(); `parse()`
* `ccg.parse.chart`: `EdgeI.next()` &rarr; `EdgeI.nextsym()`
* Chunk parser: `top_node` &rarr; `root_label`; `chunk_node` &rarr; `chunk_label`
* WordNet properties are now access methods, e.g. `Synset.definition` &rarr; `Synset.definition()`
* `sem.relextract`: `mk_pairs()` &rarr; `_tree2semi_rel()`, `mk_reldicts()` &rarr; `semi_rel2reldict()`, `show_clause()` &rarr; `clause()`, `show_raw_rtuple()` &rarr; `rtuple()`
* `corpusname.tagged_words(simplify_tags=True)` &rarr; `corpusname.tagged_words(tagset='universal')`
* `util.clean_html()` &rarr; `BeautifulSoup.get_text()`. `clean_html()` is now dropped, install & use BeautifulSoup or some other html parser instead.
* `util.ibigrams()` &rarr; `util.bigrams()`
* `util.ingrams()` &rarr; `util.ngrams()`
* `util.itrigrams()` &rarr; `util.trigrams()`
* `metrics.windowdiff` &rarr; `metrics.segmentation.windowdiff()`, `metrics.windowdiff.demo()` was removed.
* `parse.generate2` was re-written and merged into `parse.generate`

Creating objects from strings:
* Many objects now support a `fromstring()` method
* `tree.Tree.parse()` &rarr; `tree.Tree.fromstring()`
* `tree.Tree()` &rarr; `tree.Tree.fromstring()`
* `chunk.RegexpChunkRule.parse()` &rarr; `chunkRegexpChunkRule.fromstring()`
* `grammar.parse_cfg()` &rarr; `ContextFreeGrammar.fromstring()` (same for other types of grammar)
* `sem.LogicParser.parse()` &rarr; `sem.Expression.fromstring()`
* `sem.DrtParser.parse()` &rarr; `sem.DrtExpression.fromstring()`

Operations on lists of sentences or other items:
* `tokenize.batch_tokenize()` &rarr; `tokenize.tokenize_sents()`
* `tag.batch_tag()` &rarr; `tag.tag_sents()`
* `parse.batch_parse()` &rarr; `parse.parse_sents()`
* `classify.batch_classify()` &rarr; `classify.classify_many()`
* `sem.batch_interpret()` &rarr; `sem.interpret_sents()`
* `sem.batch_evaluate()` &rarr; `sem.evaluate_sents()`

Changes in `probability.FreqDist`:
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

* `classify.svm` was removed. For classification based on support vector machines (SVMs) use `classify.scikitlearn` or [scikit-learn](http://scikit-learn.org) directly. See https://github.com/nltk/nltk/issues/450.
* `probability.GoodTuringProbDist` class was removed. See https://github.com/nltk/nltk/issues/381.
* `HiddenMarkovModelTaggerTransformI` and its subclasses are removed. See https://github.com/nltk/nltk/issues/374.
* `classify.maxent` no longer support algorithms backed by `scipy.maxentropy`. See https://github.com/nltk/nltk/issues/321.
* `misc.babelfish` was removed. See https://github.com/nltk/nltk/issues/265.
* `sourcedstring` was removed. See https://github.com/nltk/nltk/issues/322.
* `yamltags` was removed. JSON is now preferred instead. See https://github.com/nltk/nltk/issues/540
* `mallet` was removed, including the `tag.crf` module. See https://github.com/nltk/nltk/issues/104
* `tag.simplify` was removed. See https://github.com/nltk/nltk/issues/483
* `model` was removed. See https://github.com/nltk/nltk/issues?labels=model
* `corpus.reader.wordnet._lcs_by_depth` was removed. See https://github.com/nltk/nltk/issues/422.

Miscellaneous changes:

* `probability.ConditionalProbDist.default_factory` now inherits from `dict` instead of `defaultdict`
* `probability.ConditionalProbDistI.default_factory` now inherits from `dict` instead of `defaultdict`
* `probability.DictionaryConditionalProbDist.default_factory` now inherits from `dict` instead of `defaultdict`

More background on Python 3 and NLTK 3:

* http://docs.python.org/2/library/2to3.html
* http://docs.python.org/dev/whatsnew/3.0.html
* http://nltk.org/dev/python3porting.html