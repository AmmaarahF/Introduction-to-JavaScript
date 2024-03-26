# Introduction-to-JavaScript

What is JavaScript ? 
-------------------------
JavaScript is a high-level programming language primarily used for creating interactive effects within web browsers. (Only language understood by the web browser)

What is it used for ?
-------------------------
It's commonly used for adding functionality to web pages, building web applications, developing server-side applications.

JavaScript allows you to work with three primitive data types:- 
> Numbers - 123, 120.50, etc
> String - "text"
> Boolean - true or false

- JavaScript also defines two trivial data types, <b>null</b> and <b>undefined</b>
- JavaScript supports a composite data type known as an <b>object</b>.
- JavaScript does not make a distinction between integer values and floating-point values.
- JavaScript represents numbers using the 64-bit floating-point format defined by the IEEE 754 standard.


 JavaScript Variables
 -------------------------
 
 - Before you use a variable in a JavaScript program, you must declare it.
 - Variables can be declared with the <b>var</b> keyword , eg. var money; 
 - You can also declare multiple variables with the same var keyword, eg. var money, name;
 - Storing a value in a variable is called variable <b>initialization</b>.
 - You can assign a value at the time of initialization. Eg, var money; and then 'money = 200.50;' below that
 - JavaScript can also be declared with <b>let</b> and <b>const</b>.
 - var is globally scoped or locally-scoped, let is blocked-scoped and be changed, and const is block-scoped and connot be reassigned.
   

 Strings
 ---------------------------
 - Use single quotes ' ' to use double quotes in a string.
 - Use backslash (\) when using "I'm" like "I'\m"

- Using .length to find out how many characters there are in a string. Such as <b>console.log(myStringName.length);</b>
- Using .toUpperCase() to make the characters all in Caps. Such as <b>console.log(myStringName.toUpperCase());</b>
- Using .toLowerCase() to make the characters all in small caps. Such as </b>console.log(myStringName.toLowerCase());</b>
- Using .indexOf() to search for the specific word you put between the brackets, such as <b>console.log(myStringName.indexOf("something"));</b>

Arrays
-----------------------------
> let arr = new Array();
> let arr = [];
> let Fruits = ["Apple", "orange", "Plum"];
- Array elements are numbered from 0
- to display the element
  > alert(fruits[0]);//Apple
- to replace an element
  > fruits[2] = 'Pear'; // Plum is now Pear

Ways to manipulate arrays
-----------------------------
- push() - adds an element at the end of the array
- pop() - removes an element at the end of the array
- shift() - removes an element at the beginning of the array
- unshift() - adds an element at the beginning of the array 


Functions
---------------------------
- Functions in JavaScript are blocks of code that perform specific tasks. They can be reused multiple times and accept inputs called parameters. They often return a result.
- Functions in JavaScript can also be assigned to variables, passed as arguments to other functions, and returned from other functions, enabling powerful and flexible programming patterns such as callbacks, higher-order functions, and closures.
-------------
Example
-------------
// Function assigned to a variable<br>
const add = function(a, b) {<br>
  return a + b;<br>
};
<br>
// Function passed as an argument<br>
function operate(num1, num2, operation) {<br>
  return operation(num1, num2);<br>
}<br>
<br>
// Using the operate function with the add function<br>
const result = operate(5, 3, add);<br>
console.log(result); // Output: 8<br>
<br>
// Function returning another function<br>
function createMultiplier(factor) {<br>
  return function(num) {<br>
    return num * factor;<br>
  };<br>
}<br>
<br>
const double = createMultiplier(2);<br>
console.log(double(5)); // Output: 10<br>


Booleans
------------------------------
- is a data type representing true or false values. They often used in conditional statementments, comparison and logical operators.
- Conditional statements like if, else if, and else evaluate expressions that result in boolean values, determining the flow of program execution based on whether those expressions evaluate to true or false. Additionally, boolean values are commonly used in logical operations such as AND (&&), OR (||), and NOT (!). Understanding how to use booleans effectively in conditionals and logical operations is fundamental for writing robust JavaScript code.
- Booleans are also used as flags to control program behavior and to represent the state of conditions or switches within your code.
  
  Example
  --------------------

let isRaining = true; // Boolean variable representing whether it's raining or not <br>

if (isRaining) {<br>
  console.log("Remember to bring an umbrella!");<br>
} else {<br>
  console.log("No need for an umbrella today.");<br>
}<br>


