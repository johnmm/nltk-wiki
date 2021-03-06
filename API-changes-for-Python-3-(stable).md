Please see [[Porting your code to NLTK 3.0]].

## Proposed Changes for Consideration

* methods that return sequences should produce iterators by default; there would be no special iter methods
  * should we remove the `..._iter` methods completely, or just deprecate them?
* make Tree(s) synonymous with Tree(s,[]) and use Tree.parse(s) directly
  * this would simplify the code in tree.py a lot! I'm all for, --Peter Ljunglöf
  * but the name `parse` is unfortunate -- it reminds too much of all the NLTK parsers -- how about `fromstring`? (used in the libraries array, xml.etree, lxml, numpy, ...)
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
  * we should go ahead and remove it, yeah. https://github.com/nltk/nltk/issues/265 --Alex Rudnick
* perhaps this could be used to simplify sem/logic.py?
  * http://sigusr2.net/2008/Sep/30/python-type-constructors-like-ocaml.html
* `ConditionalFreqDist.conditions()` currently returns a *sorted* list, which is inefficient:
  * Suggestion: Just let it return `.keys()` without sorting.
* we may need to wrap word_tokenize() in sent_tokenize(), since some users (and the book?) apply word_tokenize to un-sentence-segmented text
* `Tree` should *not* be a subclass of `list` --Peter Ljunglöf
  * Almost all list-operations are anyway unsupported on trees. E.g., `+` or `*` are not supported, but `+=` is.