# error handling :

1- ORDER OF EXECUTION (how scripts are processed.)


2-**EXECUTION CONTEXTS:** (global scope)
Every statement in a script lives in one of three
execution contexts:

+ ** GLOBAL CONTEXT** (function scope)
Code that is in the script, but not in a function.


 + **FUNCTION CONTEXT**


+ **EVAL CONTEXT (NOT SHOWN)**
Text is executed like code in an internal function


**Each time a script enters a new execution context, there are two phases of activity:**

1- PREPARE (scope is created Variables, functions, and arguments are created)

2-EXECUTE (assign values to variables,  Reference functions and run their code)

**hoisting:** Call functions before they have been declared ,Assign a value to avariable that has not yet been declared
( the function and first statement are in the same execution context.)




**If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code.**

 ### Whenever the interpreter comes across an error, it will look for error-handling code So it is going through the stack looking for errorhandling code until it gets to the global context. If there is still no error handler, the script stops running and the Error object is created.

 **Error objects** can help you find where your mistakes are.

 When there is an error, you can see all of this information in the JavaScript console



 errors syntax :

 1-Syntax Error(SYNTAX IS NOT CORRECT)

 2-EvalError INCORRECT USE OF eval() FUNCTION **rare**

 3-Referrence erenceError VARIABLE DOES NOT EXIST

 4-URI Error INCORRECT USE OF URI FUNCTIONS

 5-Type Error VALUE IS UNEXPECTED DATA TYPE

 6- RangeError NUMBER OUTSIDE OF RANGE

 7-NAN not a NUMBER


 ## HOW TO DEAL WITH ERRORS :

 1: DEBUG THE SCRIPT TO FIX ERRORS

 2- HANDLE ERRORS GRACEFULLY :
 using `try`, `catch`, `throw`, and `finally` statements

 **Try to narrow down where the problem might be, then look for clues**

 + ` TRY` you specify the code that you think might throw an
exception within the try block
+  `CATCH` If the try code block throws an exception, catch steps in with an alternative set of code.

+ `FINALLY` The contents of the finally code block will run either
way - whether the try block succeeded or failed.


```
try {
// II Try to execute this code
catch (exception) {
// II If there is an exception, run this code
finally {
// this This always gets executed
}
```


 **+ Look at the error message, it tells you:**

• The relevant script that caused the problem.

• The line number where it became a problem for the interpreter
+ The type of error

3- TYPING IN THE CONSOLE 
type the error in the console and see what is the results


## THROWING ERRORS :
this is used when you know your code will cause errors

`throw new Error( 1message 1) ;`


## DEBUGGING TIPS :
1- Some problems are browser specific. (change the browser)

2- SEARCH (Stack Overflow)

3-ADD NUMBERS

4-STRIP IT BACK

Remove parts of code, and strip it down to the minimum you
need

5- VALIDATION TOOLS 

6- EXPLAINING THE CODE



## COMMON ERRORS :

1-JavaScript is case sensitive so check your capitalization.

2-MISSED/ EXTRA CHARACTERS

3- DATA TYPE ISSUES
