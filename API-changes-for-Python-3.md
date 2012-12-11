## Proposed Changes for Consideration

* methods that return sequences should produce iterators by default; there would be no special iter methods
* make Tree(s) synonymous with Tree(s,[]) and use Tree.parse(s) directly
  * this would simplify the code in tree.py a lot! I'm all for, --Peter Ljunglöf
* The same argument could be made for nltk.align.Alignment, --Peter Ljunglöf
  * `__new__` is used to be able to give a Giza string instead of a list of pairs. 
  * Suggestion: add classmethod `Alignment.fromGiza` and let the constructor only
    allow a list of pairs.
* not use `__new__` in Abstract Base Classes, for propagating the constructor to subclasses --Peter Ljunglöf
  * example: `FeatStruct(x)` returns a FeatDict or a FeatList, depending on `x`. 
    This means that `type(T(x)) != T` for some classes T, which is unintuitive (and un-object-oriented).
  * Suggestion: the same as above -- use `FeatStruct.parse(s)` or something like that
  * This also holds for nltk.sourcedstring.SourcedString, I think
  * I'm not sure if it will work for nltk.util.AbstractLazySequence
* remove/deprecate nltk.misc.babelfish?
* perhaps this could be used to simplify sem/logic.py?
  * http://sigusr2.net/2008/Sep/30/python-type-constructors-like-ocaml.html
