## Unit Testing and Documentation

* Unit tests don’t deal with their environment and with external systems to the codebase.

* If you have a console application and you pipe input to it from the command line and test for output, you’re executing an end-to-end system test — not a unit test.

* In C#, a  unit test will test something specific about a method in isolation.

* There are frameworks that have been created to make unit testing easier, faster, and cleaner.

* The first thing you should do is arrange everything that you need to run the test.
* Once everything is arranged, invoke the add method and capture the result.
* The assert is then invoked, which represents a general category of action that you cannon omit and have a unit test. There should only be one assert per test method.

* Each test should handle its own set up and tear down. The test runner will execute the tests in whatever order it feels like, and can change that order.
