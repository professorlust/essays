Global Replacement
===

## Basic syntax
``:s/old/new`` changes the **first** occurrence of the pattern __old__ to __new__ on the current line.

``:s/old/new/g`` change **every** occurrence of __old__ to __new__ on the current line.

``:1,$s/old/new/g`` change every occurrence of __old__ to __new__ within the entire file.

``:%s/old/new/g`` % represents 1,$.

``.,+5s/old/new/g`` represents from the current line to the next five.

## Confirming Substitutions
use ``/``, ``n`` and ``.`` is more useful when you not intent to replacement globally.

## Context-Sensitive Replacement
``:g/pattern/s/old/new/g`` This syntax lets you search for a pattern, and then, once you find the line with the pattern, make a substitution on a string different from the pattern.

--
2015-09-26