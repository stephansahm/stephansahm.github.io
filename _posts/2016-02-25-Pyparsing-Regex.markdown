---
layout: default
github: https://github.com/schlichtanders/pyparsing_regex
readthedocs: http://pyparsing-regex.readthedocs.io/en/latest/pyparsing_regex.html
keywords: pyparsing, regular expressions
description: "Implementation of pyparsing's interfaces, however running on regular expressions."
---

pyparsing_regex is a reimplementation of the pyparsing interface, building upon regular expressions.

It is intended to be a replacement for pyparsing where no recursion is needed, in order to speed up parsing
significantly (factor 100).

##### Additions to Pyparsing
In addition to pyparsing, pyparsing_regex has a ``GroupLiftKeys`` class which works like ``Group``, only that all string-keys
are also available at the upper level (encompassing everything which belongs to that key further down). In a normal
``Group``, the nested keys would be hidden from the upper layer, which might be unwanted.

Further a standard, efficient ``Repeat`` class is supported, which repeats an element an arbitrary number of times. It is the interface to a regex like ``(group-content){min, max}``


##### Further References
See also <http://pyparsing.wikispaces.com/>

For a version of pyparsing using OrderedDict instead of dict (here and there useful to have) see <https://github.com/schlichtanders/pyparsing-2.0.3-OrderedDict>