Type Conversions
-------------------------
String Conversion
-------------------
- string conversion happens when we need the string form of a value
- alert(value) shows the value
- call String(value) function to concert a value to a string
  > eg. let value = true;<br>
    alert(typeofvalue);// boolean<br>
    value = String(value);

Example
------------------
A false become "false", null becomes "null", etc

<br>

Numeric Conversion
--------------------------
- Numeric conversion happens in math functions and expressions automatically

Example
---------------
When division is applied to non-number: <br>
alert("6"/"2");//3
<br>


To explicitly convert a value to a number: <br>

Example
-----------
let str = "123";<br>
alert(typeofstr);//String<br>
let num = Number(str); //123<br>
alert(typeofnum); //number<br>
<br>

- if the string is not a value number, the result of such a conversion is NaN.//conversion failed
<br>

Number conversion rules:
----------------------------
undefined = NaN<br>
null = 0 <br>
true or false = 1 and 0<br>
String = NaN<br>

Example
--------------
alert(Number("123"));//123 <br>
alert(Number("123z"));//NaN <br>
alert(Number(true));//1 <br>
alert(Number(false));//2 <br>

Boolean Conversion
---------------------------------
Conversion rule:
- Values that are intuitively "empty" like ) or an empty string an empty string, null, undefined, and NaN, become false.
- other values become true

Example
--------------------------
alert(Boolean(0));// false<br>
alert(Boolean("hello"));//true<br>
alert(Boolean("")); // false<br>
alert(Boolean("0"));// true<br>


The Document Object Model Revisited
---------------------------------------------------
The Document Object Model and JavaScript Syntax
------------------------------------------------------
- The Document Object Model is an Application Programming Interface (API) for HTML and XML documents.
- it provides a structural representation of the document
- it defines the way that that structure is to be accessed from script
 > This allows you to get at the web page as a structured group of nodes. Essentially, it connects web pages to scripts or programming languages.
- The JavaScript syntax has to do with objects.
-  To access an object, property, or method, its reference must include every object that contains it, separated by a dot. This is called the <b>"dot syntax".</b>

<b>OBJECT</b>
- In JavaScript, objects can be either scriptable HTML elements within a webpage or core objects that are not tied to HTML elements but are part of the language itself. Additionally, homemade objects can be created by developers. Both core and homemade objects are part of the JavaScript Object Model.<br>
The following are some of the JavaScript objects:<br>
- window
- document
- form
- image

<b>PROPERTY</b>
- In JavaScript, objects have properties, similar to HTML tag attributes, representing their characteristics. However, unlike HTML attributes, JavaScript properties can also be objects themselves. This means they can have their own properties and methods. For example, a document, form, or image, while properties of other objects like the window or document, are also considered objects themselves. It's important to recognize these dual identities and treat them as objects to understand their capabilities fully.
<br>

<b>Method</b>
- In web development, methods are actions that directly affect objects, such as HTML documents. These actions enable dynamic interactions with users, creating a meaningful and engaging experience that would otherwise be static and one-sided.
<br>
Method Parameters<br>
- Methods in JavaScript are indicated by parentheses immediately following their name, such as "alert()". These parentheses may contain parameters, which are necessary for the method to perform its task. Parameters provide information to the method. For example, the alert() method displays an alert box. Without a parameter, the alert method would produce a meaningless dialog box. However, with a parameter like alert("Hello World"), it communicates a specific message to the user.

Here are a Few JavaScript Methods:

- alert() causes an alert dialog box to appear over the page that launched it
- write() writes content to a page
- focus() causes the mouse cursor to be inserted into a form element

Core APIs in the DOM
-------------------------------------
- document and window objects are the objects whose interfaces you generally use most often in DOM programming.
- the window object represents something like the browser, and the document object is the root of the document itself.
- The following is a brief list of common APIs in web and XML page scripting using the DOM.

> document.getElementById(id)<br>
> document.getElementsByTagName(name)<br>
> document.createElement(name)<br>
> parentNode.appendChild(node)<br>
> element.innerHTML<br>
> element.style.left<br>
> element.setAttribute<br>
> element.getAttribute<br>
> element.addEventListener<br>
> window._content<br>
> window.onload<br>
> window.dump()<br>
> window.scrollTo()<br>
<br>

