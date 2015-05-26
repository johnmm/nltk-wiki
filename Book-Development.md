This page documents our plans for the development of the NLTK book, leading to a second edition.

1. **Language Processing and the Natural Language Toolkit**
    1. NLP systems: translation (SB), dialogue (done), summarisation (SB), web search (EL), question answering (logic-rich, inferencing approach EK), recommendations (similarity metrics over document collections, EL), sentiment analysis (EK). Pointers to demonstrations online (links hosted at nltk.org to avoid link rot). Motivation. Architecture. Limitations. Discussion to highlight the non-trivial NLP involved. Help readers understand the breadth and limitations of NLP.
        * description, the pieces you need to solve it (architecture diagram if necessary)
        * the fact that there's overlap between these in terms of the required subtasks
        * some very different approaches exist for the above (favour popularity, reasonableness, coverage of approaches across the whole set)
    2. Sub-tasks: WSD, pronoun resolution, entailment, finding things in text, language modeling, collocations, sentence segmentation
    3. Overview of NLTK (simple things you can do, intended to engage non-linguists with the content and non-programmers with the syntax) (SB)
    4. Overview of book
    5. Summary
    6. Further Reading
    7. Exercises

2. **Accessing Text Corpora and Lexical Resources**
    1. Accessing Text Corpora _mention NomBank, PropBank_ [ewanklein]
    2. Conditional Frequency Distributions
    3. Lexical Resources _add FrameNet, VerbNet, Sentiwordnet_ [edloper]
    4. WordNet _add Open Multilingual WordNet_ [stevenbird]
    5. Summary
    6. Further Reading
    7. Exercises
3. **Processing Raw Text**
    1. Accessing Text from the Web and from Disk (_add Twitter_) [ewanklein]
    2. Strings: Text Processing at the Lowest Level
    3. Text Processing with Unicode _updated for Python 3 including bytes type_ – but this will already be done [edloper]
    4. Regular Expressions for Detecting Word Patterns
    5. Useful Applications of Regular Expressions
    6. Normalizing Text (_add Twitter_) [ewanklein]
    7. Regular Expressions for Tokenizing Text
    8. Segmentation
    9. Formatting: From Lists to Strings (_update to use string.format_ – but this will already be done)
    10. _Scaling up (incl how to use the Stanford tokenizer)_ [stevenbird]
    11. Summary
    12. Further Reading
    13. Exercises

4. **Language Modeling** [edloper]
  1. n-gram models
  2. bins: forming equivalence classes
  3. independence assumptions
  4. sparse data problems.
  5. statistical estimators (MLE, laplace, heldout, etc)
  6. combining estimators
  7. word clusters and word similarity
  8. word embeddings
  9. scaling up -- show how to perform some task that we've already performed, but using an external tool and a larger data set.  Should be a short section, but enough to show how to use the interface to the external tool, and to show the performance difference etc.
  10. Summary
  11. Further Reading
  12. Exercises

    
5. **Categorizing and Tagging Words**
    1. Using a Tagger
    2. Tagged Corpora _mention MASC tagged corpus?_ [stevenbird]
    3. Mapping Words to Properties Using Python Dictionaries
    4. Automatic Tagging
    5. N-Gram Tagging
    6. Transformation-Based Tagging
    7. How to Determine the Category of a Word
    8. _Scaling Up (incl how to use the Stanford tagger)_ [stevenbird]
    9. Summary
    10. Further Reading
    11. Exercises
6. **Learning to Classify Text**
    1. Supervised Classification
    2. Further Examples of Supervised Classification
    3. Evaluation
    4. Decision Trees
    5. Naive Bayes Classifiers
    6. Maximum Entropy Classifiers
    7. Modeling Linguistic Patterns
    8. _Sentiment Detection (incl sentiwordnet); here or in chapter 7_ [ewanklein]
    9. _Scaling Up_ [edloper]
    10. Summary
    11. Further Reading
    12. Exercises
7. **Extracting Information from Text**
    1. Information Extraction
    2. Chunking (decide which interface to use: chunking, tagging, or parsing)
    3. Developing and Evaluating Chunkers
    4. Recursion in Linguistic Structure
    5. Named Entity Recognition
    6. Relation Extraction
    7. _Scaling Up (incl how to use the Stanford chunker and named entity recognizer)_ [edloper]
    8. Summary
    9. Further Reading
    10. Exercises
8. **Analyzing Sentence Structure**
    1. Some Grammatical Dilemmas
    2. What's the Use of Syntax?
    3. Context Free Grammar
    4. Parsing With Context Free Grammar
    5. _Combinatory Categorial Grammar_ [ewanklein]
    5. Dependencies and Dependency Grammar [edloper]
        * _split into two sections:_
        * _(a) heads, arguments, and roles (mentions FrameNet, VerbNet, NomBank, PropBank)_
        * _(b) dependency grammar and dependency parsing_
    6. Grammar Development (_could this work in chapter 9?_)
    7. _Scaling Up (incl how to use the Stanford parser)_ [edloper]
    8. Summary
    9. Further Reading
    10. Exercises
9. **Building Feature Based Grammars**
    1. Grammatical Features
    2. Processing Feature Structures
    3. Extending a Feature based Grammar
    4. Summary
    5. Further Reading
    6. Exercises
10. **Analyzing the Meaning of Sentences**
    1. Natural Language Understanding
    2. ~~Propositional Logic~~
    3. ~~First-Order Logic~~
    2. Logic-based Semantics
    4. The Semantics of English Sentences
    5. ~~Discourse Semantics~~
    6. _Learning to build logical representations_ [tbd, depends on new implementation]
    6. Summary
    7. Further Reading
    8. Exercises
11. **Managing Linguistic Data**
    1. Corpus Structure: a Case Study
    2. The Life-Cycle of a Corpus
    3. Acquiring Data
    4. Working with XML
    5. ~~Working with Toolbox Data~~ _Working with FLEx Data_ [stevenbird]
    6. Describing Language Resources using OLAC Metadata
    7. Summary
    8. Further Reading
    9. Exercises
12. _**Further Topics**_
    1. _Machine Translation_ [stevenbird]
       * _Sentence Alignment (incl Gale-Church algorithm)_
       * _Word Alignment (IBM model 1; mention existence of other models)_
       * _Aligned Corpora_
       * _Decoding_ [depends on new implementation]
       * _Evaluation_
    2. _Twitter Processing_
    3. _Sentiment Analysis_
    4. _Further Reading_
    5. _Exercises_

13. _**Appendix: Enough Python for this Book**_ (incorporating material from old chapters 1 and 4)
    1. Getting started with Python (from 1.1)
    1. Texts as lists of words (lists, variables, strings, from 1.2)
    2. Making decisions and taking control (conditionals, comprehensions, nesting, from 1.4)
    3. Sequences (includes tuples, from 4.2)
    4. Functions and modules (from 2.3 and 4.4)
    5. Doing more with functions (from 4.5, plus module structure from 4.6)
    6. Getting started with NLTK (from 1.1 and 1.3)
    7. Exercises

14. _**Appendix: Useful Python libraries for NLP**_ (from 4.8)
    1. matplotlib
    2. networkx
    3. csv
    4. numpy
    5. scikit-learn
    6. gensim


#Workplan#

We are working on groups of chapters as indicated in the following diagram:

![Book development plan](https://github.com/nltk/nltk_book/blob/master/images/2nd_ed_plan.png)