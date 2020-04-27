  # HTML Text, CSS Intro & Basic JS Instructions        


 # Text  
- Headings and Paragraphs    
  
<h1></h1>  
*Is used for main headings*  
<h2></h2>  
*Is used for subheadings*  
<h3></h3>
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

- Shorthand for creating variables  

1.   var price = 5;  
     var quantity = 14;  
     var total = price * quantity;  

2.   var price = quantity, total;  
     price = 5;  
     quantity = 14;  
     total = price * quantity;  
     
3.   var price = 5, quantity = 14;  
     var total = price * quantity;    
     
 - Chaging the Value of a Variable  
 
 - Rule for Naming Variable  
 
 *There are sic rules you must always follow when giving a variable a name*  
 
 1. The name must begin with a letter, dollar sign ($), or an underscore (_).  
    It must <b>Not</b> start with a number.  
    
 2. The name can contain letters, numbers, dollar sign ($), or an underscore (_).  
    Note that you must not use a dash(-) or a period(.) in a variable name.  
    
3. You cannot use <b>Keywords</b> or <>reserved</b> words. Keywords are special  
   words that tell the interpreter to do something. For example, var is a keyword  
   used to declare a variable. Reserved words are ones that may be used in a *future*  
   version of JavaScript.  
   
4. All variables are case sensitive, so score and Score would be different variable  
   names, but it is bad practice to create two variables that have the same name  
   using different cases.  
   
5. Use a name that describes the kind of information that the variable stores.  
   For example, firstName might be used to store a person's first name, lastName  
   for their last name, and age for their age.  
   
6. If your variable name is made up of more than one word, use a capitol letter  
   for the first name of every word *after* the first word. For example, firstName  
   rather than firstname (this is referred to as camel case). You can also use an  
   underscore between each word (you cannot use a dash).    
   
- Arrays  

   *An Array is a special type of variable. It doesn't just store one value; it stores a list of values.*  
 
- Creating an Array  

colors = ['white';  
         'black'  
         'custom'];  
         
- Values in an Array  

*Values in an array are accessed as if they are in a numbered list. It is important to know that the
numbering of this list starts at zero (not one).*  

- Accessing & Changing Values in an Array  

*To access a value from an array, after the array name you specify the index number for that value
 inside square brackets. You can change the value of an item an array by selecting it and assigning
 it a new value just as you would any other variable (using the equals sign and the new value for that item).*  
 
 - Expressions  
 
 *An <b>expression</b> evaluates into (results in) a single value. Broadly speaking there are two types of expressions.*
 
 1. Expressions that just assign a value to a variable  
        
        var color = 'beige';  
        The value of color is now beige  
        
2. Expressions that use two or more values to return a single value  

        var area = 3 * 2;  
        The value of area is now six  
        
  - Operators  
  
  *Expressions rely on things called <b>operators</b>; they allow programmers to create a single vallue 
  from one or more values.*  

<table>
  <tr>
    <th>Operators</th>
    <th>What They Do</th>
  </tr>
  <tr>
    <td>Assignment</td>  
    <td>Assigns a value to a variable</td>   
  </tr>
  <tr>
    <td>Arithmetic</td>
    <td>Performs basic math</td>
  </tr>
  <tr>
    <td>String Operators</td>
    <td>Combine two strings</td>
  </tr>
  <tr>
    <td>Comparison Operators</td>
    <td>Compare two values and return true or false</td>
  </tr>
  <tr>
    <td>Logical Operators</td>
    <td>Combine expressions and return true or false</td>
  </tr>  
  
</table>  





  
      
 


