# List Comprehensions in Python

Python provides a more concise method for handling lists and list comprehension. 

**List comprehension** is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.


## Syntax
`my_new_list = [ expression for item in list ]`
+ First is the expression we’d like to carry out. expression inside the square brackets.

+ Second is the object that the expression will work on. item inside the square brackets.

+ Finally, we need an iterable list of objects to build our new list from. list inside the square brackets.

## Notes about Lists Comprehensions
+ List comprehension methods are an elegant way to create and manage lists. 
+ In Python, list comprehensions are a more compact way of creating lists. 
+ More flexible than for loops, list comprehension is usually faster than other methods.

## Create a List with range()

```
digits = [x for x in range(10)
print(digits)
```
Output
`[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`

## Create a List Using Loops and List Comprehension in Python


##  Create a List Using Loops and List Comprehension in Python
```
squares = [x**2 for x in range(10)]
print(squares)
```

Output

`[0, 3, 6, 9, 12, 15, 18, 21, 24, 27]`


## Show the first letter of each word using Python


```
letters = [ name[0] for name in authors ]
print(letters)
```
Output

`['E', 'L', 'F', 'T', 'E', 'S']`



## Lower/Upper case converter using Python

```
lower_case = [ letter.lower() for letter in ['A','B','C'] ]
upper_case = [ letter.upper() for letter in ['a','b','c'] ]
print(lower_case, upper_case)
```

Output

`['a', 'b', 'c'] ['A', 'B', 'C']`


## Print numbers only from a given string
```
user_data = "Elvis Presley 987-654-3210"
phone_number = [ x for x in user_data if x.isdigit()]

print(phone_number)
```
Output

`['9', '8', '7', '6', '5', '4', '3', '2', '1', '0']`

## Parsing a file using list comprehension


# open the file in read-only mode
```
file = open("dreams.txt", 'r')
poem = [ line for line in file ]

for line in poem:
    print(line)
    ```
Output
```
Hold fast to dreams

For if dreams die

Life is a broken-winged bird

That cannot fly.

-Langston Hughs

```

## Using functions in list comprehensions


```
def double(x):
    return x*2

nums = [double(x) for x in range(1,10)]
print(nums)
```
Output


`[2, 4, 6, 8, 10, 12, 14, 16, 18]`
