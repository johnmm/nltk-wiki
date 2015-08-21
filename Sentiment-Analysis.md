# Sentiment Analysis Overview

Sentiment analysis has a wide appeal as providing information about the subjective dimension of texts. It can be regarded as a classification technique, either binary (polarity classification into positive/negative) or multi-class categorization (e.g. positive/neutral/negative). 

Most approaches use a sentiment lexicon as a component (sometimes the only component). Lexicons can either be general purpose, or extracted from a suitable corpus, such as movie reviews with explicit ranking information. 

We now have much better support for sentiment analysis in NLTK, with the following resources having been added:

## Lexicons

- ***Opinion Lexicon by Bing Liu***

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#lexicon
  - **PAPERS**: [Mining and summarizing customer reviews](http://www.cs.uic.edu/~liub/publications/kdd04-revSummary.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**:

----------------------

## Datasets

- ***Customer Review Dataset*** (Product reviews)

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#datasets
  - **PAPERS**: [Mining and summarizing customer reviews](http://www.cs.uic.edu/~liub/publications/kdd04-revSummary.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**: Title of review, product feature, positive/negative label with opinion strength, other info (comparisons, pronoun resolution, etc.)


- ***Pros and Cons Dataset*** (Pros and cons sentences)

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#datasets
  - **PAPERS**: [Mining Opinions in Comparative Sentences (Ganapathibhotla, Liu 2008)](http://www.cs.uic.edu/~liub/FBS/Coling-2008-camera-ready.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**: A list of sentences tagged `<pros>` or `<cons>`

- ***Comparative Sentences*** (Reviews)

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#datasets
  - **PAPERS**: [Identifying Comparative Sentences in Text Documents (Nitin Jindal and Bing Liu)](http://www.cs.uic.edu/~liub/publications/sigir06-comp.pdf), [Mining Opinion Features in Customer Reviews (Minqing Hu and Bing Liu)](http://www.cs.uic.edu/~liub/publications/aaai04-featureExtract.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**: Sentence, POS-tagged sentence, entities, comparison type (non-equal, equative, superlative, non-gradable)


# Next Steps


* Build a trained model of sentiment for a large-ish Tweet corpus
* Add a module for feature-based classification (e.g. using the Customer Product Reviews)

We should also investigate the following resources:


# Lexicons

- ***MPQA Subjectivity Lexicon***

  - **URL**: [http://mpqa.cs.pitt.edu/#subj_lexicon]
  - **PAPERS**: [Recognizing Contextual Polarity in Phrase-Level Sentiment Analysis (Theresa Wilson, Janyce Wiebe, and Paul Hoffmann, 2005)](http://people.cs.pitt.edu/~wiebe/pubs/papers/emnlp05polarity.pdf).
  - **CONTACT**: mpqa.project@gmail.com
  - **NOTES**: GNU Public License


- ***Harvard General Inquirer***
  - **URL**: http://www.wjh.harvard.edu/~inquirer/
  - **PAPERS**: [The General Inquirer: A Computer Approach to Content Analysis (Stone, Philip J; Dexter C. Dunphry; Marshall S. Smith; and Daniel M. Ogilvie. 1966)](http://psycnet.apa.org/psycinfo/1967-04539-000)
  - **CONTACT**:
  - **NOTES**: Not clear if lexicon is available for download -- possibly for academic use only


----------------------

# Datasets

- ***MPQA Datasets***

  - **URL**: http://mpqa.cs.pitt.edu/
  - **PAPERS**: Various
  - **CONTACT**: mpqa.project@gmail.com
  - **NOTES**: GNU Public License. These datasets could be interesting.

    - Political Debate data
    - Product Debate data
    - Subjectivity Sense Annotations (could be useful for subjectivity classification)



- ***STS-Gold*** (Tweets)

  - **URL**: http://www.tweenator.com/index.php?page_id=13
  - **PAPERS**: [Evaluation datasets for twitter sentiment analysis (Saif, Fernandez, He, Alani)](http://ceur-ws.org/Vol-1096/paper1.pdf)
  - **CONTACT**: Hassan Saif (h.saif@open.ac.uk)
  - **NOTES**: As Sentiment140, but the dataset is smaller and with human annotators. It comes with 3 files: tweets, entities (with their sentiment) and an aggregate set.

- ***Sanders Analytics Twitter Sentiment Corpus*** (Tweets)

  - **URL**: http://www.sananalytics.com/lab/twitter-sentiment/
  - **PAPERS**:
  - **CONTACT**: Niek Sanders (njs@sananalytics.com)
  - **NOTES**:

  > 5513 hand-classified tweets wrt 4 different topics. Because of Twitter’s ToS, a small Python script is included to download all of the tweets. The sentiment classifications themselves are provided free of charge and without restrictions. They may be used for commercial products. They may be redistributed. They may be modified.

- ***Spanish tweets*** (Tweets)

  - **URL**: http://www.daedalus.es/TASS2013/corpus.php
  - **PAPERS**:
  - **CONTACT**:
  - **NOTES**:

- ***SemEval 2014*** (Tweets)

  - **URL**: http://alt.qcri.org/semeval2014/task9/
  - **PAPERS**:
  - **CONTACT**:
  - **NOTES**: Check licensing of annotations