JavaScript Function
-------------------------
- A function is a subprogram designed to perform a particular task.
- A function will only execute if and only when it has been called (invoking a function).
- Values can be passed into functions and used within that function as well.
- All functions have a return value, otherwise they become undefined
- function is an <b>object (an HTML element, with properties and methods.</b>
<br>
<b>Calling one function from another function</b><br>
<br>
- Functions in JavaScript can be nested, meaning you can call one function from within another. This allows you to create separate functions, each performing a specific task, and then run them together as a complete process, one after the other. For instance, you can have a function that calls three other functions, each returning a string of text that has been altered in some way.
<br>
<br>
<b>Creating objects with user-defined functions</b><br>
<br>
- JavaScript is object-based, with elements like the window, links, forms, and the browser itself treated as objects. Utilizing objects can simplify programming tasks. You can create custom objects in JavaScript by using functions in a modified way, offering flexibility and organization to your code.<br>
<br>
Making a new object entails two steps:-<br>
- Define the object in a user-defined function
- Use the new keyword to create the object with a call to the object function<br>
<br>
 <b> Example of the world's simplest user-defined JavaScript object:</b><br>

 ret = new makeSimpleObject(); //creates the new object <br>

 function makeSimpleObject() {} // this part defines the object<br>
<br>
You can use the same object function to create any number of new objects. For instance, these lines create four new and separate objects: eenie, meenie, minie, and moe:<br>
eenie = new makeSimpleObject();<br>
meenie = new makeSimpleObject(); <br>
...and so on<br>

<br>
<b>Defining new properties to already-made objects</b><br>
- After an object has been created you can assign a value to it.<br>
- To create a new property and assign a value to it, simply write a variable expression like this:-<br>
<br>
myobject.property = value; <br>
- myobject is the name of the user-defined object.<br>
- property is the name of the property you want to create.<br>
- value is the value you want to assign.<br>
<br>
<br>
- Suppose you create an object called "customer" and you want to define three properties to it: name, address, and phone. Here's one way to do it:-<br>
customer = new makeSimpleObject();<br>
customer.name = "Fred";<br>
customer.address = "123 Main Street";<br>
customer.phone = "555-1212";<br>
<br>
function makeSimpleObject(){<br>
  return(this);<br>
}<br>
To call: <br>
alert(customer.name);<br>
<br>

Operators
----------------------
- Assignment operators<br>
- Comparison operators<br>
- Arithmetic operators<br>
- Bitwise operators<br>
- Logical operators<br>
- String operators<br>
- Conditional (ternary) operator<br>
- Comma operator<br>
- Unary operators<br>
- Relational operators<br>
<br>

Assignment Operators
-------------------------------
<b>Return value and chaining</b><br>
- An assignment operator assigns a value to its left operand based on the value of its right operand.<br>
- The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand. <br>

Comparison Operators 
--------------------------------
- JavaScript comparison operators compare operands and return a logical value based on the comparison's truth.
-  Operands can be numeric, string, logical, or object values. Strings are compared based on lexicographical ordering using Unicode values.
-  JavaScript usually converts operands to compatible types for comparison, except for === and !== operators, which perform strict equality checks without type conversion.
<br>
Arithmetic operators
---------------------------------
- An arithmetic operator takes numerical values (either literals or variables) as their operands and returns a single numerical value.
- The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/).
<br>

Bitwise Operators
---------------------------------
- A bitwise operator treats their operands as a set of 32 bits (zeros and ones), rather than as decimal, hexadecimal, or octal numbers.
- Bitwise operators perform their operations on such binary representations, but they return standard JavaScript numerical values.
  <br>
  
Bitwise AND - a&b //Returns a one in each bit position for which the corresponding bits of both operands are ones. <br>

Bitwise OR - a|b // Returns a zero in each bit position for which the corresponding bits of both operands are zeros. <br>

Bitwise XOR - a ^ b// Returns a zero in each bit position for which the corresponding bits are the same. 
[Returns a one in each bit position for which the corresponding bits are different.]
<br>

Bitwise NOT - ~a // Inverts the bits of its operand.
<br>

Left shift - a >>> b //Shifts a in binary representation b bits to the right, discarding bits shifted off. 
<br>

Zero-fill right shift - a >>> b // Shifts a in binary representation b bits to the right, discarding bits shifted off, and shifting in zeros from the left. 


The Document Object Model
---------------------------------------
<b>Event Bubbling</b>

