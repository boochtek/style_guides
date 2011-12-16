Ruby
====

Indentation
-----------
* Follow standard Ruby style guide of 2 spaces to indent.
* Outdent ``private`` and ``protected`` keywords.
  * Similar to how ``rescue`` clause in a method (without a ``begin`` block) is outdented.

Quoting
-------
* Prefer single quotes (``'``) to double quotes (``"``).
  * Single quotes are easier to type.
  * Single quotes ensure that special characters don't have any unwanted effects.
  * Use double quotes if you need interpolation or escape characters (like ``"\n"``).
  * Distinction carries over to UNIX shell and most other scripting languages.
* Prefer ``%(interpolated string)`` to other options, like ``%[]`` and ``%{}``.
  * Just generally looks cleaner than the other options.
  * Seems to be the most common choice for most Ruby programmers.
* Prefer ``%w[word1 another_word]`` to other options.
  * The ``[]`` reminds us that it's an array.
