## TDD
Test-Driven Development

 with TDD we need to think about tests first. And to be ok with the possibility of the beginning to be hard sometimes

 ### AAA: Arrange, Act and Assert.
1-**Arrange:** you need to organize the data needed to execute that piece of code (input)

2-**Act:** here you will execute the code being tested (exercise the behaviour)

3-**Assert:** after executing the code, you will check if the result (output) is the same as you were expecting.

**The test file name should follow the same name of module name.**

 important thing about TDD: **the cycle.**

 The cycle is made by three steps:

🆘 Write a unit test and make it fail 

✅ Write the feature and make the test pass! 

🔵 Refactor the code — the first version doesn’t need to be the beautiful one .


## TDD is not about the money/tests
More than any checking, we need to think about our software design first.

## summary:
+ The greatest advantage about TDD is to craft the software design first

+ Your code will be more reliable: after a change you can run your tests and be in peace

+ Beginning may be hard — and that’s fine. You just need to practice!


## if __name__ == “__main__”

**Python interpreter reads source file and define few special variables/global variables.**

If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”. If this file is being imported from another module(module is a file containing Python definitions and statements), __name__ will be set to the module’s name. 


+ Every Python module has it’s __name__ defined and if this is` ‘__main__’`, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.

+ If you import this script as a module in another script, the` __name__` is set to the name of the script/module.

+ Python files can act as either reusable modules, or as standalone programs.

+ `if __name__ == “main”`: is used to execute some code only if the file was run directly, and not imported.

## Recursion
unction calls itself directly or indirectly 

![](https://media.geeksforgeeks.org/wp-content/uploads/20191107235734/fib1.jpg)

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/recursion.jpg)

Recursion is the process of defining a problem (or the solution to a problem) in terms of (a simpler version of) itself.

example uses of recursion:
**factorial**


recursion is good for the program in term of memroy usage 
