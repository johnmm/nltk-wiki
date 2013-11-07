NLTK 3.0 contains a number of interface changes. These are being incorporated into a new version of the [NLTK book](http://nltk.org/book3), updated for Python 3 and NLTK 3.

Here are some changes you may need to make:

* `Tree.node` &rarr; `Tree.label()` / `Tree.set_label()`
* Chunk parser: `top_node` &rarr; `root_label`; `chunk_node` &rarr; `chunk_label`
* WordNet properties are now access methods, e.g. `Synset.definition` &rarr; `Synset.definition()`
* relextract: `show_raw_rtuple()` &rarr; `rtuple()`, `show_clause()` &rarr; `clause()`
* `corpusname.tagged_words(simplify_tags=True)` &rarr; `corpusname.tagged_words(tagset='universal')`
* `clean_html()` &rarr; `BeautifulSoup.get_text()`
* `fdist.keys()` &rarr; `sorted(fdist)`

More background on NLTK 3:

* http://nltk.org/dev/python3porting.html