- Bubbling is what the event itself does.
- The event starts at the element that triggered it (Clicking 1. Element button, An Event Listener would be attached to each element).
- Then, it bubbles up to each of it’s parent elements until it reaches the document
-  Any listeners on any of those parent elements would get triggered as it bubbles up.
-  Causing all the events to occur on the page possibly slowing down your application.
-  That e.stopPropagation() halts this “bubbling” of events “up” through the DOM. We stop all the events from the parents occurring. 


Regular Expressions
--------------------------------------
- A regular expression is a sequence of characters that forms a search pattern.
- When you search for data in a text, you can use this search pattern to describe what you are searching for.
- A regular expression can be a single character, or a more complicated pattern.
- Regular expressions can be used to perform all types of text search and text replace operations.

Example 
var patt = /w3schools/i; 

Example explained: 

/w3schools/i  is a regular expression. 

w3schools  is a pattern (to be used in a search). 

i  is a modifier (modifies the search to be case-insensitive). 

Week 3
--------------------
Strings Operations
------------------
Creating strings
------------------
- Strings can be created as primitives, from string literals, or as objects, using the String() constructor: <br>
eg. const string = "A string primitive"; <br>
const string2 = "new String("A String object");
<br>
- String primitives and string objects can be used interchangeably in most situations.
- String literals can be specified using single or double quotes, which are treated identically, or using the backtick character ` .
  >  This last form specifies a template literal: with this form you can interpolate expressions.
<br>
- There are two ways to access an individual character in a string. The first is the charAt() method:<br>
>  return 'cat'.charAt(1) // returns "a"

- The other way is to treat the string as an array-like object, where individual characters correspond to a numerical index: <br>
> return 'cat'[1] //returns "a"

- When using bracket notation for character access, attempting to delete or assign a value to these properties will not succeed.

-In C, the strcmp() function is used for comparing strings. In JavaScript, you just use the less-than and greater-than operators: <br>
> let a = 'a' <br>
  let b = 'b' <br>

> if (a<b) { //true <br>
    console.log(a + ' is less than ' + b)}<br>
    else if (a > b) { console.log(a + ' is greater than ' + b)}<br>
    else{ console.log(a + 'and' + b + ' are equal.')}
<br> 

- A similar result can be achieved using the localeCompare() method inherited by String instances.
- Note that a == b compares the strings in a and b for being equal in the usual case-sensitive way.
- To compare without regard to upper or lower case characters, use a function similar to this: <br>
> function isEqual(str1, str2){
  return str1.toUpperCase() === str2.toUpperCase()} //isEqual
 <br>
- JavaScript distinguishes between String objects and primitive string values, similarly for Booleans and Numbers.
  
- String literals (enclosed in double or single quotes) and strings returned from String calls in a non-constructor context are considered primitive strings.
  
- JavaScript automatically converts primitives to String objects, enabling the use of String object methods for primitive strings.
  
- In contexts where a method is invoked on a primitive string or a property lookup occurs, JavaScript automatically wraps the string primitive and performs the method call or property lookup.
> eg. let s_prim = 'foo'<br>
      let s_obj = new String(s_prim)<br>
      console.log(typeof s_prim) // logs "string"console.log(typeof s_obj) // logs"object"


- String primitives and String objects also give different results when using eval().
- Primitives passed to eval are treated as source code; String objects are treated as all other objects are, by returning the object.
  > eg. let s1 = '2 + 2' //creates a string primitive <br>
  > let s2 = new String('2 + 2') //creates a String object  <br>
  > console.log(eval(s1)) //returns the number 4 <br>
  > console.log(eval(s2)) //returns the string "2 + 2" <br>

- For these reasons, the code may break when it encounters String objects when it expects a primitive string instead
-  A String object can always be converted to its primitive counterpart with the valueOf() method.
  > eg. console.log(eval(s2.valueOf())) //returns the number 4
  


On-event Handlers
------------------------------
- DOM elements offer on-event handlers to manage how they react to events.
- Events can include actions like clicking, key presses, focus changes, etc.
- Elements can be interactive (e.g., links, buttons, forms) or non-interactive (e.g., the base document).
- The on-event handler is typically named according to the event it's designed to react to, such as onclick, onkeypress, onfocus, etc.

You can specify an on<...> event handler for a particular event (such as click) for a given object in different ways:

- Using an HTML attribute named on{eventtype} on an element, for example:
<button onclick="return handleClick(event);">,
- Or by setting the corresponding property from JavaScript, for example:
document.getElementById("mybutton").onclick = function(event) { ... }.

- Each object can have only one on-event handler for a specific event, although this handler can call multiple sub-handlers.
- addEventListener() is often preferred for event handling as it allows multiple event handlers to be applied independently for the same event and/or element.
- on-event handlers are automatically called, not at the programmer's discretion, although they can be invoked directly using syntax like mybutton.onclick(myevent);.
- on-event handlers serve as placeholders to which real handler functions can be assigned.

Event handler’s parameters, this binding, and the return value
--------------------------------------------------------------------------
When the event handler is specified as an HTML attribute, the specified code is wrapped into a function with the following parameters:- <br>

- event - for all event handlers, except onerror.
- event, source, lineno, colno, and error for the onerror event handler.

> Note that the event parameter actually contains the error message as a string.

- When an event handler is invoked, the `this` keyword inside the handler refers to the DOM element on which the handler is registered.
  
- The return value from the handler determines whether the event is cancelled.
  
- The handling of the return value depends on the type of event, with detailed specifications outlined in "The event handler processing algorithm" in the HTML specification.

The term event handler may be used to refer to:- <br>

- any function or object registered to be notified of events,
- or, more specifically, to the mechanism of registering event listeners via on... attributes in HTML or properties in web APIs, such as <button onclick="alert(this)"> or window.onload = function() { /* ... */ }.

- the EventTarget method addEventListener() sets up a function that will be called whenever the specified event is delivered to the target.
- Common targets include Element, Document, and Window, but any object supporting events can be a target.
- addEventListener() operates by appending a function or an object implementing EventListener to the list of event listeners for the specified event type on the EventTarget where it's invoked.
<br>

> target.addEventListener(type, listener[, options]);


> target.addEventListener(type, listener[, useCapture]);


Event handlers specific rules
--------------------------------------------
- Certain event handler attributes have specific rules: -
- They must be supported by all HTML elements except for body and frameset elements.
- These attributes function both as event handler content attributes and event handler IDL attributes.
- They must be supported by all Document objects solely as event handler IDL attributes.
- They must be supported by all Window objects as event handler IDL attributes directly on the Window objects themselves.
- Corresponding event handler content attributes and event handler IDL attributes are exposed on all body and frameset elements owned by the Window object's Documents.

Event Handlers for All HTML5 Elements & document & window Objects
---------------------------------------------------------------------
- onclick - Invoked when the user clicked on the object.<br>
- onabort - Invoked when an event has been aborted.
- oninvalid - invalid event handler.
- onshow - 	show event handler.


Dynamic HTML
-------------------------
- Dynamic HTML (DHTML) involves combining CSS and JavaScript with HTML to create dynamic web pages.
- Events drive changes to website features, ranging from simple text font, color, and style alterations to dynamically altering page content and moving objects around the page.
- CSS facilitates the styling and layout aspects of the page, allowing for visual enhancements and modifications.
- JavaScript adds interactivity and dynamic behavior to the webpage, enabling responses to user actions and events.
- Through DHTML, web pages can evolve dynamically, providing richer and more engaging user experiences.

HTML objects can be changed in two ways:-

- Changing the class of the object - thereby changing the style of the object
- Using the style property of the object to change the style.


JavaScript functions can be designed in various ways:- 

- Directly referencing an object in the function using its id value. This allows for changing the style of only that specific object.
- Passing an object id as an argument to the JavaScript function, enabling the style of any object to be changed.
- Accessing an object using the event to determine the object in which the event occurred, allowing for dynamic handling based on user interaction.


Date Object
------------------
- The Date object is a built-in object in JavaScript that stores the date and time.
- It provides a number of built-in methods for formatting and managing that data.
- When instantiated without arguments, a new Date instance represents the current date and time.
- The current date and time are determined by the computer's system settings.
- The Date object created reflects the current system's date and time accurately.
- This default behavior allows easy access to the current date and time within JavaScript applications.

> const now = new Date(); // Wed Oct 18 2017 12:41:34 GMT+0000 (UTC)

- <b>Epoch time</b>, or zero time, refers to the date string "01 January, 1970 00:00:00 Universal Time (UTC)" and is represented by the timestamp 0.
- In JavaScript, we can test epoch time by creating a new variable and assigning it a Date instance based on a timestamp of 0.
- This Date instance represents the epoch time and serves as a reference point for measuring time intervals in JavaScript.
- The epoch time concept is widely used in computing for representing and calculating time durations, especially in systems that utilize Unix time.

- We can use these set methods to modify one, more, or all of the components of a date.

Keyboard Events
--------------------------
Here are some of the most important keyboard events and their event handler:-

Keydown Event (onkeydown):

- Occurs when a user presses down a key on the keyboard.
- Handled with the onkeydown event handler.
- Example: Displays an alert message when the keydown event occurs.

Keyup Event (onkeyup):

- Occurs when a user releases a key on the keyboard.
- Handled with the onkeyup event handler.
- Example: Displays an alert message when the keyup event occurs.

Keypress Event (onkeypress):

- Occurs when a user presses down a key on the keyboard that has a character value associated with it.
- Certain keys like Ctrl, Shift, Alt, Esc, Arrow keys, etc., do not generate a keypress event but generate keydown and keyup events.
- Handled with the onkeypress event handler.
- Example: Displays an alert message when the keypress event occurs.


Form Events
--------------------
- A form event is fired when a form control receives or loses focus or when the user modify a form control value, such as by typing text in a text input, select any option in a select box etc.


Here are some of the most important form events and their event handlers- 

Focus Event (onfocus):

- Occurs when a user gives focus to an element on a web page.
- Handled with the onfocus event handler.
- Example: Highlights the background of a text input in yellow color when it receives focus.

  
Blur Event (onblur):

- Occurs when the user takes focus away from a form element or window.
- Handled with the onblur event handler.
- Example: Displays an alert message when a text input element loses focus.
  
Change Event (onchange):

- Occurs when a user changes the value of a form element.
- Handled with the onchange event handler.
- Example: Displays an alert message when an option in a select box is changed.
  
Submit Event (onsubmit):

- Occurs only when the user submits a form on a web page.
- Handled with the onsubmit event handler.
- Example: Displays an alert message while submitting the form to the server.






Document/Window Events
---------------------------------
- Events are also triggered in situations when the page has loaded or when the user resizes the browser window, etc. 


Here are some of the most important document/window events and their event handlers:-


Load Event (onload):

- Occurs when a web page finishes loading in the browser.
- Handler: onload event handler.
- Example: Alert message displayed upon page load completion.

Unload Event (onunload):

- Occurs when a user leaves the current web page.
- Handler: onunload event handler.
- Example: Alert message triggered when attempting to leave the page.


Resize Event (onresize):

- Occurs when the browser window is resized, including minimization or maximization.
- Handler: onresize event handler.
- Example: Alert message displayed upon resizing the browser window to a new width and height.


Creating an Image Slider
---------------------------------

eg . code in javaScript on how to create a slideshow 

let slideIndex = 0;
showSlides();

function showSlides() {
  let slides = document.getElementsByClassName("slide");
  for (let i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  slideIndex++;
  if (slideIndex > slides.length) {
    slideIndex = 1;
  }
  slides[slideIndex - 1].style.display = "block";
  setTimeout(showSlides, 2000); // Change image every 2 seconds
}

function nextSlide() {
  slideIndex++;
  showSlides();
}

function prevSlide() {
  slideIndex--;
  showSlides();
}




Program Flowcharts
---------------------------
Purpose of Program Flowchart:

- Illustrates the logic of a program.
- Provides details on manipulating data.
- Helps in understanding and designing the program's structure.

Design Process:

- Occurs after analyzing a problem or opportunity.
- Results in the creation of a program flowchart.
  
Benefits:

- Facilitates determining, arranging, and rearranging complex logic.
- Helps in identifying errors and correcting them before implementation.
- Aids in easy and efficient maintenance of the program.
- Essential for making modifications to the program.

Cost-effectiveness:

- It is less costly to determine, arrange, and rearrange complex logic on a flowchart than to correct logic errors in an implemented program.


Javascript For Loop
----------------------------
Loops can execute a block of code a number of times and are handy if you want to run the same code over and over again, each time with a different value.

Often this is the case when working with arrays:

Instead of writing:
text += cars[0] + " 1 ";

text += cars[1] + " 1 ";

text += cars[2] + " 1 ";

text += cars[3] + " 1 ";

text += cars[4] + " 1 ";

text += cars[5] + " 1 ";

You can write:
var i;

for (i = 0; i < cars.length; i++) {

  text += cars[i] + " 1 ";

} 

JavaScript supports different kinds of loops:

- for - loops through a block of code a number of times
- for/in - loops through the properties of an object
- for/of - loops through the values of an iterable object 
- while - loops through a block of code while a specified condition is true
- do/while - also loops through a block of code while a specified condition is true
