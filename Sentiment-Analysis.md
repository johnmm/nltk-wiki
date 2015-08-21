Sentiment analysis has a wide appeal as providing information about the subjective dimension of texts. It can be regarded as a classification technique, either binary (polarity classification into positive/negative) or multi-class categorization (e.g. positive/neutral/negative). 

Most approaches use a sentiment lexicon as a component (sometimes the only component). Lexicons can either be general purpose, or extracted from a suitable corpus, such as movie reviews with explicit ranking information. 

We now have much better support for sentiment analysis in NLTK, with the following resources having been added:


# Lexicons

- ***Opinion Lexicon by Bing Liu***

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#lexicon
  - **PAPERS**: [Mining and summarizing customer reviews](http://www.cs.uic.edu/~liub/publications/kdd04-revSummary.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**:



----------------------

# Datasets

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




## Next Steps

* Follow-up on request to distribute MPQA subjectivity lexicon (and possible other resources) under non-viral license.
* Build a trained model of sentiment for a large-ish Tweet corpus
* Add a module for feature-based classification (e.g. using the Customer Product Reviews)



# Sentiment Analysis MSc Thesis
##### Pierpaolo Pantone
----------------------

# Lexicons

- ***Opinion Lexicon by Bing Liu***

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#lexicon
  - **PAPERS**: [Mining and summarizing customer reviews](http://www.cs.uic.edu/~liub/publications/kdd04-revSummary.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**:

- ***MPQA Subjectivity Lexicon***

  - **URL**: [http://mpqa.cs.pitt.edu/#subj_lexicon]
  - **PAPERS**: [Recognizing Contextual Polarity in Phrase-Level Sentiment Analysis (Theresa Wilson, Janyce Wiebe, and Paul Hoffmann, 2005)](http://people.cs.pitt.edu/~wiebe/pubs/papers/emnlp05polarity.pdf).
  - **CONTACT**: mpqa.project@gmail.com
  - **NOTES**: GNU Public License

- ***SentiWordNet***

  - **NOTES**: Already included in NLTK

- ***Harvard General Inquirer***

  - **URL**: http://www.wjh.harvard.edu/~inquirer/
  - **PAPERS**: [The General Inquirer: A Computer Approach to Content Analysis (Stone, Philip J; Dexter C. Dunphry; Marshall S. Smith; and Daniel M. Ogilvie. 1966)](http://psycnet.apa.org/psycinfo/1967-04539-000)
  - **CONTACT**:
  - **NOTES**: Website is apparently down

- ***~~Linguistic Inquiry and Word Counts (LIWC)~~***

  - **URL**: http://www.liwc.net/
  - **PAPERS**:
  - **CONTACT**:
  - **NOTES**: Not suitable (proprietary database)

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

- ***~~Experience Project~~***
  - **URL**:
  - **PAPERS**:
  - **CONTACT**:
  - **NOTES**: Not suitable (copyright).

  > All content included on this site, such as text, graphics, logos, button icons, images, audio clips, digital downloads, data compilations, and software, is the property of Experience Project or its content suppliers and protected by United States and international copyright laws.

- ***Sentiment140*** (Tweets)

  - **URL**: http://help.sentiment140.com/for-students
  - **PAPERS**: [Twitter Sent classification using Distant Supervision (Go, Alec, Richa Bhayani, and Lei Huang)](http://cs.stanford.edu/people/alecmgo/papers/TwitterDistantSupervision09.pdf)
  - **CONTACT**: http://help.sentiment140.com/
           https://groups.google.com/forum/#!forum/sentiment140
  - **NOTES**: "polarity","id","date","query","user","text"

- ***STS-Gold*** (Tweets)

  - **URL**: http://www.tweenator.com/index.php?page_id=13
  - **PAPERS**: [Evaluation datasets for twitter sentiment analysis (Saif, Fernandez, He, Alani)](http://ceur-ws.org/Vol-1096/paper1.pdf)
  - **CONTACT**: Hassan Saif (h.saif@open.ac.uk)
  - **NOTES**: As Sentiment140, but the dataset is smaller and with human annotators. It comes with 3 files: tweets, entities (with their sentiment) and an aggregate set.

- ***Customer Review Dataset*** (Product reviews)

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#datasets
  - **PAPERS**: [Mining and summarizing customer reviews](http://www.cs.uic.edu/~liub/publications/kdd04-revSummary.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**: Title of review, product feature, positive/negative label with opinion strength, other info (comparisons, pronoun resolution, etc.)

- ***Amazon Product Review Data*** (Product Reviews)

  - **URL**: http://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#datasets
  - **PAPERS**: [Opinion Spam and Analysis (Jindal, Liu)](http://www.cs.uic.edu/~liub/FBS/opinion-spam-WSDM-08.pdf)
  - **CONTACT**: Bing Liu (liub@cs.uic.edu)
  - **NOTES**: Available upon request to Bing Liu (so I suppose it cannot be incorporated in NLTK)

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

- ***~~SemEval 2014~~*** (Tweets)

  - **URL**: http://alt.qcri.org/semeval2014/task9/
  - **PAPERS**:
  - **CONTACT**:
  - **NOTES**: Not suitable for our purpose:

  > You MUST NOT re-distribute the tweets, the annotations or the corpus obtained (from the readme file)

- ***Various Datasets*** (Reviews)

  - **URL**: https://personalwebs.coloradocollege.edu/~mwhitehead/html/opinion_mining.html
  - **PAPERS**: [Building a General Purpose Cross-Domain Sentiment Mining Model (Whitehead and Yaeger)](https://personalwebs.coloradocollege.edu/~mwhitehead/files/cross_domain_training.pdf), [Sentiment Mining Using Ensemble Classification Models (Whitehead and Yaeger)](https://personalwebs.coloradocollege.edu/~mwhitehead/files/whitehead_yaeger_scss08b.pdf)
  - **CONTACT**:
  - **NOTES**:

  > "If you find these datasets useful, then we ask that you please cite the first paper"

- ***Various Datasets #2*** (Reviews)

  - **URL**: http://www.text-analytics101.com/2011/07/user-review-datasets_20.html
  - **PAPERS**:
  - **CONTACT**:
  - **NOTES**:




## Useful links
* [Pang and Lee, 'Opinion mining and sentiment analysis'](http://www.cs.cornell.edu/home/llee/omsa/omsa-published.pdf)
* [Liu (2010) 'Sentiment Analysis and Subjectivity'](http://www.cs.uic.edu/~liub/FBS/NLP-handbook-sentiment-analysis.pdf)