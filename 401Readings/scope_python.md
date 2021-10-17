## scope

how variables and names are looked up in your code. It determines the visibility of a variable within the code.

The Python scope concept is generally presented using a rule known as the **LEGB** rule.

**LEGB: Local, Enclosing, Global, and Built-in**

## 1-What scopes are and how they work in Python

 Python is a **dynamically-typed** language (variables in Python come into existence when you first assign them a value. On the other hand, functions and classes are available after you define them using def or class,)

**Global scope**: The names that you define in this scope are available to all your code.

**Local scope:** The names that you define in this scope are only available or visible to the code within the scope.


language that implements scope, there’s no way for you to access all the variables in a program at all locations in that program. In this case, your ability to access a given name will depend on where you’ve defined that name. like `python`


## 2-Why it’s important to know about Python scope

**where you assign or define a name in your code determines the scope or visibility of that name.**

** namespaces. These are the concrete mechanisms that Python uses to store names**

**Names at the top level of a module are stored in the module’s namespace.  `__dict__`**
```
>>> sys.ps1
'>>> '
>>> sys.__dict__['ps1']
'>>> '
```

## 3-What the LEGB rule is and how Python uses it to resolve names

+ **Local** (or function) scope :

This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. 
+ **nonlocal** names can be accessed from inside nested functions, but they can’t be modified or updated from there.


+ **Enclosing**(or nonlocal) scope
special scope that only exists for nested functions

+ **Global** (or module) scope Names in this Python scope are visible from everywhere in your code.
+  **Built-in scope **  Names in this Python scope are also available from everywhere in your code. 
**This scope contains names such as keywords, functions, exceptions,**


## 4-How to modify the standard behavior of Python scope using global and nonlocal

 Python provides two keywords that allow you to modify the content of global and nonlocal names. These two keywords are:

+ global    
 `global counter  # Declare counter as global`
+ nonlocal
The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas
 ```
def nested(
     nonlocal var  # Declare var as nonlocal
    var += 100
 ```

**a closure is an inner or nested function that carries information about its enclosing scope, even though this scope has completed its execution**

**Closures provide a way to retain state information between function calls**

**functools provides a function named partial() that makes use of the closure technique to create new function objects that can be called using predefined arguments.**

```
 from functools import partial
>>> def power(exp, base):
...     return base ** exp
...
>>> square = partial(power, 2)
>>> square(10)
```

**Bringing Names to Scope With import**

import the modules or the names explicitly to your `__main__` module


**Discovering Unusual Python Scopes**
**Comprehension Variables Scope:**

 A comprehension is a compact way to process all or part of the elements in a collection or sequence. You can use comprehensions to create lists, dictionaries, and sets.

 Comprehensions consist of a pair of brackets ([]) or curly braces ({}) containing an expression, followed by one or more for clauses and then zero or one if clause per for clause.


 **Exception Variables Scope**

 The exception variable is a variable that holds a reference to the exception raised by a try statement. In Python 3.x, such variables are local to the except block and are forgotten when the block ends. 


 **Class and Instance Attributes Scope**


## 5-What scope-related tools Python offers and how you can use them

+ globals()
In Python, globals() is a built-in function that returns a reference to the current global scope or namespace dictionary.

+ locals() This function updates and returns a dictionary that holds a copy of the current state of the local Python scope or namespace. 

+ vars() vars() is a Python built-in function that returns the .__dict__ attribute of a module, class, instance, 


+ dir() You can use dir() without arguments to get the list of names in the current Python scope. If you call dir() with an argument
 
