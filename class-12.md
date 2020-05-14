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
  
 # Drawing shapes with canvas    


# Applying styles and colors  

# Drawing text
