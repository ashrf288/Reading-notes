# Functions :
 To use a function, you must define it somewhere in the scope from which you wish to call it.

 A **function definition** (also called a **function declaration**, or function statement) consists of the `function` keyword, followed by:

+ The name of the function.

+ A list of parameters to the function, enclosed in parentheses and separated by commas.

+ The JavaScript statements that define the function, enclosed in curly brackets,` {...}.`
+  The statement `return` specifies the value returned by the function.

## Function expression:
 The `function` keyword can be used to define a function inside an expression or it could be **anonymous** it does not have to have a name.
 ## Calling functions:
 Defining a function does **not execute it**. Defining it names the function and specifies what to do when the function is called.

 ## Function scope:
 Variables defined inside a function **cannot** be accessed from anywhere outside the function, because the variable is **defined only in the scope of the function.** However, a function **can access all** variables and functions defined inside the scope in which it is defined.

 ## Function parameters:
 In JavaScript, parameters of functions default to undefined. However, in some situations it might be useful to set a different default value.
## default parameters:
 With default parameters, a manual check in the function body is no longer necessary.

** example**  You can put 1 as the default value for b in the function head:
`function multiply(a, b = 1) {`

 ` return a * b;`
 
`}`

`multiply(5); // 5`

