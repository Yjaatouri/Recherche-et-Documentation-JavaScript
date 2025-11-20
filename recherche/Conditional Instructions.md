# Recherche-et-Documentation-JavaScript
Recherche et Documentation JavaScript 
<!-- Conditionals -->

Conditionals
Conditional statements control behavior in JavaScript and determine whether or not pieces of code can run.

There are multiple different types of conditionals in JavaScript including:

“If” statements: where if a condition is true it is used to specify execution for a block of code.
“Else” statements: where if the same condition is false it specifies the execution for a block of code.
“Else if” statements: this specifies a new test if the first condition is false.
Now that you have the basic JavaScript conditional statement definitions, let’s show you examples of each.

//  Learn How to Become a Web Developer with Pluralsight Skills

If Statement Example
As the most common type of conditional, the if statement only runs if the condition enclosed in parentheses () is truthy.

EXAMPLE
if (10 > 5) {
      var outcome = "if block";
}
​
outcome;
OUTPUT
"if block"

Here’s what’s happening in the example above:

The keyword if tells JavaScript to start the conditional statement.
(10 > 5) is the condition to test, which in this case is true — 10 is greater than 5.
The part contained inside curly braces {} is the block of code to run.
Because the condition passes, the variable outcome is assigned the value "if block".
Else Statement Example
You can extend an if statement with an else statement, which adds another block to run when the if conditional doesn’t pass.

EXAMPLE
if ("cat" === "dog") {
      var outcome = "if block";
} else {
      var outcome = "else block";
}
outcome;
OUTPUT
"else block"
In the example above, "cat" and "dog" are not equal, so the else block runs and the variable outcome gets the value "else block".

Else If Statement Example
You can also extend an if statement with an else if statement, which adds another conditional with its own block.

EXAMPLE
if (false) {
      var outcome = "if block";
} else if (true) {
      var outcome = "else if block";
} else {
      var outcome = "else block";
}

outcome;
OUTPUT
"else if block"

You can use multiple if else conditionals, but note that only the first else if block runs. JavaScript skips any remaining conditionals after it runs the first one that passes.

EXAMPLE
if (false) {
      var outcome = "if block";
} else if (true) {
      var outcome = "first else if block";
} else if (true) {
      var outcome = "second else if block";
} else {
      var outcome = "else block";
}
​
outcome;
OUTPUT
"first else if block"

An else if statement doesn’t need a following else statement to work. If none of the if or else if conditions pass, then JavaScript moves forward and doesn’t run any of the conditional blocks of code.

EXAMPLE
if (false) {
      var outcome = "if block";
} else if (false) {
      var outcome = "else if block";
}
​
outcome;
OUTPUT
"first else if block"

===================================================
<!-- If Statements -->

An if statement allows you to execute a block of code if a specified condition evaluates to true. Otherwise, the block of code is skipped. The following is the syntax for an if statement in JavaScript:

if (condition) {
  // code to be executed if condition is true
}

The condition can be any expression that evaluates to a boolean value (true or false). If the condition is true, the code inside the curly braces will be executed. Otherwise, the code will be skipped. Here is an example of an if statement in JavaScript:

let num = 10;

if (num > 0) {
  console.log("The number is positive");
}

In this example, the condition is num > 0. Since num is equal to 10, which is greater than 0, the condition is true, and the code inside the curly braces will be executed. The output of this code will be "The number is positive".

<!-- Else Statements -->

An else statement is used to execute a block of code if the condition in the if statement is false. Here is the syntax of an else statement in JavaScript:

if (condition) {
  // code to be executed if condition is true
} else {
  // code to be executed if condition is false
}

If the condition in the if statement is true, the code inside the first set of curly braces will be executed. If the condition is false, the code inside the second set of curly braces will be executed. Here is an example of an if/else statement in JavaScript:

let num = -10;

if (num > 0) {
  console.log("The number is positive");
} else {
  console.log("The number is not positive");
}

In this example, the condition is num > 0. Since num is equal to -10, which is not greater than 0, the condition is false, and the code inside the else block will be executed. The output of this code will be "The number is not positive".

<!-- Else If Statements -->

An else if statement is used to check additional conditions after the first condition in an if statement is false. Here is the syntax of an else if statement in JavaScript:

