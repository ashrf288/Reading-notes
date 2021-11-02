# Regular Expression

sequence of characters used to check whether a pattern exists in a given text (string) or not


## In Python, regular expressions are supported by the re module

```
import re
```

## Basic Patterns

Ordinary characters can be used to perform simple exact matches

```
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")

## #################result######################

Match!
```



The **match()** function returns a match object if the text matches the pattern. Otherwise, it returns None

`r''`
**This is called a raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.**

 `search()` 

 the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.

`group().`

The group function returns the string matched by the re. You will see both these functions in more detail later.




## Wild Card Characters: Special Characters

characters that do not match themselves as seen but have a special meaning when used in a regular expression


+ `.`  A period. Matches any single character except the newline character.
```
re.search(r'Co.k.e', 'Cookie').group()
'Cookie'
```

+ `^`  A caret. Matches the start of the string.

This is helpful if you want to make sure a document/sentence starts with certain characters.

`re.search(r'^Eat', "Eat cake!").group()`


+ `$`  Matches the end of string.

This is helpful if you want to make sure a document/sentence ends with certain characters.

`re.search(r'cake$', "Cake! Let's eat cake").group()`

`[abc]` - Matches a or b or c.

`[a-zA-Z0-9]` - Matches any letter from (a to z) or (A to Z) or (0 to 9).


 **Characters that are not within a range can be matched by complementing the set. If the first character of the set is `^`, all the characters that are not in the set will be matched.**

```
re.search(r'[0-6]', 'Number: 5').group()
'5'
## Matches any character except 5
re.search(r'Number: [^5]', 'Number: 0').group()

## This will not match and hence a NONE value will be returned
#re.search(r'Number: [^5]', 'Number: 5').group()
'Number: 0'
```


+ `\` - Backslash.
Perhaps, the most diverse metacharacter!!

1- If the character following the backslash is a recognized escape character, then the special meaning of the term is taken 

2- Else if the character following the `\` is not a recognized escape character, then the `\` is treated like any other character and passed through

3-`\ `can be used in front of all the metacharacters to remove their special meaning 


+ `\w` - Lowercase 'w'. Matches any single letter, digit, or underscore.
`\W` - Uppercase 'W'. Matches any character not part of \w (lowercase w).



+ `\s` - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
`\S` - Uppercase 'S'. Matches any character not part of \s (lowercase s).


+ `\d` - Lowercase d. Matches decimal digit 0-9.
`\D` - Uppercase d. Matches any character that is not a decimal digit.


`\t` - Lowercase t. Matches tab.

`\n `- Lowercase n. Matches newline.

`\r` - Lowercase r. Matches return.

`\A` - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.

`\Z` - Uppercase z. Matches only at the end of the string.


`\b` - Lowercase b. Matches only the beginning or end of the word.

## Repetitions


+ `+` - Checks if the preceding character appears one or more times starting from that position.

+ `* `- Checks if the preceding character appears zero or more times starting from that position.

+ `?` - Checks if the preceding character appears exactly zero or one time starting from that position.

+ Repeat

`{x}` - Repeat exactly x number of times.

`{x,}` - Repeat at least x times or more.

`{x, y}` - Repeat at least x times but no more than y times


## Grouping in Regular Expressions


The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis `()`



## Greedy vs. Non-Greedy Matching

When a special character matches as much of the search sequence (string) as possible, it is said to be a "Greedy Match"




[complete list of regex](https://docs.python.org/3/library/re.html#re-syntax)



# shutil 

## Copying Files

copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.
```
shutil_copyfile.py
import glob
import shutil

print('BEFORE:', glob.glob('shutil_copyfile.*'))

shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

print('AFTER:', glob.glob('shutil_copyfile.*'))
```

Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as new special files with copyfile().


The implementation of copyfile() uses the lower-level function copyfileobj(). While the arguments to copyfile() are filenames, the arguments to copyfileobj() are open file handles. The optional third argument is a buffer length to use for reading in blocks.



## Copying File Metadata


By default when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file to another, use copymode().

```
shutil_copymode.py
import os
import shutil
import subprocess

with open('file_to_change.txt', 'wt') as f:
    f.write('content')
os.chmod('file_to_change.txt', 0o444)

print('BEFORE:', oct(os.stat('file_to_change.txt').st_mode))

shutil.copymode('shutil_copymode.py', 'file_to_change.txt')

print('AFTER :', oct(os.stat('file_to_change.txt').st_mode))
```

## Working With Directory Trees

shutil includes three functions for working with directory trees. To copy a directory from one place to another, use copytree(). It recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.

```
shutil_copytree.py
import glob
import pprint
import shutil

print('BEFORE:')
pprint.pprint(glob.glob('/tmp/example/*'))

shutil.copytree('../shutil', '/tmp/example')

print('\nAFTER:')
pprint.pprint(glob.glob('/tmp/example/*'))
```



## Finding Files


The which() function scans a search path looking for a named file. The typical use case is to find an executable program on the shell’s search path defined in the environment variable PATH.

```
shutil_which.py
import shutil

print(shutil.which('virtualenv'))
print(shutil.which('tox'))
print(shutil.which('no-such-program'))
```


## Archives

Python’s standard library includes many modules for managing archive files such as tarfile and zipfile. There are also several higher-level functions for creating and extracting archives in shutil. get_archive_formats() returns a sequence of names and descriptions for formats supported on the current system.

```
shutil_get_archive_formats.py
import shutil

for format, description in shutil.get_archive_formats():
    print('{:<5}: {}'.format(format, description))
```


## File System Space

It can be useful to examine the local file system to see how much space is available before performing a long running operation that may exhaust that space. disk_usage() returns a tuple with the total space, the amount currently being used, and the amount remaining free

```
shutil_disk_usage.py
import shutil

total_b, used_b, free_b = shutil.disk_usage('.')

gib = 2 ** 30  # GiB == gibibyte
gb = 10 ** 9   # GB == gigabyte

print('Total: {:6.2f} GB  {:6.2f} GiB'.format(
    total_b / gb, total_b / gib))
print('Used : {:6.2f} GB  {:6.2f} GiB'.format(
    used_b / gb, used_b / gib))
print('Free : {:6.2f} GB  {:6.2f} GiB'.format(
    free_b / gb, free_b / gib))
```

```
#######result

$ python3 shutil_disk_usage.py

Total: 499.42 GB  465.12 GiB
Used : 246.68 GB  229.73 GiB
Free : 252.48 GB  235.14 GiB

```
