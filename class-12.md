# charts :

** Chart.js,** a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page



## setting up :

1- download **Chart.js.** (zip folder) 

2-Copy the **Chart.min.js** ( into the directory you’ll be working in)

3-create a new html page and **import** the script.

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>
```
## some types of charts:
**1- bar charts **
1- add this to the body of our HTML page:

`<canvas id="income" width="600" height="400"></canvas>`

2-retrieve the context of the canvas:

var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);



**2- line charts**
1- add this to the body of our HTML page:

`<canvas id="buyers" width="600" height="400"></canvas>`
`new Chart(buyers).Line(buyerData);`

2-retrieve the context of the canvas:

`var buyers = document.getElementById('buyers').getContext('2d');`


**3-pie charts**

1- add this to the body of our HTML page:


`<canvas id="countries" width="600" height="400"></canvas>`

2-retrieve the context of the canvas:
`var countries= document.getElementById("countries").getContext("2d");`
`new Chart(countries).Pie(pieData, pieOptions);`


# The <canvas> element :
the `<canvas>` element has only two attributes,` width `and` height`

The `id` attribute isn't specific to the `<canvas>` element but is one of the **global HTML attributes**

**The <canvas> element can be styled just like any normal image
however, don't affect the actual drawing on the canvas.**


**Fallback content** content to be displayed if the browser dosenot support the feature.

 ### how to apply it : just insert the alternate content inside the <canvas> element. thats why  `<canvas>` element requires the closing tag `(</canvas>)`


 ## rendering context:
  which are used to create and manipulate the content shown,a script first needs to access the rendering context and draw on it.

  ** <canvas> element has a method called `getContext()`, used to obtain the rendering context**


  ## Drawing shapes with canvas :

   `<canvas>` only supports two primitive shapes: **rectangles and paths** (lists of points connected by lines) ,All other shapes must be created by combining one or more paths

   **rectangle functions draw immediately to the canvas.**


   ## paths :

   First, you create the path.

   `beginPath()`

Then you use **drawing commands** to draw into the path.

Once the path has been created, you can stroke or fill the path to render it.

`closePath()`

`stroke()`

`fill()`

`moveTo(x, y)` use it to draw unconnected paths

` lineTo(x,y)` to draw staight lines

`rect(x, y, width, height)` draw a rectangle

`arc(x, y, radius, startAngle, endAngle, counterclockwise)` to draw arc or circle 

`quadraticCurveTo(cp1x, cp1y, x, y)` draw complex shapes


## Path2D objects :
simplify the code and to improve performance, using SVG path data to initialize paths on your canvas.



## Colors:

`fillStyle = color`
Sets the style used when filling shapes.
`strokeStyle = color`
Sets the style for shapes' outlines.

`globalAlpha = transparencyValue` gives transperancy

 0.0 (fully transparent) to 1.0 (fully opaque/defult)


 ## Line styles
 `lineWidth = value`
Sets the width of lines drawn in the future.

`lineCap = type`
Sets the appearance of the ends of lines.

`lineJoin = type`
Sets the appearance of the "corners" where lines meet.

`miterLimit = value`
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

`getLineDash()`
Returns the current line dash pattern array containing an even number of non-negative numbers.

`setLineDash(segments)`
Sets the current line dash pattern.

`lineDashOffset = value`
Specifies where to start a dash array on a line.

## Gradients
`createLinearGradient(x1, y1, x2, y2)`
Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).

`createRadialGradient(x1, y1, r1, x2, y2, r2)`
Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.

`createConicGradient(angle, x, y)`
Creates a conic gradient object with a starting angle of angle in radians, at the position (x, y).

`gradient.addColorStop(position, color)`

position is a number between 0.0 and 1.0

## Patterns:
`createPattern(image, type)`

**repeat**
Tiles the image in both vertical and horizontal directions.

**repeat-x**
Tiles the image horizontally but not vertically.

**repeat-y**
Tiles the image vertically but not horizontally.

**no-repeat**
Doesn't tile the image. It's used only once

## Shadows

`shadowOffsetX = float`

Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0

`shadowOffsetY = float`
Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

`shadowBlur = float`
Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.

`shadowColor = color`
A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.


Canvas fill rules: 

1-"nonzero "  
 2-"evenodd"

 ## Drawing text
 
 `fillText(text, x, y [, maxWidth])`
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.

`strokeText(text, x, y [, maxWidth])`
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

## Styling text :
font , textalign,decoration

`measureText()`
Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style


 
