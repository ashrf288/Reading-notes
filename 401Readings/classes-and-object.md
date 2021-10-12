# Classes and Objects
**Objects** are an encapsulation of variables and functions into a single entity. 

**Objects** get their variables and functions from classes.

**Classes** are essentially a template to create your objects.


```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()

print(myobjectx.variable)
```

## Accessing Object Functions

To access a function inside of an object you use notation similar to accessing a variable

# Thinking Recursively in Python


## The algorithm for iterative present delivery

1-lgorithm with which he can divide the work of delivering presents among his elves:

2- Appoint an elf and give all the work to him
Assign titles and responsibilities to the elves based on the number of houses for which they are responsible:

> 1 He is a manager and can appoint two elves and divide his work among them

> 1 He is a worker and has to deliver the presents to the house assigned to him

![image](https://files.realpython.com/media/elves_7.8d1af1cd85c8.png)



## Recursive Functions in Python

 A recursive function is a function defined in terms of itself via self-referential expressions.
 (function will continue to call itself and repeat its behavior until some condition is met to return a result)

 ![](https://files.realpython.com/media/stack.9c4ba62929cf.gif)

 each recursive call has its own execution context, so to maintain state during recursion you have to either:

+ Thread the state through each recursive call so that the current state is part of the current call’s execution context

+ Keep the state in global scope


**A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. **

The recursive function’s structure can often be modeled after the definition of the recursive data structure it takes as an input. 


python’s mutable data structures don’t support structural sharing
treating them like immutable data structures is going to negatively affect your space and GC (garbage collection) 

## Python Testing with pytest: Fixtures and Coverage

### Fixtures
test suite", with each test aiming to check a different path through your code.
fine fixtures using a combination of the pytest.
fixture decorator, along with a function definition.


fixture that'll provide your test with the appropriate object at the right time.

```
@pytest.fixture
def simple_file():
   return StringIO('\n'.join(['abc', 'def', 'ghi', 'jkl']))
```

fxture might act like data, in that you don't invoke it with parentheses. But it's actually a function under the hood, which means it executes **every time you invoke a test using that fixture.** This means that the fixture, in contrast with regular-old data, can make calculations and decisions.


### fixture's "scope"
 If your fixture uses "yield" instead of "return", pytest understands that the post-yield code is for tearing down objects and connections. And yes, if your fixture has "module" scope, pytest will wait until all of the functions in the scope have finished executing before tearing it down.

## Coverage

how thoroughly you have tested your code,ested all of the possible paths through those functions

### how can you include code coverage with pytest?

1-you can invoke pytest with the --cov option. If you don't say anything more than that, you'll get a coverage report for every part of the Python library that your program used.

2-  turn the coverage report into something human-readable

`
pytest --cov=mymul .`


