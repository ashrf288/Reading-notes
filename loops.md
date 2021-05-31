# Operators :
+ ## Assignment operators :
An assignment operator assigns a value to its left operand based on the value of its right operand :
example ` x = y`;
+ ## Comparison operators:
A comparison operator compares its operands and returns a logical value based on whether the comparison is true. example `var2 > var1`

+ ## Arithmetic operators:
An arithmetic operator takes numerical values as their operands and returns a single numerical value .example : `1 / 2;`

+ ## Bitwise operators :
A bitwise operator treats their operands as a set of 32 bits (zeros and ones). example:
`a & b`
+ ## Logical operators :
Logical operators are typically used with Boolean (logical) values .
example : `expr1 && expr2`

+ ## String operators :
example : `var mystring = 'alpha';`

+ ## Comma operator :
evaluates both of its operands and returns the value of the last operand .
 + ## Unary operators:
 delete
The delete operator deletes an object's property. The syntax is:
` delete object.property;`
 + ## Relational operators:
 in
The in operator returns true if the specified property is in the specified object.


#  Loops and iteration:
Loops offer a quick and easy way to do something repeatedly. This chapter of the JavaScript Guide introduces the different iteration statements available to JavaScript.

## 1- for statement:
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.

`for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement`
## 2- do...while statement:
The do...while statement repeats until a specified condition evaluates to false.

 `do`

 ` statement`

`while (condition);`

## 3- while statement
A while statement executes its statements as long as a specified condition evaluates to true. 

`while (condition)`

  `statement`

  ## 4-break statement
Use the break statement to terminate a loop, switch, or in conjunction with a labeled statement.

`break;`

`break [label];`

## 5-  for...in statement
The for...in statement iterates a specified variable over all the enumerable properties of an object.

`for (variable in object)`

 ` statement`
