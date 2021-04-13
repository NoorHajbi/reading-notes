# Read: 12 - Docs for the HTML <canvas> Element & Chart.js

## Article: Easily create stunning animated charts with chart.Js
- **Chart.js**   is a free open-source JavaScript library for data visualization(to create charts).
- Setting up:
1. Import the script on html page` <script src='Chart.min.js'></script>`.
2. Create a **canvas** element in our HTML in which Chart.js.`<canvas id="" width="" height=""></canvas>`
3. Write a script that will retrieve the context of the canvas.
4. Inside the same script tags we need to create our data.
---
## Article: Basic usage of canvas
- The `<canvas>` element can be styled just like any normal image (margin, border, background).
- You should always provide **fallback content** to display **Canvas**In older browsers.
-  The `<canvas>` element has a method called `getContext()`(takes one parameter), used to obtain the rendering context and its drawing functions.*ex: `var ctx = canvas.getContext('2d');`* .
---
## Article: Drawing shapes with canvas
-  `<canvas>` only supports two primitive shapes: rectangles and paths (lists of points connected by lines). 
### Three functions that draw rectangles on the canvas:
1. `fillRect(x, y, width, height)` -> Draws filled rectangle.
2. `strokeRect(x, y, width, height)` -> Draws a rectangular outline.
3. `clearRect(x, y, width, height)` -> Clears the specified rectangular area, making it fully transparent.
ch side. 
- The `clearRect()` function  erases a `numxnum` pixel square from the center.
---
### Drawing paths:
1. **First Step:** `beginPath()` -> Creates a new path. 
2. **Path methods** -> Methods to set different paths for objects.
3. `closePath()` ->  Adds a straight line to the path, going to the start of the current sub-path.
`stroke()` -> Draws the shape by stroking its outline.
`fill()` -> Draws a solid shape by filling the path's content area.
- **Note:** When you call `fill()`, any open shapes are closed automatically, so you don't have to call `closePath()`. 
---
### Drawing a triangle:
- the `moveTo()` function-> it is like lifting a pen or pencil from one spot on a piece of paper and placing it on the next.

- `moveTo(x, y`) Moves the pen to the coordinates specified by x and y.
---
### Lines:
- `lineTo(x, y)` -> For drawing straight lines, Draws a line from the current drawing position to the position specified by x and y.
---
### Arcs
- `arc()` or `arcTo()` -> To draw arcs or circles.
- `arc(x, y, radius, startAngle, endAngle, counterclockwise)` ->
Draws an arc which is centered at *(x, y)* position with *radius* r starting at *startAngle* and ending at *endAngle* going in the given direction indicated by *counterclockwise* (defaulting to clockwise).
- `arcTo(x1, y1, x2, y2, radius)` -> 
Draws an arc with the given control points and radius, connected to the previous point by a straight line.

- **Note:** Angles in the arc function are measured in radians, not degrees. 
---
### Bezier and quadratic curves:  

- `quadraticCurveTo(cp1x, cp1y, x, y)`
Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.
- `bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)`
Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).
--- 
### Rectangles:
In addition to the three methods....

- `rect(x, y, width, height)` ->
Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.
---
- **we can Make combinations of previous functions**
---
### Path2D objects
- the **Path2D** object, available in recent versions of browsers.
- `Path2D()` -> constructor returns a newly instantiated Path2D object.
---
## Article: Applying styles and colors
### two important properties to apply colors to a shape:
1. `fillStyle = color` -> Sets the style used when filling shapes.
2. `strokeStyle = color`-> Sets the style for shapes' outlines.
- By default, the stroke and fill color are set to black (CSS color value #000000).
---
### Transparency
- drawing a semi-transparent (or translucent) shapes, can be done by either setting the **globalAlpha** property or by assigning a **semi-transparent** color to the *stroke and/or fill style*
- `globalAlpha = transparencyValue` -> The value must be between 0.0 (fully transparent) to 1.0 (fully opaque)-which is defualt value. 
---
### Line styles properties:
- `lineWidth = value`
- `lineCap = type` -> Sets the appearance of the ends of lines; it's *values* **butt, round and square.**
- `lineJoin = type` -> Sets the appearance of the "corners" where lines meet.*Values: **round, bevel and miter***
-`miterLimit = value` -> Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
-`getLineDash()` -> Returns the current line dash pattern array containing an even number of non-negative numbers.
- `setLineDash(segments)` -> Sets the current line dash pattern.
- `lineDashOffset = value` -> Specifies where to start a dash array on a line.
---
### Gradients
- `createLinearGradient(x1, y1, x2, y2)` -> Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).
- `createRadialGradient(x1, y1, r1, x2, y2, r2)` -> Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.
- `createConicGradient(angle, x, y)` -> Creates a conic gradient object with a starting angle of angle in radians, at the position (x, y).
---
### Patterns
- `createPattern(image, type)`
- **The type values:**
1. `repeat` -> Tiles the image in both vertical and horizontal directions.
2. `repeat-x` -> Tiles the image horizontally but not vertically.
3. `repeat-y` -> Tiles the image vertically but not horizontally.
4. `no-repeat` -> Doesn't tile the image. It's used only once.
---
### Shadows
- `shadowOffsetX = float` -> Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.
- `shadowOffsetY = float` -> same but for *vertical distance*.
- `shadowBlur = float` -> Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.
- `shadowColor = color` -> A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.
---
## Article: Drawing text
### Drawing text 2methods:
- `fillText(text, x, y [, maxWidth])` -> Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
- `strokeText(text, x, y [, maxWidth])` -> Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
### Styling text properties:
- `font = value` -> This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
- `textAlign = value` -> *Possible values: **start, end, left, right or center***. The **default value is start**.
- `textBaseline = value` -> Baseline alignment setting. *Possible values: **top, hanging, middle, alphabetic, ideographic, bottom***. The **default value is alphabetic**.
- `direction = value` -> Directionality. *Possible values: **ltr, rtl, inherit***. The **default value is inherit**.

