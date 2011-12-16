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

Parentheses
-----------
* Use optional parentheses:
  * To clarify or force order of operations.
  * Around arguments in method definitions. (This is most common, but not universal, in the Ruby community.)
  * In most calls to instance methods that take arguments.
* Omit optional parentheses:
  * In almost every call that takes no arguments. (This makes it look and feel like an attribute instead of a method call.)
  * In most calls to class methods when called within the class definition, because they feel more like commands than method calls.
  * When using most DSLs.
  * In RSpec ``should`` calls. Note that you'll need to include the parentheses for any methods after the ``should`` that take arguments.
* Parentheses are required:
  * Surrounding range literals, when calling a method on the range. Example: ``(1..10).select{|n| n.even?}
* Parentheses for a method call go directly after the method name, with no space between.
  * This is actually a Ruby syntax requirement.
