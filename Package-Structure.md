Note that this page is stale; links need to be updated, instructions about import * need to be updated.

Most NLTK code is structured into packages, which have the following structure:

  1. all modules
    * opening comment with package name, copyright, license, authors
  2. `__init__.py`
    * package-level docstring
    * import statements that import module names (but not `api` or `util`) into the package namespace: `from module import *` (for all modules in the package)
    * define `__all__`
    * mappings from deprecated functions to current functions, with deprecation decorators
    * example: http://code.google.com/p/nltk/source/browse/trunk/nltk/nltk/chunk/__init__.py
  3. `api.py`
    * define any interface classes that are used in other modules
    * this should be imported into other modules
    * (this filename is misleading as it is not an external API)
    * example: http://code.google.com/p/nltk/source/browse/trunk/nltk/nltk/chunk/api.py
  4. `util.py`
    * common utilities shared by modules in this package
    * example: http://code.google.com/p/nltk/source/browse/trunk/nltk/nltk/chunk/util.py
  5. `module.py` (where "module" is the name of a module)
    * imports in three blocks: standard library and third party imports, nltk imports, package-local imports
    * imports from this package are local imports, of the form `from other_module import name` (and not `from nltk.package.other_module import name`; to facilitate moving, splitting and merging of packages)
    * imports from other nltk packages are fully qualified, e.g. `from nltk import tokenize`
