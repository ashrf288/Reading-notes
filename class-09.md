# forms :


## Form Structure:
Form controls live inside  `<form>` element.

**1-action** Every <form> element requires
an action attribute. Its value
is the URL for the page on the
server that will receive the
information in the form when it
is submitted.

**2-method**
Forms can be sent using one of
two methods: get or post

```
<form action="http://www.example.com/subscribe.php"
method="get">
<p>This is where the form controls will appear.
</p>
</form>
```

**`name`
When users enter information
into a form, the server needs to
know which form control each
piece of data was entered into.**


## `<input>`

1- `type="text"`  creates a singleline
text input.

2-`type="password"`

3-`type="radio"`

**value**
The value attribute indicates
the value that is sent to the
server

**checked**
The checked attribute can be
used to indicate which value (if
any) should be selected when
the page loads.

4-`type="checkbox"`

**value**
The value attribute indicates
the value sent to the server if this
checkbox is checked.

**checked**
The checked attribute indicates
that this box should be checked
when the page loads.

5-`type="file"`
This type of input creates a
box that looks like a text input
followed by a **browse button**.
When the user clicks on the
browse button, a window opens
up that allows them to select a
file from their computer to be
uploaded to the website.

6-`type="submit"`

`value`
The value attribute is used to
control the text that appears
on a button.

7-`type="image"`

8-`type="date"`

9-`type="email"`

10-`type="search"`



## `<textarea>`
The `<textarea>` element
is used to create a mutli-line
text input.


## Drop Down List Box:
`<select>`


`<option>`
The `<option>` element is used
to specify the options that the
user can select from.

## button 
newley introduced

## `<label>`
`for`
The for attribute states which
form control the label belongs to


## Grouping Form Elements:

`<fieldset>`You can group related form
controls together inside the
`<fieldset>` element

`<legend>`
The `<legend>` element can
come directly after the opening
`<fieldset>` tag and contains a
caption which helps identify the
purpose of that group of form
controls.


# lists tables and forms : 


1-list-style-type

**Unordered Lists**

For an unordered list you can use
the following values:
```
none
disc
circle
square
```

**Ordered Lists**

For an ordered (numbered) list
you can use the following values:
```
decimal
1 2 3
decimal-leading-zero
01 02 03
lower-alpha
a b c
upper-alpha
A B C
lower-roman
i. ii. iii.
upper-roman
I II III
```

**list-style-image**
```
ul {
list-style-image: url("images/star.png");
}
```
**list-style-position**

`outside`
The marker sits to the left of the
block of text.

`inside`
The marker sits inside the box of
text (**which is indented**).


## Table Properties:
`width`
 to set the width of the table

`padding` to set the space
between the border of each table
cell and its content
`text-transform` to convert the
content of the table headers to
uppercase
`letter-spacing`, 
`font-size`
to add additional styling to the
content of the table headers

`border-top`, `border-bottom`
to set borders above and below
the table headers

**empty-cells**

`show`
This shows the borders of any
empty cells.

`hide`
This hides the borders of any
empty cells.

`inherit`
If you have one table nested
inside another, the inherit
value instructs the table cells to
obey the rules of the containing
table.


## Styling Forms :

 1-Styling Text Inputs:
 font-size sets the size of the
text entered by the user.

2-color sets the text color

3- background-color sets the
background color of the input.

4- border adds a border around
the edge of the input box

5- border-radius can be used
to create rounded corners


**Styling Submit Buttons**
1-color is used to change the
color of the text on the button.

2-text-shadow can give a 3D
look to the text in browsers that
support this property.

3- border-bottom has been used
to make the bottom border of
the button slightly thicker, which
gives it a more 3D feel.

**Styling Fieldsets
& Legends**

width is used to control
the width of the fieldset.

color is used to control the
color of text.

background-color is used to
change the color behind these
items.

border is used to control the
appearance of the border around
the fieldset and/or legend.



# events:

When you browse the web, your browser registers different
types of events.


**THREE WAYS TO BIND ANEVENT TO AN ELEMENT**

There are three types of event handlers:

1-HTML EVENT HANDLERS.


2-TRADITIONAL DOM EVENT HANDLERS:

they let you separate the
JavaScript from the HTML.
**The main drawback is that you
can only attach a single function
to any event.**


3-Event listeners
event listeners allow
one event to trigger multiple
functions. As a result, there
are less likely to be conflicts
between different scripts that
run on the same page



**Because you cannot have parentheses after the
function names in event handlers or listeners,
passing arguments requires a workaround**


**if you need to pass
arguments to a function that is
called by an event handler or
listener, you wrap the function
call in an anonymous function**


## THE EVENT OBJECT

## MOUSE EVENTS :

1- CLICK :
You may also be tempted to use
the c 1 i ck event to run a script
when a user clicks on a form
element, but it is better to use
the focus event because that
fires when the user accesses
that control using the tab key



## KEYBOARD EVENTS :

The three events that begin key  in this order:

1. keydown - user presses key down

2. keypress - user has pressed or is holding a keY
that adds a character into the page

3. keyup - user releases key

## FORM EVENTS :

1-FOCUS AND BLUR 
2-VALIDATION (Checking form values)



## MUTATION EVENTS & OBSERVERS :

Whenever elements are added to or removed from the DOM, its
structure changes. This change triggers a mutation event
**PROBLEMS WITH MUTATION EVENTS**
If your script makes a lot of changes to a page, you
end up with a lot of mutation events firing. This can
make a page fee l slow or unresponsive

**NEW MUTATION OBSERVERS**
Mutation observers are designed to wait until a
script has finished its task before reacting, then
report the changes as a batch
