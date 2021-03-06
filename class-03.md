# HTML Lists, CSS Boxes, JS Control Flow  

# Lists  
  Numbered, Bullet & Definition lists  
  
  - <b>Ordered Lists</b> are lists where each item in the list is numbered.  
  Example 
  <ol>  
    <li>open door</li>  
    <li>step outside</li>  
    <li>shut door</li>  
  </ol>  
  
  - <b>Unordered Lists</b> are lists that begin with a bullet point.
  Example  
  <ul>
    <li>step outside</li>
    <li>open door</li>
    <li>shut door</li>
  </ul>
  
  - <b>Definition Lists</b> are made up of a set of terms along with the definition
  for each of those terms.      
  Example  
  <dl>
    <dt>sashimi</dt>
    <dd>is sliced raw fish that is served with condiments</dd>  
    <dt>scale</dt>  
    <dd>a device used to accurately measure the weight of ingredients</dd>  
  </dl>  
  
  - <b>Nested Lists</b> can be used inside the list element to create a sublist
  or nested list.    
   Example    
  <ul>
    <li>mousses</li>
    <li>pastries  
      <ul>  
        <li>croissant</li>  
        <li>mille-feuille</li>  
      </ul>  
    </li>  
  </ul>  
  
# Boxes  
Controlling size of boxes, Box models for borders, margin & padding & 
Displaying and hiding boxes  

- <b>Box Dimensions</b> (width, height)  
_By default a box is sized just big enough to hold it's contents. Toset your own dimensions 
for a box you can use the height and width properties._

div>    
  <p>The Moog company pioneered the commercial manufactor of modular voltage-controlled analog
    synthesizer systems in the early 1950s.</p>
</div>  

div {
    height: 300px;  
    width: 400px;  
    background-color: #ee3e80:}

The box-sizing property allows us to include the padding and border in an element's total width and height.

If you set box-sizing: border-box; on an element, padding and border are included in the width and height:

- <b>Limiting Width</b> (min-width, max-width)  
*Some page designs expand and shrink to fit the size of the users screen. In such designs the min-width
properties specifies the smallest size a box can be displayed at when the browser window is narrow, and 
the mzx-width properties indicates a maximun width a box can stretch to when the browser window is wide.*  

td.description {  
    min-width: 450px;  
    max-width: 650px;  
    tex-align: left;  
    padding: 5px;  
    margin: 0px;}    
   
 - <b>Limiting Height</b> (min-height, max-height)  
 *The min-height property defines the minimum height of an element.
If the content is smaller than the minimum height, the minimum height will be applied.
If the content is larger than the minimum height, the min-height property has no effect.*  

p {
  width: 400px;  
  font-size: 90%;  
  line-height: 1.2em;)  
  {

- <b>Overflowing Content</b>  
*The overflow property tells the browser what to do if the content contained within the box  
is larger than the box itself. It can have one of two values.*  

1. <b>Hidden,</b>    
  *This property hides any content that does not fit in the box*  
  p. one {  
    overflow: hidden;}  
2. <b>Scroll</b>    
  *This property adds a scroll bar to the box.*  
  p.two {  
    overflow: scroll;}  
  
# Border, Margin & Padding  
*Every box has three avaiable properties that can be adjusted to control its appearance.*  

1. Border  
2. Margin  
3. Padding  

# White Spacing  
*The padding and margin properties are very helpful in adding space between various items on the page.*  

#Border Width  
*The border-width property is used to control the width of the property. The value of this property can either
be given in pixels or using one of the following values.*  

thin  
thick  
medium  

p. one {
  border-width: 2px;}  
p. two {  
  border-width: thick;}  
p. three {  
  border-width: 1px 4px 12px 4px;}  
  
# Border Style  
*You can control the style of a border using the border-style property. The property can take the
following values.*  

1. solid   *a single solid line*
2. dotted  *a series of square dots*
3. dashed  *a series of short lines*  
4. double  *two solid lines*  
5. groove  *appears to be carved into the page*  
6. ridge   *appears to stick out from the page*  
7. inset   *appears embedded into the page*  
8. outset  *looks like it is coming out of the screen*  
9. hidden/non  *no border is shown*    

You can individually change the styles of different borders by using:  

border-top-style  
border-left-style  
border-right-style  
border-bottom-style  
 
# Padding    
 *Padding property allows you to specify how much space should appear between the content of an element and 
 its border*  

# Margin  
*Margin property controls the gap between boxes. Its value is commonly given in pixels, although you may also
percentage or ems*  

# Decissions and Loops  

- Conditional statements allow your code to make decisions about what to do next.  
- Comparison operators (===, !==, ==, !=, <, >, <=, =>)  
- Logical operators allow you to combine more than one set of comparison operators.  
- if...else statements allow you to run one set of code if a condition is true, and another if it is false.  
- Switch statements allow you to compare a value against possible outcomes (and also provides a default option
if none match).  
- Data types can be coerced from one type to another.  
- All values evaluate to either truthy or falsy.  
- There are three types of loops and each repeats a set of statements:  
1. for  
2. while  
3. do...while  

Jon Duckett http://www.htmlandcssbook.com/  
    
    
         




