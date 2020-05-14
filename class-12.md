# Docs for the HTML < canvas > Element & Chart.js

# Basic usage  
*The < canvas > element can be styled just like any normal image (margin, border, background…).  
These rules, however, don't affect the actual drawing on the canvas. When no styling rules are  
applied to the canvas it will initially be fully transparent.*  

<b>Fallback content</b>  
*The < canvas > element differs from an < img > tag in that, like for < video >, < audio >, or < picture >  
elements, it is easy to define some fallback content, to be displayed in older browsers not supporting  
it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always  
provide fallback content to be displayed by those browsers.*

*Providing fallback content is very straightforward: just insert the alternate content inside the  
< canvas > element. Browsers that don't support < canvas > will ignore the container and render  
the fallback content inside it. Browsers that do support < canvas > will ignore the content inside  
the container, and just render the canvas normally.*  

<b>Required </ canvas > tag</b>  
*As a consequence of the way fallback is provided, unlike the <img> element, the < canvas > element requires  
the closing tag (</ canvas >). If this tag is not present, the rest of the document would be considered  
the fallback content and wouldn't be displayed* 

*If fallback content is not needed, a simple <canvas id="foo" ...> </ canvas > is fully compatible with  
all browsers that support canvas at all.*  

<b>The rendering context</b>  
*The < canvas > element creates a fixed-size drawing surface that exposes one or more rendering contexts,  
which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering  
context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based  
on OpenGL ES.*

*The canvas is initially blank. To display something, a script first needs to access the rendering context  
and draw on it. The < canvas > element has a method called getContext(), used to obtain the rendering context  
and its drawing functions. getContext() takes one parameter, the type of context. For 2D graphics, such as  
those covered by this tutorial, you specify "2d" to get a CanvasRenderingContext2D.*  

1. | var canvas = document.getElementById('tutorial');  
2. | var ctx = canvas.getContext('2d');  

*The first line in the script retrieves the node in the DOM representing the < canvas > element by calling  
the document.getElementById() method. Once you have the element node, you can access the drawing context using  
its getContext() method.*  

<b>Checking for support</b>  
*The fallback content is displayed in browsers which do not support <canvas>. Scripts can also check for support  
programmatically by simply testing for the presence of the getContext() method.*  

# Drawing shapes with canvas  

<b>Drawing rectangles</b>  
*Unlike SVG, < canvas > only supports two primitive shapes: rectangles and paths (lists of points connected by lines).  
All other shapes must be created by combining one or more paths*  

*There are three functions that draw rectangles on the canvas:  

fillRect(x, y, width, height)
Draws a filled rectangle.  

strokeRect(x, y, width, height)
Draws a rectangular outline.  

clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.  

*Each of these three functions takes the same parameters. x and y specify the position on the canvas   
(relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.

<b>Drawing paths</b>  
*A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of  
different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths,  
we take some extra steps:*  

1. First, you create the path.  
2. Then you use drawing commands to draw into the path.  
3. Once the path has been created, you can stroke or fill the path to render it.  

Here are the functions used to perform these steps:

beginPath()
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.  

Path methods
Methods to set different paths for objects.  

closePath()
Adds a straight line to the path, going to the start of the current sub-path.  

stroke()
Draws the shape by stroking its outline.  

fill()
Draws a solid shape by filling the path's content area.  

*The first step to create a path is to call the beginPath(). Internally, paths are stored as a list of  
sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is  
reset and we can start drawing new shapes.*  

*The second step is calling the methods that actually specify the paths to be drawn. We'll see these shortly.*  

*The third, and an optional step, is to call closePath(). This method tries to close the shape by drawing a  
straight line from the current point to the start. If the shape has already been closed or there's only one  
point in the list, this function does nothing.*  
  
# Applying styles and colors  

<b>Colors</b>  
*If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.*  

fillStyle = color
Sets the style used when filling shapes.  

strokeStyle = color
Sets the style for shapes' outlines.  

*Color is a string representing a CSS < color >, a gradient object, or a pattern object. By default, the stroke  
and fill color are set to black (CSS color value #000000).*  

*The valid strings you can enter should, according to the specification, be CSS < color > values.*  

<b>Transparency</b>  
*In addition to drawing opaque shapes to the canvas, you can also draw semi-transparent (or translucent) shapes.  
This is done by either setting the globalAlpha property or by assigning a semi-transparent color to the stroke  
and/or fill style.*  

globalAlpha = transparencyValue
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0    
(fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.  

The globalAlpha property can be useful if you want to draw a lot of shapes on the canvas with similar transparency,  
but otherwise it's generally more useful to set the transparency on individual shapes when setting their colors.  

The rgba() function is similar to the rgb() function but it has one extra parameter. The last parameter sets the  
transparency value of this particular color. The valid range is again between 0.0 (fully transparent) and 1.0 (fully opaque).

    
# Drawing text
