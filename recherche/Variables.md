# Recherche-et-Documentation-JavaScript
Recherche et Documentation JavaScript 
<!-- Variables = Data Containers -->

Older JavaScript :
Using var (Not Recommended)
Automatically (Not Recommended)

Modern JavaScript :
Using let
Using const

Example using let :
let x = 5;
let y = 6;
let z = x + y;

Example using const :
const x = 5;
const y = 6;
const z = x + y;

Example using var :
var x = 5;
var y = 6;
var z = x + y;

JavaScript Identifiers :
Variables are identified with unique names called identifiers.

Names can be short like x, y, z.

Names can be descriptive age, sum, carName.

The rules for constructing names (identifiers) are:

Names can contain letters, digits, underscores, and dollar signs.
Names must begin with a letter, a $ sign or an underscore (_).
Names are case sensitive (X is different from x).
Reserved words (JavaScript keywords) cannot be used as names.

Note :
Numbers are not allowed as the first character in names.

This way JavaScript can easily distinguish identifiers from numbers.

Example :
let _lastName = "Johnson";
let _x = 2;
let _100 = 5;

JavaScript Dollar Sign $ :
JavaScript also treats a dollar sign as a letter.

Identifiers containing $ are valid variable names: 
Example :
let $ = "Hello World";
let $$$ = 2;
let $myMoney = 5;

<!-- Declaring JavaScript Variables-->
Creating a variable in JavaScript is called declaring a variable.

you can declare variable with "let","var" or "const"

Declaring a Variable Using var:
The var keyword was used in all JavaScript code before 2015.

The let and const keywords were new to JavaScript in 2015.

Using var (Not Recommended)
var x = 5;
var y = 6;
var z = x + y;

<!-- When to Use var, let, or const? -->
1. Always declare variables

2. Always use const if the value should not be changed

3. Always use const if the type should not be changed (Arrays and Objects)

4. Only use let if you cannot use const

5. Never use var if you can use let or const.

<!-- variables in JS can hold 8 datatypes -->
Number
Example: let age = 25;

BigInt
Example: let big = 12345678901234567890n;

String
Example: let name = "Yahya";

Boolean
Example: let isOnline = true;

Undefined
Example: let x; // undefined

Null
Example: let emptyValue = null;

Symbol
Example: let id = Symbol("id");

Object (non-primitive?) → Actually function and array are objects
But ECMAScript now classifies "Object" as a primitive type container, even though the values are non-primitive.

<!-- JavaScript Let -->
The let keyword was introduced in ES6 (2015)

Variables declared with let have Block Scope

Variables declared with let must be Declared before use

Variables declared with let cannot be Redeclared in the same scope

<!--Block Scope -->

Before ES6 (2015), JavaScript did not have Block Scope.

JavaScript had Global Scope and Function Scope.

ES6 introduced the two new JavaScript keywords: let and const.

These two keywords provided Block Scope in JavaScript

Example :
{
  let x = 2;
}
 // x can NOT be used here

 <!-- Global Scope -->
 Variables declared with the var always have Global Scope.

Variables declared with the var keyword can NOT have block scope
Example :
{
  var x = 2;
}
// x CAN be used here
<!-- Cannot be Redeclared -->
Variables defined with let can not be redeclared.

You can not accidentally redeclare a variable declared with let.

With let you can not do this:

let x = "John Doe";

let x = 0;

Variables defined with var can be redeclared.

With var you can do this:

var x = "John Doe";

var x = 0;
Redeclaring a variable using the var keyword can impose problems.

Redeclaring a variable inside a block will also redeclare the variable outside the block

<!-- What is Good? -->

let and const have block scope.

let and const can not be redeclared.

let and const must be declared before use.

let and const does not bind to this.

let and const are not hoisted.

<!-- What is Not Good? -->

var does not have to be declared.

var is hoisted.

var binds to this.

<!-- Let Hoisting -->

Variables defined with var are hoisted to the top and can be initialized at any time.

Meaning: You can use the variable before it is declared:

Example:
This is OK:

carName = "Volvo";
var carName;