if (condition1) {
  // code to be executed if condition1 is true
} else if (condition2) {
  // code to be executed if condition2 is true
} else {
  // code to be executed if both condition1 and condition2 are false
}

If the first condition is true, the code inside the first set of curly braces will be executed, and the code inside the else if and else blocks will be skipped. If the first condition is false, the second condition will be checked. If the second condition is true, the code inside the second set of curly braces will be executed, and the code inside the else block will be skipped. If both conditions are false, the code inside the else block will be executed. Here is an example of an if/else if/else statement in JavaScript:

let num = 0;

if (num > 0) {
  console.log("The number is positive");
} else if (num < 0) {
  console.log("The number is negative");
} else {
  console.log("The number is zero");

<!-- Nested If/Else Statements -->

Nested if/else statements are used when we want to check for more than one condition, and each condition has its own set of actions. In a nested if/else statement, there is an inner if/else statement within an outer if/else statement.

<!-- Here is the syntax of a nested if/else statement in JavaScript: -->

if (condition1) {
  // code to be executed if condition1 is true
  if (condition2) {
    // code to be executed if both condition1 and condition2 are true
  } else {
    // code to be executed if condition1 is true and condition2 is false
  }
} else {
  // code to be executed if condition1 is false
}
If condition1 is true, the code inside the first set of curly braces will be executed. If condition2 is also true, the code inside the inner set of curly braces will be executed. If condition2 is false, the code inside the else block will be executed. If condition1 is false, the code inside the else block will be executed.

<!-- Here is an example of a nested if/else statement in JavaScript: -->

let num = 10;

if (num > 0) {
  if (num < 100) {
    console.log("The number is between 0 and 100");
  } else {
    console.log("The number is greater than or equal to 100");
  }
} else {
  console.log("The number is less than or equal to 0");
}

In this example, the first condition checks if num is greater than 0. If it is, the second condition checks if num is less than 100. If it is, the code inside the first inner set of curly braces will be executed, and the output will be "The number is between 0 and 100". If num is greater than or equal to 100, the code inside the else block of the inner if statement will be executed, and the output will be "The number is greater than or equal to 100". If num is less than or equal to 0, the code inside the else block of the outer if statement will be executed, and the output will be "The number is less than or equal to 0".

<!-- Best Practices -->

Keep it simple: Try to use simple conditions and limit the number of nested if/else statements to make your code more readable and easier to understand.

Be consistent: Use the same type of braces, indentation, and spacing in your code to make it more readable and consistent. This will make it easier for other developers to read and understand your code.

Use descriptive variable names: Use descriptive names for variables and avoid using single-letter variables to make your code more readable and self-explanatory.

Avoid repetition: Use functions or loops to avoid repeating the same if/else statements throughout your code.
Test your code: Test your code with different inputs and edge cases to ensure that it works as expected and handles unexpected inputs and errors correctly.

<!-- Real World Scenario Examples -->

E-commerce website: When a customer adds items to their shopping cart, the website might use a conditional statement to check whether the cart is empty or not. If the cart is empty, the website might display a message to encourage the customer to add items to their cart. If the cart is not empty, the website might display the items and the total cost of the purchase.
Weather App: A weather app might use conditional statements to display different information depending on the weather conditions. For example, if it's raining, the app might display an animation of raindrops falling on the screen. If it's sunny, the app might display an animation of a sun with a smiling face.
Online Quiz: An online quiz might use conditional statements to calculate the score of a user based on their answers. For example, if the user answers a question correctly, the quiz might add a point to their score. If the user answers incorrectly, the quiz might deduct a point from their score. The quiz might also use conditional statements to determine the level of difficulty for each question based on the user's previous answers and their overall score.
Traffic Lights: Traffic lights use conditional statements to control the flow of traffic. If the traffic light is green, the cars are allowed to move forward. If the traffic light is yellow, the cars are warned to slow down. If the traffic light is red, the cars must stop.

<!-- Conclusion -->

Conditional statements in JavaScript provide a way to make decisions and execute code based on certain conditions. The if statement is used to execute code if a condition is true, while the else statement is used to execute code if the condition is false. The else if statement allows for additional conditions to be checked and code to be executed accordingly. Understanding and effectively using conditional statements is an important skill for writing dynamic and responsive code in JavaScript.