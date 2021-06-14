## layouts:
**CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.**

**Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding text**


Block-level elements start on a new line Examples include:
`<h1> <p> <ul> <li> <div>`

Inline elements flow in between
surrounding text Examples include:
`<img> <b> <i>`

## positioning schemes:
##  Normal flow :
`position:static` you dont need to write it its the defult 

## 2-Relative Positioning :
This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.

Relative positioning moves an element in relation to where it would have been in normal flow.
`position:relative`

## 3-Absolute positioning
Absolutely positioned elements move as users scroll up and down the page.
(They act like it is not there.)

**box offset**: properites to control the postitoning of an elemnt used in absoluete postitoning.

`position:absolute`
The box offset properties (top or bottom and left or right) specify where the element should appear in relation to its containing element.
```
h1 {
position: absolute;
top: 0px;
left: 500px;
width: 250px;}
p {
width: 450px;}
```
**types :**
  + Fixed Positioning :
It positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place.

**To control where the fixed position box appears in relation to the browser window, the box offset properties are used.**

**Overlapping Elements :**
If you want to control which element sits on top, you can use the` z-index` property. Its value is a `number`, and the higher the number the closer that element is to the front.

## 4- float : 
When you use the `float` property, you should also use the `width` property to indicate how wide the floated element should be. If you do not, results can be inconsistent but the box is likely to take up the full width of the containing element .


**use flow to style elemnts next to each other:
+ Clearing Floats:

to say that no element (within
the same containing element)
should touch the left or righthand
sides of a box.

**it takes 4 values :**
left(elemnts should not touch the left side),right(elemnts should not touch the right side),both(no touch for left and right),none(elemnts can touch).
`clear=left;`


**issue: If a containing element only contains floated elements, some browsers will treat it as if it is zero pixels tall.**
 
 **solution: by adding an extra element after the last floated box (inside the containing element**

**recent solution**

● The overflow property is
given a value auto.

● The width property is set to
100%.

**you can create multi column in the website using float**



## layouts:
 + **A Fixed Width Layout**
 the width of the main boxes on a page will usually be specified in pixels.

 + **A Liquid Layout**  layout uses percentages to specify the width of each box so that the design will stretch to fit the size of the screen.

 This is where the `min-width` and `max-width` properties help create boundaries within which the layout can stretch.

 + **Layout Grids**  Grids set consistent proportions and spaces between items which helps to create a professional looking design.

 ## CSS Frameworks :
providing the code for common tasks, such as creating layout grids, styling forms.


## Multiple Style Sheets :


**1- @import** : HTML page can link
to one style sheet and that stylesheet can use the @import rule to import other style sheets.

`@import url("tables.css");`

**2-link** : Inside the `<head> `element is a separate `<link>` element for each style sheet
