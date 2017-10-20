These are frequently asked questions on StackOverflow.


[What are all possible pos tags of NLTK?](https://stackoverflow.com/q/15388831/610569)
====

Depending on the POS tagger you're using, the list of possible tags for each POS tagger is unique.

(Got to work... so continue this answer later


How to setup Stanford tools with NLTK?
====

There are many questions on this in StackOverflow but the more prominent ones with solutions are:

 - For NLTK v3.2.5 (only taggers and tokenizers) see https://stackoverflow.com/a/46781723/610569
 - For NLTK v3.2.4 (parsers, taggers and tokenizers/segmenters) see https://stackoverflow.com/q/13883277/610569


[How to remove stopwords with NLTK?](https://stackoverflow.com/questions/5486337/how-to-remove-stop-words-using-nltk-or-python)
====

```python
from nltk.corpus import stopwords
from nltk import word_tokenize

stoplist = set(stopwords.words('english'))

sent = "The quick brown fox jumps over the lazy dog"
tokenized_sent = word_tokenize(sent.lower())
tokenized_sent_nostop = [token for token in tokenized_sent if token not in stoplist]
```


[How to extract 4-grams, 5-grams, 6-grams, etc.?](https://stackoverflow.com/q/17531684/610569)
====

For bigrams and trigrams:

```python
from nltk word_tokenize
from nltk import bigrams, trigrams

sent = word_tokenize("The quick brown fox jumps over the lazy dog")
sent_bigrams = bigrams(sent)
sent_trigrams = trigrams(sent)
```

For n-grams with other order of n:

```python
from nltk import ngrams
from nltk import word_tokenize

sent = word_tokenize("The quick brown fox jumps over the lazy dog")
sent_unigrams = ngrams(sent, 1)
sent_4grams =  ngrams(sent, 4)
```

If you want to extract n-grams for m to n order, use `everygrams`:

```python
from nltk import everygrams
from nltk import word_tokenize

sent = word_tokenize("The quick brown fox jumps over the lazy dog")
# Extracts 2-grams, 3-grams and 4-grams
sent_2to4grams = everygrams(sent, 2, 4)
```


**Note:** 

 - The `bigrams`, `trigrams` and `ngrams` functions returns a generator, so you might want to do `list(ngrams(sent, 4))` to materialize the generator.
 - The input for these n-grams function are list of strings, generally the input needs to be tokenized to get word n-grams. Otherwise it would return character n-grams


[How to config nltk data directory from code?](https://stackoverflow.com/q/3522372/610569)
====


To modify the path, simply append to the list of possible paths:

```python
import nltk
nltk.data.path.append("/home/yourusername/whateverpath/")
```

Or in Windows:

```
import nltk
nltk.data.path.append("C:\somewhere\farfar\away\path")
```

[How to download NLTK data?](https://stackoverflow.com/q/22211525/610569)
====

To download a particular dataset/models, use the `nltk.download()` function, e.g. if you are looking to download the punkt sentence tokenizer, use:

```
$ python
>>> import nltk
>>> nltk.download('punkt')
```

If you're unsure of which data/model you need, you can start out with the basic list of data + models with:

```python
>>> import nltk
>>> nltk.download('popular')
```

It will download a list of "popular" resources, these includes:

```
<collection id="popular" name="Popular packages">
      <item ref="cmudict" />
      <item ref="gazetteers" />
      <item ref="genesis" />
      <item ref="gutenberg" />
      <item ref="inaugural" />
      <item ref="movie_reviews" />
      <item ref="names" />
      <item ref="shakespeare" />
      <item ref="stopwords" />
      <item ref="treebank" />
      <item ref="twitter_samples" />
      <item ref="omw" />
      <item ref="wordnet" />
      <item ref="wordnet_ic" />
      <item ref="words" />
      <item ref="maxent_ne_chunker" />
      <item ref="punkt" />
      <item ref="snowball_data" />
      <item ref="averaged_perceptron_tagger" />
    </collection>
```

From v3.2.5, NLTK should have a more informative error message when nltk_data resource is not found, e.g.:

```python
>>> from nltk import word_tokenize
>>> word_tokenize('x')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/Users/l/alvas/git/nltk/nltk/tokenize/__init__.py", line 128, in word_tokenize
    sentences = [text] if preserve_line else sent_tokenize(text, language)
  File "/Users//alvas/git/nltk/nltk/tokenize/__init__.py", line 94, in sent_tokenize
    tokenizer = load('tokenizers/punkt/{0}.pickle'.format(language))
  File "/Users/alvas/git/nltk/nltk/data.py", line 820, in load
    opened_resource = _open(resource_url)
  File "/Users/alvas/git/nltk/nltk/data.py", line 938, in _open
    return find(path_, path + ['']).open()
  File "/Users/alvas/git/nltk/nltk/data.py", line 659, in find
    raise LookupError(resource_not_found)
LookupError: 
**********************************************************************
  Resource punkt not found.
  Please use the NLTK Downloader to obtain the resource:

  >>> import nltk
  >>> nltk.download('punkt')

  Searched in:
    - '/Users/alvas/nltk_data'
    - '/usr/share/nltk_data'
    - '/usr/local/share/nltk_data'
    - '/usr/lib/nltk_data'
    - '/usr/local/lib/nltk_data'
    - ''
**********************************************************************

```