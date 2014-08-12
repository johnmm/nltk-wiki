Sentiment analysis has a wide appeal as providing information about the subjective dimension of texts. It can be regarded as a classification technique, either binary (polarity classification into positive/negative) or multi-class categorization (e.g. positive/neutral/negative) . 

Most approaches use a sentiment lexicon as a component (sometimes the only component). Lexicons can either be general purpose, or extracted from a suitable corpus, such as movie reviews with explicit ranking information.

## General Lexicons

The following seem to be easily available and have suitable licences:

* SentiWordNet (CC-BY-SA) (now available in NLTK)
* Wiebe et al's Subjectivity Lexicon (GPL) (a collection of small lexicons, each in a different format)

There may well be other useful lexical resources that we could adopt.

## Training / Testing Data

It is probably worth illustrating sentiment analysis with both longer texts (e.g. movie review corpus) and shorter ones (e.g. Tweets).

* [Twitter Sentiment](http://www.sananalytics.com/lab/twitter-sentiment/)

* [NLTK Movie review corpus](http://nltk.github.com/nltk_data/packages/corpora/movie_reviews.zip)






## Useful links
* [Pang and Lee, 'Opinion mining and sentiment analysis'](http://www.cs.cornell.edu/home/llee/omsa/omsa-published.pdf)
* [Liu (2010) 'Sentiment Analysis and Subjectivity'](http://www.cs.uic.edu/~liub/FBS/NLP-handbook-sentiment-analysis.pdf)