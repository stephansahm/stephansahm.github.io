---
layout: default
github: https://github.com/schlichtanders/pyparsing_regex
readthedocs: http://pyparsing-regex.readthedocs.io/en/latest/
category: pyparsing, regular expressions
description: "Implementation of pyparsing's interfaces, however running on regular expressions."
---


pyparsing_regex is a reimplementation of the pyparsing interface, building upon regular expressions.

It is intended to be a replacement for pyparsing where no recursion is needed, in order to speed up parsing
significantly (factor 100). The outputs are roughly similar


The index-interface of the parse result is analog to the of pyparsing, i.e. with string-keys "example-key" you can access
all entries where ``setResultName("example-key")`` was called.
Alternatively you can access elements with integer-key, in a list like way.
Important to know, the ``Group`` class creates a nesting within this listing interface.

In addition to pyparsing, pyparsing_regex has a ``GroupLiftKeys`` class which works like ``Group``, only that all keys
are also available at the upper level (encompassing everything which belongs to that key further down). In a normal
``Group``, the nested keys would be hided from the upper layer, which might not be what is wanted.

The returned object is a ``schlichtanders.myobjects.Structure`` which is a general powerful datastructure imitating
pyparsings ParseResult in a general way.

For further documentation, see also  http://pyparsing.wikispaces.com/
For a version of pyparsing using OrderedDict instead of dict (here and there useful to have) see https://github.com/schlichtanders/pyparsing-2.0.3-OrderedDict
