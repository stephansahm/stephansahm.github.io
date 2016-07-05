---
layout: default
github: https://github.com/schlichtanders/pyparsing_regex
readthedocs: http://pyparsing-regex.readthedocs.io/en/latest/
keywords: pyparsing, regular expressions
description: "Implementation of pyparsing's interfaces, however running on regular expressions."
---

pyparsing_regex is a reimplementation of the pyparsing interface, building upon regular expressions.

It is intended to be a replacement for pyparsing where no recursion is needed, in order to speed up parsing
significantly (factor 100). The outputs are roughly similar


##### How To Use It
Like in pyparsing you build up a parser by combining simpler building blocks (parsers themselves)
using pythons operators which got overloaded within the specific pyparsing classes.

Once you have your parser, you can parse any string or file according to the specified grammar.

The parse result you get then is analog to the of pyparsing, i.e. with string-keys like ``parserresult["example-key"]`` you can access
all entries where ``setResultName("example-key")`` was called.
Alternatively you can access elements with an integer-key in a list like way.
Important to know, the ``Group`` class creates a nesting within this listing interface.

The returned object is of type ``schlichtanders.myobjects.Structure`` which is a powerful datastructure imitating
pyparsings ParseResult in a generic way.


##### Additions to Pyparsing
In addition to pyparsing, pyparsing_regex has a ``GroupLiftKeys`` class which works like ``Group``, only that all keys
are also available at the upper level (encompassing everything which belongs to that key further down). In a normal
``Group``, the nested keys would be hided from the upper layer, which might not be what is wanted.

Further a standard ``Repeat`` class is supported, which repeats an element in arbitrary number of times. It
is the interface to a regex like ``(group-content){min, max}``


##### Further References
See also  http://pyparsing.wikispaces.com/
For a version of pyparsing using OrderedDict instead of dict (here and there useful to have) see https://github.com/schlichtanders/pyparsing-2.0.3-OrderedDict
