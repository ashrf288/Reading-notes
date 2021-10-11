## Reading and Writing Files in Python

**file** is a contiguous set of bytes used to store data. This data is organized in a specific format .

**Files on most modern file systems are composed of three main parts:**

**Header**: metadata about the contents of the file (file name, size, type, and so on)

**Data**: contents of the file as written by the creator or editor

**End of file (EOF):** special character that indicates the end of the file


## File Paths

**Folder Path**: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

**File Name:** the actual name of the file
Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

**The double-dot (..) can be chained together to traverse multiple directories above the current directory.**

**ASA standard states that line endings should use the sequence of the Carriage Return (CR or \r) and the Line Feed (LF or \n) characters (CR+LF or \r\n).**


```
Pug\r\n
Jack Russell Terrier\r\n
English Springer Spaniel\r\n
German Shepherd\r\n
Staffordshire Bull Terrier\r\n
Cavalier King Charles Spaniel\r\n
Golden Retriever\r\n
West Highland White Terrier\r\n
Boxer\r\n
Border Terrier\r\n
```


## Opening and Closing a File in Python
`file = open('dog_breeds.txt')`

you should always make sure that an open file is properly closed.

 **The first way to close a file is to use the try-finally block:**
 ```
 reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()

```
## File Handling

```
"r" - Read 
"x" - Create 

"a" - Append 

"w" - Write 

"x" - Create 
"t" - Text - Default value. Text mode

"b" - Binary - Binary mode 
```

**eturn one line by using the readline()**
looping through the lines of the file, you can read the whole file, line by line


**To delete a file, you must import the OS module, and run its os.remove()**

### example to appending to a file:

```
with open('dog_breeds.txt', 'a') as a_writer:
    a_writer.write('\nBeagle')

  ```



## Exceptions versus Syntax Errors


(`Syntax errors` occur when the parser detects an incorrect statement. )

### Raising an Exception
**raise allows you to throw an exception at any time.**
while **enables you to verify if a certain condition is met and throw an exception if it isn’t.**
We can use raise to throw an exception if a condition occurs

**The AssertionError Exception
Instead of waiting for a program to crash midway, you can also start by making an assertion in Python **


### The try and except Block: Handling Exceptions

Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions

![aa](https://files.realpython.com/media/try_except.c94eabed2c59.png)

### The else Clause

instruct a program to execute a certain block of code only in the absence of exceptions.

![](https://files.realpython.com/media/try_except_else.703aaeeb63d3.png)



### Cleaning Up After Using finally

lean up after executing your code

![](https://files.realpython.com/media/try_except_else_finally.a7fac6c36c55.png)



