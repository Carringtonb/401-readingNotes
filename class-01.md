## Try/Catch Blocks

* Try/Catch blocks are used to handle exceptions in C#. The compiler will first try to execute the code in the try statement and if there is an exception it will move on to the catch code blocks.

* A Try block must be followed by a Catch block, a Finally block, or both.

* Checking for preventable errors is preferable to relying on try/catch blocks because exceptions are relatively expensive to handle, taking hundreds of clock cycles or more.

* You can specify an exception filter by adding a when clause to your catch block.

* A finally block always executes—whether or not an exception is thrown and whether or not the try block runs to completion. finally blocks are typically used for cleanup code.

* An infinite loop can defeat a finally block, as well as the process ending abruplty.

* Throw expressions can appear in ternary conditional expressions.

* Therac-25 was a machine that administered radiation between 1985-1987. The over confidence of the designing engineers and the lack of due-dilligence caused the machine to have several errors in its base code that resulted in some patients being administered radiation at levels that were hundreds of times higher than expected, causing injury and even death.

* The first flight of the Ariane 5 rocket failed because a data-conversion created a foating point value that was too large to be represented by a 16-bit signed integer. Three of the variables were not protected with a handler.