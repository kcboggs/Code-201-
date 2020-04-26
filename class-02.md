#  HTML Text, CSS Introduction & Basic JavaScript Instructions  

# Text  
- Headings and Paragraphs  
  
<h1>Heading 1</h1>  
*Is used for main headings*  
<h2>Heading 2</h2>  
*Is used for subheadings*  
<h3>Heading 3</h3>
*and so on are used for further sectioning under the
subheadings*  

- Bold, italic, emphasis  

<b><i>This is how to make a word appear bold and italic</i></b>  

- Structural and semantic markup  

*Structural markup are the elements that you can use
to describe both headings and paragraphs and Semantic
markups provide extra information; such as where emphasis
is placed in a sentence, that something you have written 
is a quotation*  

# Introducing CSS  
- What CSS does  

*CSS allows you to create rules that control the way that each
individual box (and the contents of that bax) is presented.*  

p { 
  font-family: Arial;}  

- How CSS works  

*CSS works by associating style rules with HTML elements These rules
govern how the content of specified elements should be displayed.
A CSS rule contains two parts: a selector and a declaration.*  

- Rules, properties and values  

*A CSS rule is a grouping of one or more CSS properties which are to be 
applied to one or more target HTML elements. A CSS rule consists of a CSS 
selector and a set of CSS properties. The CSS selector determines what HTML 
elements to target with the CSS rule.*  

# Basic JavaScript Instructions  

- Statements  

*A script is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement. Statements should
end with a semicolon.*  

var today = new Date();
var hourNow = today.getHours();
var greeting;  

if (hourNow >18 {
    greeting = 'Good Evening';  
}   else if (hourNow >12 {
    greeting = 'Good Afternoon';  
}   else if (hourNow >0 {
    greeting 'Good Morning';  
}   else {  
    greeting = 'Welcome';  
}  
document.write(greeting);  

- Comments  

*You should write comments to explain what your code does. They help make 
your code easier to read and understand. This can help you and others who 
read your code.*  

/* */

- Variables  

*Variables are used to store information to be referenced and manipulated in a 
computer program. They also provide a way of labeling data with a descriptive 
name, so our programs can be understood more clearly by the reader and ourselves. 
It is helpful to think of variables as containers that hold information. Their 
sole purpose is to label and store data in memory. This data can then be used 
throughout your program.*  

var quantity;   
is how you declare a variable   
quantity = 3;   
is how you assign a value  

- Data Types  

*JavaScript distinguishes between numbers, strings, and true or false values
known as Booleans.*

<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
}

/* Create three equal columns that floats next to each other */
.column {
  float: left;
  width: 33.33%;
  padding: 10px;
  height: 300px; /* Should be removed. Only for demonstration */
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
</style>
</head>
<body>

<h2>Three Different Data Types</h2>

<div class="row">
  <div class="column" style="background-color:#aaa;">
    <h2>Numeric Data Type</h2>
    <p>The numeric data type handles numbers..</p>
  </div>
  <div class="column" style="background-color:#bbb;">
    <h2>String Data Type</h2>
    <p>The strings data type consists of letters and other charaters..</p>
  </div>
  <div class="column" style="background-color:#ccc;">
    <h2>Boolean Data Type</h2>
    <p>Boolean data types can have one of two values: true or false..</p>
  </div>
</div>

</body>
</html>  

- Using a variable to store a number  

var price;  
var quantity;  
var total;  

price = 5;  
quantity = 14;  
total = price * quantity;  

var el = document.getElementById('cost');  
el.textContent = '$' + total;  

- Using a variable to store a string 

var username;  
var message;  
username = 'Kim';  
message = 'See our upcoming range';   

var elName = document.getElementById('name);  
elName.textContent = username;  
var elNote = document.getElementById('note');  
elNote.textContent = message;  

- Using quotes inside a string  

var title;  
var message;  
title ="Kim's Special Offers";  
message = '<a href=\"sale.html\"25% off!</a>';  

var elTitle = document.getElementById('title');  
elTitle.innerHTML = title;  
var elNote = document.getElementById('note');  
elNote.innerHTML = message;  

- Using a variable to store a Boolean  

var inStock;  
var shipping;  
inStock = true;  
shipping = false;  

var elStock = document.getElementById('stock');  
elStock.className = inStock;  

var elShip = document.getElementById('shipping');  
elShip.className = shipping;  






























