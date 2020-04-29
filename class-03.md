# HTML Lists, CSS Boxes, JS Control Flow  

# Lists  
  Numbered, Bullet & Definition lists  
  
  *<b>Ordered Lists</b> are lists where each item in the list is numbered.*  
  Example 
  <ol>  
    <li>open door</li>  
    <li>step outside</li>  
    <li>shut door</li>  
  </ol>  
  
  *<b>Unordered Lists</b> are lists that begin with a bullet point.*
  Example  
  <ul>
    <li>step outside</li>
    <li>open door</li>
    <li>shut door</li>
  </ul>
  
  *<b>Definition Lists</b> are made up of a set of terms along with the definition
  for each of those terms.*      
  Example  
  <dl>
    <dt>sashimi</dt>
    <dd>is sliced raw fish that is served with condiments</dd>  
    <dt>scale</dt>  
    <dd>a device used to accurately measure the weight of ingredients</dd>  
  </dl>  
  
  *<b>Nested Lists</b> can be used inside the list element to create a sublist
  or nested list.*    
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

# <b>Box Dimensions</b> (width, height)  
_By default a box is sized just big enough to hold it's contents. Toset your own dimensions 
for a box you can use the height and width properties._

div {
  <p>The Moog company pioneered the commercial manufactor of modular voltage-controlled analog
    synthesizer systems in the early 1950s.</p>
</div>  

div {
    height: 300px;  
    width: 400px;  
    background-color: #ee3e80:}

The box-sizing property allows us to include the padding and border in an element's total width and height.

If you set box-sizing: border-box; on an element, padding and border are included in the width and height:

# <b>Limiting Width</b> (min-width, max-width)  
*Some page designs expand and shrink to fit the size of the users screen. In such designs the min-width
properties specifies the smallest size a box can be displayed at when the browser window is narrow, and 
the mzx-width properties indicates a maximun width a box can stretch to when the browser window is wide.*  



# Decisions & Loops  




