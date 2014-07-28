This page documents our plans for the development of the NLTK book, leading to a second edition. We will work on groups of chapters as indicated in the following diagram:

![Book development plan](https://github.com/nltk/nltk_book/blob/master/images/2nd_ed_plan.png)

1. **Language Processing and Python**
    1. Computing with Language: Texts and Words
    2. A Closer Look at Python: Texts as Lists of Words
    3. Computing with Language: Simple Statistics
    4. Back to Python: Making Decisions and Taking Control
    5. Automatic Natural Language Understanding
        * _replace babelize example with web link_
    6. Summary
    7. Further Reading
    8. Exercises
2. **Accessing Text Corpora and Lexical Resources**
    1. Accessing Text Corpora _mention NomBank, PropBank, ChaSen, KNBC Japanese_
    2. Conditional Frequency Distributions
    3. More Python: Reusing Code
    4. Lexical Resources _add FrameNet, VerbNet_
    5. WordNet _add Open Multilingual WordNet_
    6. Summary
    7. Further Reading
    8. Exercises
3. **Processing Raw Text**
    1. Accessing Text from the Web and from Disk (_add Twitter_)
    2. Strings: Text Processing at the Lowest Level
    3. Text Processing with Unicode _updated for Python 3 including bytes type_
    4. Regular Expressions for Detecting Word Patterns
    5. Useful Applications of Regular Expressions
    6. Normalizing Text (_add Twitter_)
    7. Regular Expressions for Tokenizing Text
    8. Segmentation
    9. Formatting: From Lists to Strings (_update to use string.format_)
    10. _Scaling up (incl how to use the Stanford tokenizer)_
    11. Summary
    12. Further Reading
    13. Exercises
4. **Writing Structured Programs** _updates for Python 3 including new view types, integer division_
    1. Back to the Basics
    2. Sequences
    3. Questions of Style
    4. Functions: The Foundation of Structured Programming
    5. Doing More with Functions
    6. Program Development
    7. Algorithm Design
    8. A Sample of Python Libraries
    9. Summary
    10. Further Reading
    11. Exercises
5. **Categorizing and Tagging Words**
    1. Using a Tagger
    2. Tagged Corpora _mention MASC tagged corpus_
    3. Mapping Words to Properties Using Python Dictionaries
    4. Automatic Tagging
    5. N-Gram Tagging
    6. Transformation-Based Tagging
    7. How to Determine the Category of a Word
    8. _Scaling Up (incl how to use the Stanford tagger)_
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
    8. _Sentiment Detection (incl sentiwordnet); here or in chapter 7_
    9. _Clustering and similarity; distributed representations of lexical meaning_
    8. Summary
    9. Further Reading
    10. Exercises
7. **Extracting Information from Text**
    1. Information Extraction
    2. Chunking
    3. Developing and Evaluating Chunkers
    4. Recursion in Linguistic Structure
    5. Named Entity Recognition
    6. Relation Extraction
    7. _Scaling Up (incl how to use the Stanford chunker and named entity recognizer)_
    8. Summary
    9. Further Reading
    10. Exercises
8. **Analyzing Sentence Structure**
    1. Some Grammatical Dilemmas
    2. What's the Use of Syntax?
    3. Context Free Grammar
    4. Parsing With Context Free Grammar
    5. Dependencies and Dependency Grammar
        * _split into two sections:_
        * _(a) heads, arguments, and roles (mentions FrameNet, VerbNet, NomBank, PropBank)_
        * _(b) dependency grammar and dependency parsing_
    6. Grammar Development
    7. _Scaling Up (incl how to use the Stanford parser)_
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
    6. _Learning to build logical representations_
    6. Summary
    7. Further Reading
    8. Exercises
11. **Managing Linguistic Data**
    1. Corpus Structure: a Case Study
    2. The Life-Cycle of a Corpus
    3. Acquiring Data
    4. Working with XML
    5. Working with Toolbox Data
    6. Describing Language Resources using OLAC Metadata
    7. Summary
    8. Further Reading
    9. Exercises
12. _**Machine Translation**_
    1. _Sentence Alignment (incl Gale-Church algorithm)_
    2. _Word Alignment (IBM model 1; mention existence of other models)_
    3. _Aligned Corpora_
    4. _Decoding_
    5. _Evaluation_
    6. _Phrase-Based Models_
    7. _Summary_
    7. _Further Reading_
    8. _Exercises_
