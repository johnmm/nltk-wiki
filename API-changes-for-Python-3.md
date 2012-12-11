## Proposed Changes for Consideration

* make Tree(s) synonymous with Tree(s,[]) and use Tree.parse(s) directly?
  * this would simplify the code in tree.py a lot! I'm all for, --Peter Ljunglöf
* The same argument could be made for nltk.align.Alignment, --Peter Ljunglöf
  * `__new__` is used to be able to give a Giza string instead of a list of pairs. 
  * Suggestion: add classmethod `Alignment.fromGiza` and let the constructor only
    allow a list of pairs.
* remove/deprecate nltk.misc.babelfish?