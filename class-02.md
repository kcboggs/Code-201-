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











