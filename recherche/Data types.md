# Recherche-et-Documentation-JavaScript
Recherche et Documentation JavaScript 
<!-- Data Types -->
	
JavaScript has 8 Datatypes

A JavaScript variable can hold 8 types of data:

<!-- String -->
    A text of characters enclosed in quotes
<!-- Number -->
    A number representing a mathematical value
<!-- Bigint -->
    A number representing a large integer
<!-- Boolean -->
	A data type representing true or false
<!-- Object -->
	A collection of key-value pairs of data
<!-- Undefined -->
	A primitive variable with no assigned value
<!-- Null -->
	A primitive value representing object absence
<!-- Symbol -->
	A unique and primitive identifier

    Examples
// Strings
let color = "Yellow";
let lastName = "Johnson";

// Number
let length = 16;
let weight = 7.5;

// BigInt
let x = 1234567890123456789012345n;
let y = BigInt(1234567890123456789012345)

// Boolean
let x = true;
let y = false;

// Object
const person = {firstName:"John", lastName:"Doe"};

// Array object
const cars = ["Saab", "Volvo", "BMW"];

// Date object
const date = new Date("2022-03-25");

// Undefined
let x;
let y;

// Null
let x = null;
let y = null;

// Symbol
const x = Symbol();
const y = Symbol();

<!-- The Concept of Data Types -->
In programming, data types is an important concept.

To be able to operate on variables, it is important to know something about the type.

Without data types, a computer cannot safely solve this:

let x = 16 + "Volvo";

Does it make any sense to add "Volvo" to sixteen? Will it produce an error or will it produce a result?

JavaScript will treat the example above as:

let x = "16" + "Volvo";

<!-- Note -->
When adding a number and a string, JavaScript will treat the number as a string.

let x = 16 + "Volvo";
let x = "Volvo" + 16;

JavaScript evaluates expressions from left to right. Different sequences can produce different results:

let x = 16 + 4 + "Volvo";
Result:
20Volvo

let x = "Volvo" + 16 + 4;
Volvo164

In the first example, JavaScript treats 16 and 4 as numbers, until it reaches "Volvo".

In the second example, since the first operand is a string, all operands are treated as strings.

<!-- JavaScript Types are Dynamic -->
JavaScript has dynamic types. This means that the same variable can be used to hold different data types:

Example:
let x;       // Now x is undefined
x = 5;       // Now x is a Number
x = "John";  // Now x is a String

<!-- JavaScript Strings -->
A string (or a text string) is a series of characters like "John Doe".

Strings are written with quotes. You can use single or double quotes:

Example :
// Using double quotes:
let carName1 = "Volvo XC60";

// Using single quotes:
let carName2 = 'Volvo XC60';

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

Example :
// Single quote inside double quotes:
let answer1 = "It's alright";

// Single quotes inside double quotes:
let answer2 = "He is called 'Johnny'";

// Double quotes inside single quotes:
let answer3 = 'He is called "Johnny"';

<!-- JavaScript Numbers -->
All JavaScript numbers are stored as decimal numbers (floating point).

Numbers can be written with, or without decimals:

Example
// With decimals:
let x1 = 34.00;

// Without decimals:
let x2 = 34;

<!-- Exponential Notation -->
Extra large or extra small numbers can be written with scientific (exponential) notation:
Example
let y = 123e5;    // 12300000
let z = 123e-5;   // 0.00123

<!-- Number Types -->
Most programming languages have many number types:

Whole numbers (integers):
byte (8-bit), short (16-bit), int (32-bit), long (64-bit)

Real numbers (floating-point):
float (32-bit), double (64-bit).

Javascript numbers are always double (64-bit floating point).

<!-- JavaScript Booleans -->
Booleans can only have two values: true or false.
let x = 5;
let y = 5;
let z = 6;
(x == y)       // Returns true
(x == z)       // Returns false

<!-- JavaScript Objects -->
JavaScript Objects represent complex data structures and functionalities beyond the primitive data types (string, number, boolean, null, undefined, symbol, bigint).

JavaScript objects are written with curly braces { }.

JavaScript objects contains a collection of different properties.

Object properties are written as name:value pairs, separated by commas.

Example
Create a person object with 4 properties: firstName, lastName, age and eyeColor:

const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};

Built-In Object Types
A JavaScript object can represent a JavScript object or a User defined object.

<!-- Built-in JavavaScript object types can be: -->

Object	The fundamental building block for complex data

Array	Object of values accessed by a numerical index

Date	Object for working with dates and times

RegExp	Object for working with regular expressions

Map	Object of key-value pairs where the keys can be of any data type

Set	Object of values where each value can only appear once

Error	Object represents error conditions during program execution

Promise	Object representing the completion or 
failure of an asynchronous operation

Int8Array	Array for storing fixed-size 8-bits integer values

Int16Array	Array for storing fixed-size 16-bits integer values

Int32Array	Array for storing fixed-size 32-bits integer values

Float16Array	Array for storing fixed-size 16-bits floating-point values

Float32Array	Array for storing fixed-size 32-bits floating-point values

Float64Array	Array for storing fixed-size 64-bits floating-point values

BigInt64Array	Array for storing fixed-size 64-bits big integer values


<!-- Note -->
The list above is not complete, as JavaScript offers other built-in object types like Math for mathematic methods and values, and various other specialized objects for specific tasks.The list above is not complete, as JavaScript offers other built-in object types like Math for mathematic methods and values, and various other specialized objects for specific tasks.

<!-- The typeof Operator -->
You can use the JavaScript typeof operator to find the type of a JavaScript variable.

The typeof operator returns the type of a variable or an expression:

typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"

<!-- JavaScript Arrays -->
JavaScript arrays are a special type of JavaScript objects.

JavaScript arrays are written with square [ ] brackets.

Array items are separated by commas.

The following code declares (creates) an array called cars, containing three items (car names):

Example
const cars = ["Saab", "Volvo", "BMW"];

Array indexes are zero-based, which means the first item is [0], second is [1], and so on.

<!-- Undefined -->
In JavaScript, a variable without a value, has the value undefined. The type is also undefined.

Example
let car;    // Value is undefined, type is undefined

Any variable can be emptied, by setting the value to undefined. The type will also be undefined.

<!-- Empty Values -->
An empty value has nothing to do with undefined.

An empty string has both a legal value and a type.

let car = "";    // The value is "", the typeof is "string"

<!-- Datatype null -->
In JavaScript, a variable or an expression can obtain the datatype null in several ways.

A function can return null or a variable can be assigned the null value:

let carName = null;


<!-- Note -->
The typeof operator returns object for null.

This is a historical quirk in JavaScript and does not indicate that null is an object.

=================================================

The strict equality operator (===) compares both the value and the type of the operands.

It returns true only if both the operands values and types are null.

The loose equality operator (==) also returns true for a null value, but it also returns true if the value is undefined.

Using == is not recommended when checking for null.