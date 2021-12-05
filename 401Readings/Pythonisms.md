##  Dunder (Magic, Special) Methods

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.


These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

## Special Methods and the Python Data Model

This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

You can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If you want to write more Pythonic code, knowing how and when to use dunder methods is an important step.

+ Object Initialization: __init__
+ Object Representation: __str__, __repr__
+ Iteration: __len__, __getitem__, __reversed__
+ Operator Overloading for Comparing Accounts: __eq__, __lt__
+ Operator Overloading for Merging Accounts: __add__
+ Callable Python Objects: __call__
+ Context Manager Support and the With Statement: __enter__, __exit__


## Python Iterators


A Simpler Iterator Class
Up until now our iterator example consisted of two separate classes, Repeater and RepeaterIterator. They corresponded directly to the two phases used by Python’s iterator protocol:

First setting up and retrieving the iterator object with an iter() call, and then repeatedly fetching values from it via next().

Many times both of these responsibilities can be shouldered by a single class. Doing this allows you to reduce the amount of code necessary to write a class-based iterator.

Python 2.x Compatible Iterators
All the code examples I showed here were written in Python 3. There’s a small but important difference between Python 2 and 3 when it comes to implementing class-based iterators:

In Python 3, the method that retrieves the next value from an iterator is called __next__.
In Python 2, the same method is called next (no underscores).
This naming difference can lead to some trouble if you’re trying to write class-based iterators that should work on both versions of Python. Luckily there’s a simple approach you can take to work around this difference.

## What Are Python Generators

Generators are a tricky subject in Python. With this tutorial you’ll make the leap from class-based iterators to using generator functions and the “yield” statement in no time.

And that’s quite a fitting mental model for what happens here. You see, when a return statement is invoked inside a function, it permanently passes control back to the caller of the function. When a yield is invoked, it also passes control back to the caller of the function—but it only does so temporarily.

Whereas a return statement disposes of a function’s local state, a yield statement suspends the function and retains its local state.

In practical terms, this means local variables and the execution state of the generator function are only stashed away temporarily and not thrown out completely.

Python Generators That Stop Generating
In this tutorial we started out by writing an infinite generator once again. By now you’re probably wondering how to write a generator that stops producing values after a while, instead of going on and on forever.

Remember, in our class-based iterator we were able to signal the end of iteration by manually raising a StopIteration exception. Because generators are fully compatible with class-based iterators, that’s still what happens behind the scenes.

Thankfully, as programmers we get to work with a nicer interface this time around. Generators stop generating values as soon as control flow returns from the generator function by any means other than a yield statement. This means you no longer have to worry about raising StopIteration at all!


**Python Generators – A Quick Summary**
Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.


#  Ethics and Professional Conduct



## resources 
+  [dunder methods](https://dbader.org/blog/python-dunder-methods)
+ [iterators](https://dbader.org/blog/python-iterators)

+ [generators](https://dbader.org/blog/python-generators)

