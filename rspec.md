RSpec
=====

Expect vs. Should
-----------------
* Use the ``expect(subject).to eq(expected_value)`` syntax instead of ``subject.should == expected_value``.
  * Uses less metaprogramming "magic".
  * Available as of RSpec 2.11. 
  * The ``should`` syntax may be deprecated soon.
  * Prevents us from trying to use ``subject.should != expected_value``, which does not work.
  * The syntax for checking that exceptions are raised is also clearer:
    * ``expect { subject_code }.to raise_error``
  * Does not have problems with proxying and delegation that ``should`` has.
  * Can disable the ``should`` syntax:
    * ``RSpec.configure {|config| config.expect_with(:rspec) {|c| c.syntax = :expect }}
  * See http://myronmars.to/n/dev-blog/2012/06/rspecs-new-expectation-syntax for full details.

Matchers
--------
* For comparison matchers, use ``be``:
  * ``expect(foo).to be < 12``
  * ``foo.should be < 12``
