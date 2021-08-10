# functional programming


## What is functional programming?
 a way of thinking about software construction by creating pure functions

 ## What is a pure function and how do we know if something is a pure function?

 does not use any external data to obtain the return value

 ## What are the benefits of a pure function?

 1- easier to reason about

 2-easier to combine

 3-easier to test

4- easier to debug

 5-easier to parallelize

 ## What is immutability?

  unable to change (If we need, we create a new one, but we do not modify the existing object's state.)

  ## What is Referential transparency?

   can be replaced with its value and the resulting behavior is the same as before the change.


   # NODE JS : 


   ## What is a module?
   (another javaScript file)
blocks of encapsulated code that communicates with an external application on the basis of their related functionality. 

## What does the word ‘require’ do?

builtin require function is the easiest way to include modules that exist in separate files. 

## How do we bring another module into the file the we are working in? 
using require

## What do we have to do to make a module available?
require it and then use  exports to speccifiy which spicif things we want to make avialble to the other moudle

```
module.exports = 
```
