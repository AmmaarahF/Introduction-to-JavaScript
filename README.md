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

