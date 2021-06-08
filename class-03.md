## lists:
**● Ordered** lists are lists where each item in the list is
numbered. For example, the list might be a set of steps for
a recipe that must be performed in order, or a legal contract
where each point needs to be identified by a section
number.   
`<ol>`

**● Unordered lists** are lists that begin with a bullet point
(rather than characters that indicate order). ` <ul>`

**● Definition lists** are made up of a set of terms along with the definitions for each of those terms. `<dl>`

**you can nest list inside each other**

## Boxes:
**CSS treats each HTML element as if it lives in its own box.**

**The most popular ways to specify the size of a box are to use pixels,percentages, or ems**

**Designers
have recently started to use percentages and ems more for measurements as they try to create designs that are flexible across devices which have different-sized screens.**

## 1- width and height :
 min-width, max-width ,min-height, max-height

 **These are very helpful properties to ensure that the content of pages are legible (especially on the smaller screens of handheld devices).**

 ## 2- overflow: 
 (tells the browser what to do if the content contained within a box is larger than the box itself.)

 **hidden** This property simply hides any extra content that does not fit in the box.

**scroll** This property adds a scrollbar to the box so that users can scroll to see the missing content.

## 3- Border

Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

## 4- Margin

Margins sit outside the edge of the border. You can set the
width of a margin to create a gap between the borders of two
adjacent boxes.
## 5- Padding
Padding is the space between the border of a box and any
content contained within it. Adding padding can increase the
readability of its contents.


**If you want to center a box on the page (or center it inside
the element that it sits in), you can set the left-margin and
right-margin to auto.**


## 6- display:
The display property allows you to turn an inline element into a block-level element or vice versa.
+ inline

This causes a block-level
element to act like an inline
element.

+ block This causes an inline element to act like a block-level element.

+ inline-block This causes a block-level element to flow like an inline element, while retaining other features of a block-level element.

+ none This hides an element from the page.

## 7- visibility
 + hidden
This hides the element.
 + visible
This shows the element.


## border-image :
The border-image property applies an image to the border of
any box. It takes a background image and slices it into nine
pieces.


**This property requires three pieces of information:**

1: The URL of the image

2: Where to slice the image

3: What to do with the straight edges; the possible values are:
stretch stretches the image repeat repeats the image round like repeat but if the tiles do not fit exactly, scales
the tile image so they will.

## box-shadow
+ **Horizontal offset**Negative values position the
shadow to the left of the box.

+ **Vertical offset** Negative values position the
shadow to the top of the box. Blur distance If omitted, the shadow is a solid
line like a border.

+ **Spread of shadow** If used, a positive value will
cause the shadow to expand in all directions, and a negative
value will make it contract.


# array 
is a special type of variable. It doesn't
just store one value; it stores a list of values
`colors= ['white','black','custom'];`

To access a value from an array, after the array name you specify the index number for that value inside square brackets.


# dicions
**EVALUATIONS** You can analyze values in your scripts to determine whether or note they match expected results.

**DECISIONS & LOOPS**

DECISIONS Using the results of evaluations, you can decide which path your script should go down.

LOOPS There are also many occasions where you will
want to perform the same set of steps repeatedly.

**There are three types of loop: for, while, and
do ... while. Each repeats a set of statements**

+ DO WHILE LOOPS
+ while loops
+ for loops

 ## break
This keyword causes the
termination of the loop and tells
the interpreter to go onto the
next statement of code outside
of the loop. (You may also see it
used in functions.)

## continue
This keyword te lls the interpreter
to continue with the current
iteration, and then check the
condition again. (If it is true, the
code runs again.)

