Statistical machine translation (SMT) is a rapidly growing area within Computational Linguistics. NLTK should provide a pathway for students who want to learn about the basic algorithms. [View NLTK activity on SMT.](https://github.com/nltk/nltk/issues?labels=SMT)

## Existing functionality

Existing functionality is mostly in the [align package](https://github.com/nltk/nltk/tree/develop/nltk/translate). It includes:

* IBM Models 1-3 `translate/ibm{1,2,3}.py`
* MT evaluation metrics
 * BLEU `translate/bleu_score.py`
 * RIBES `translate/ribes_score.py`
 * ChrF `translate/chrf_score.py`
 * GLEU `translate/gleu_score.py`
* Gale-Church Sentence Aligner `translate/gale_church.py`
* Aligned sentence reader `corpus/reader/aligned.py`
* Grow-Diagonal-Final-And Phrase Extraction `translate/phrase_based.py`

## Planned functionality

We would like to add functionality in the following areas:

* Decoder for word-based models
* Phrase-based models
 * Phrase probability estimation
* Decoder for phrase-based models
* [Visualization of word alignments](https://github.com/nltk/nltk/issues/684)

## Third-party implementations

Existing Python implementations that could possibly be incorporated into NLTK

* [KenLM](https://github.com/kpu/kenlm/tree/master/python)
* [Kriya](https://github.com/sfu-natlang/Kriya)

## Useful links

* http://www.statmt.org/
* https://github.com/jonsafari/nmt-list