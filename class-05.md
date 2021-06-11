# images :
## Images should...
+ Be relevant
+ Convey information
+ Convey the right mood
+ Be instantly recognisable
+ Fit the color palette


**Use JPEG format for all images that contain a natural scene or photograph where variation in colour and intensity is smooth.**

 **Use PNG format for any image that needs transparency or for images with text & objects with sharp contrast edges like logos.**
 
 **Use GIF format for images that contain animations.**


To add an image into the page you need to use an `<img>`
element. This is an empty element ,It must carry the
following two attributes :
+ **`alt`** 
This provides a text description
of the image which describes the
image if you cannot see it.
+ **`src`**
  This tells the browser where
it can find the image file.

example:
```
<img src="images/quokka.jpg" alt="A family of
quokka"/>
```


`height` This specifies the height of the image in pixels.  `width` This specifies the width of the image in pixels.

**but its better practice to use css to cnotrol width and height  and the align atrributes of the image**


## where to put the image in youw website:
**1: before a paragraph**

**2:inside the start of a
paragraph**

**3: in the middle of a
paragraph**

## Three Rules for Creating Images :
1-Save images in the right format.

2-Save images at the right size.

3-Use the correct resolution.

**The images you use on your website should be
saved at the same width and height that you
want them to appear on the page.**

**Images created for the web should be saved at
a resolution of 72 ppi. The higher the resolution
of the image, the larger the size of the file.**


## Vector Images :
such as a logo The advantage of creating line
drawings in vector format is that you can increase the dimensions of the image without affecting the quality of it.

 + Animated GIFs :
 Animated GIFs show several frames of an
image in sequence and therefore can be used to
create simple animations  
**Each extra frame of the image
increases the size of the file, and
can therefore add to the time it
takes for an image to download**


### Creating an image that is partially transparent (or "see-through") for the web involves selecting one of two formats:
+ Transparent GIF  
+ PNG


## Figure and Figure Caption :
Before these elements were
created there was no way to
associate an `<img>` element with
its caption.
```
<figure>
<img src="images/otters.jpg" alt="Photograph of
two sea otters floating in water">
<br />
<figcaption>Sea otters hold hands when they
sleep so they don't drift away from each
other.</figcaption>
</figure>
```

# COLOR :
**+ rgb values** These express colors in terms
of how much red, green and blue are used to make it up. For
example: rgb(100,100,90).

**+ hex codes** These are six-digit codes that
represent the amount of red, green and blue in a color,
preceded by a pound or hash # sign. For example: #ee3e80

**+ color names** There are 147 predefined color
names that are recognized by browsers. For example:
DarkCyan.

**+ Hue** 
Hue is near to the colloquial idea
of color. Technically speaking
however, a color can also have
saturation and brightness as
well as hue.

**+ Saturation**
Saturation refers to the amount
of gray in a color. At maximum
saturation, there would be no
gray in the color. At minimum
saturation, the color would be
mostly gray.

**+ Brigh tness**
Brightness (or "value") refers
to how much black is in a color.
At maximum brightness, there
would be no black in the color.
At minimum brightness, the
color would be very dark.



## 1- color:
The `color` property allows you
to specify the color of text inside
an element.

## 2- background-color :


## 3-Opacity:
specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0.


**hsl, hsla**
The value of the property starts with the letters hsl, followed by individual values inside parentheses for:
**hue,saturation,lightness,alpha(transparency).**



# text:

The properties that allow you to control
the appearance of text can be split into
two groups:

+ Those that directly affect the font and its appearance
(including the typeface, whether it is regular, bold or italic,
and the size of the text)

+ Those that would have the same effect on text no matter
what font you were using (including the color of text and
the spacing between words and letters).



**1- font-family:** The value of this property is the
name of the typeface you want
to use.


**2- font-size :** specify a size for the
font. 

**+ pixels** 
Pixels are commonly used because they allow web designers very precise control over how much space their text
takes up.

**+ percentages**

**+ ems** An em is equivalent to the width
of a letter m.

**3- font-weight :**

**+normal**
This causes text to appear at a normal weight.

**+ bold**
This causes text to appear bold.

**4-font-style**

**+ normal**


  **+italic**
This causes text to appear italic.

  **+oblique**
This causes text to appear
oblique.

**5-text-transform**

**uppercase**
This causes the text to appear
uppercase.

**lowercase**
This causes the text to appear
lowercase.

**capitalize**
This causes the first letter of
each word to appear capitalized.


**6-text-decoration**
**none**
This removes any decoration
already applied to the text.

**underline**
This adds a line underneath the
text.

**overline**
This adds a line over the top of
the text.

**line-through**
This adds a line through words.
blink
This animates the text to make it
flash on and off .

**7-line-height**

**8-text-align**

**left** This indicates that the text
should be left-aligned.

**right**
This indicates that the text
should be right-aligned.

**center**
This allows you to center text.

**justify**
This indicates that every line in
a paragraph, except the last line,
should be set to take up the full
width of the containing box.


**9- vertical-align**
more used with inline elemnts
```
baseline
sub
super
top
text-top
middle
bottom
text-bottom
```
**10-text-indent**
indent the first
line of text within an element

**11-text-shadow**

**:first-letter, :first-line**
Technically these are not
properties. They are known as
pseudo-elements
```

p.intro:first-letter {
font-size: 200%;}
p.intro:first-line {
font-weight: bold;}
```

**12-Styling links :**

**:link**
This allows you to set styles
for links that have not yet been
visited.

**:visited**
This allows you to set styles for
links that have been clicked on.
```
a:link {
color: deeppink;
text-decoration: none;}
a:visited {
color: black;}
a:hover {
color: deeppink;
text-decoration: underline;}
a:active {
color: darkcyan;}
```

**13-Responding to Users :**
```
:hove
 :active
  :focus
  ```
  ```
  input {
padding: 6px 12px 6px 12px;
border: 1px solid #665544;
color: #ffffff;}
input.submit:hover {
background-color: #665544;}
input.submit:active {
background-color: chocolate;}
input.text {
color: #cccccc;}
input.text:focus {
color: #665544;}
```
