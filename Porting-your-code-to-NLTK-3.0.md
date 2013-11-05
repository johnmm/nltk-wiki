NLTK 3.0 contains a number of interface changes. These are being incorporated into a new version of the [NLTK book](http://nltk.org/book3), updated for Python 3 and NLTK 3.

Here are some changes you may need to make:

* Tree.node -> Tree.label() / Tree.set_label()
* Chunk parser: top_node -> root_label; chunk_node -> chunk_label
* WordNet properties are now access methods, e.g. Synset.definition -> Synset.definition()
* relextract: show_raw_rtuple() -> rtuple(), show_clause() -> clause()
* corpusname.tagged_words(simplify_tags=True) -> corpusname.tagged_words(tagset='universal')
* clean_html -> BeautifulSoup.get_text

