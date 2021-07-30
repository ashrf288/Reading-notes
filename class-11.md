# images :
(images are **inline** elements. This means that they
flow within the surrounding text.)

You can control the size of an
image using the `width` and `height` properties in CSS.

In order to center an image, it should be turned into a blocklevel
element using the display property.


## Background Images:

place an image behind any HTML element. This could be the entire
page or just part of the page.


1-`background-repeat` have 3 values :
```
repeat-x
repeat-y
no-repeat
```


`background-attachment`

**fixed** The background image stays in
the same position on the page.

**scroll** The background image moves
up and down as the user scrolls up and down the page.


`background-position`
use it when the background is not being repeated to controll where do you want the image to be placed




## spirits
When a single image is used
for several different parts of an
interface, it is known as a sprite.


## rollover
a link or button that changes to a second style when a user moves
their mouse over it



**you shoul lower the consttrat of your image if you want to add text to it and make the text clear**



## BREAKPOINTS :
**pause the execution of a script on any
line using breakpoints. Then you can check the
values stored in variables at that point in time.**

very important in debugging


you can set multiple breakpoints 

## CONDITIONAL
BREAKPOINTS You can indicate that a breakpoint should be triggered only if a condition that you specify is met.


## HANDLING EXCEPTIONS:
**use `try`, `catch`, and `finally`**


**1-TRY**
 specify the code that you t hink might throw an
exception within the try block.

**2-CATCH** If the try code block throws an exception, catch steps in with an alternative set of code.


**3-FI NALLY**
The contents of the fi na 11 y code block will run either
way - whether the try block succeeded or failed.



## THROWING ERRORS
add  your own errors if you know the code will cuase errors

`throw new Error( 1message 1) ;`


## DEBUGGING TIPS :

1-ANOTHER BROWSER

2-ADD NUMBERS

3-STRIP IT BACK


4-EXPLAINING THE CODE

5-SEARCH (Stack Overflow)

6-VALIDATION TOOLS (jquery)



## COMMON ERRORS :
1- case sensetive
2- variable scope 
3-reserved words
4- extra characters
5-data types issues


## Video and Audio APIs:

The `<video>` and `<audio>` elements allow us to embed video and audio into web pages :
```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```
 **controls** which enables the default set of playback controls. If you don't specify this, you get no playback controls

 `<video>` element contains two `<source>` elements so that different formats can be loaded depending on the browser viewing the site.


 ## The HTMLMediaElement API
  API provides features to allow you to control video and audio players programmatically.

  you can style them using css and add functionality using java script just like any other html element
