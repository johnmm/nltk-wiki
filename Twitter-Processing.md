## Functionality currently implemented (in `develop` branch)

* Twitter client for both Streaming and REST API
* Extraction of Tweet fields into CSV format
* Twitter corpus reader 
* 'Casual' tokenizer with some normalisation
* First 20k sample of Tweets in data download
* Basic HOWTO (IPython notebook)

## To do

* Better Token Normaliser (e.g., see https://noisy-text.github.io/norm-shared-task.html)
* Tweet POS tagger (baseline would be to annotate corpus using existing Twitter-specific POS tagger and train from that)
* Named Entity Recognition (e.g., see https://noisy-text.github.io/ner-shared-task.html) and grounding / disambiguation
* Relation and event detection
* Detecting irony and sarcasm
* Clustering 