# class 04 readings:
## links: 
Links are created using the` <a>` element. Users can click on anything
between the opening `<a>` tag and the closing `</a>` tag.

Links are created using the` <a>`
element which has an attribute
called **href**. The value of the
href attribute is the page that
you want people to go to when
they click on the link.

### On larger websites it's a good idea to organize your code by placing the pages for each different section of the site into a new folder. Folders on a website are sometimes referred to as directories.

## 1- Linking to Other Sites : (absolute URL.)
```
li><a href="http://www.empireonline.com">Empire
</a>
```


## 2-Linking to Other Pages on the Sa me Site : (relative URL.)


`<a href="index.html">Home</a>`

## 3- Email Links:
the
value of the href attribute starts with `mailto:` and is followed by the email address you want the email to be sent to.

`<a href="mailto:jon@example org">Email Jon</a>`

## 4- Opening Links in a New Window :
you can use the `target=` attribute on the opening `<a>` tag. The value of this attribute should be` _blank`.
`<a href="http://www.imdb.com" target="_blank"> Internet Movie Database</a>`
## 5-Linking to a Specific Part of the Same Page :
As long as the page you are linking to has `id` attributes that identify specific parts of the page, you can simply add the same syntax to the end of the link for that page.

**(either an absolute URL or
a relative URL), followed by the
`# `symbol, followed by the value
of the id attribute that is used on
the element you are linking to.**

`<a href="http:/www.htmlandcssbookcom/#bottom">`


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


# Functions:
group a series of statements together to perform a specific task.

**parameters** :information required by the functon in order to do its task.

**return value.** the outcome of the function
**You can also have anonymous function they dont have a name so the interpter
run them as soon it reach them**


![function](https://fireship.io/courses/javascript/img/function-declaration.png)
 

 **you call a function by typing its function name and the paramters if it needs any**


named function: 
```
function area (width, height)
return width * height;
};
var size= area(3, 4) ;
```
function exprission:
```
var area = f unction(width, height) {
r eturn width * height;
} ;
var size = area(3, 4) ;
```


## IMMEDIATELY INVOKED FUNCTION EXPRESSIONS :
these functions are not given
a name. Instead, they are executed once as the interpreter comes across them.

### when to use them :
 • As an argument when a function is called
(to calculate a value for that function).

• To assign the value of a property to an object.

• In event handlers and listeners
to perform a task when an event occurs

• To prevent conflicts between two scripts that might use the same variable names
```
var area = (function(){
var wi dth = 3;
var height = 2;
return width * height;
}());
```

## VARIABLE SCOPE :
+ **LOCAL VARIABLES** 
When a variable is created inside a function using the var keyword, it can only be used in that function. It is called a local variable or function-level variable
+ **GLOBAL VARIABLES**
If you create a variable outside of a function, then it can be used anywhere within the script. It is called a
global variable and has global scope.

**Global variables are stored in memory for as long
as the web page is loaded into the web browser.**
