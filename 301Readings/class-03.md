## Lists and Keys :

1-What does .map() return?
**returns the elemnts of the array after making a modification on it** 


2-Each list item needs a unique?
 **Keys**

3- If I want to loop through an array and display each value in JSX, how do I do that in React?

**JSX allows embedding any expression in curly braces so we could inline the map()** 

4- What is the purpose of a key?

**key is unique value  used to help browser and developer fnd the difference or the modification that happened to the comoponent tree faster.**

## The Spread Operator :

1-  What is the spread operator?

** ellipsis of three dots (…) to expand an iterable object into the list of arguments.**



2- List 4 things that the spread operator can do?


**Copying an array**

**Concatenating or combining arrays**

**Using Math functions**

**Using an array as arguments**

**Adding an item to a list**


3-Give an example of using the spread operator to combine two arrays?
```
let array1=[1,2,3];
let array2=[1,2,3];

let theArr=[..arr1,...arr2];

```

4-Give an example of using the spread operator to add a new item to an array?

```
let array1=[1,2,3];
let number=5;

let theArr=[num,...arr2]

```

5-Give an example of using the spread operator to combine two objects into one?

```
let object1={};
let object2={};

let object={...obj1,...obj2}

```

## Pass functions between components:



1- In the video, what is the first step that the developer does to pass functions between components?

** define the function inside the parent and pass it to the child as a prop**


2- n your own words, what does the increment function do?

**recive a name and match with the objects names in the state to  find a matching name and update the value of count to that object**


3-How can you pass a method from a parent component into a child component?

**you can pass it as a prop**



4-How does the child component invoke a method that was passed to it from a parent component?


** by calling  the prop that holds the function inside the child function**
