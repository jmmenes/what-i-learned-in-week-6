# What I Learned In Week 6 At Code Immersives

&nbsp;

## Arrays

The JavaScript Array class is a global object that is used in the construction of arrays; which are high-level, list-like objects.

JavaScript arrays are used to store multiple values in a single variable.

    var cars = ["Saab", "Volvo", "BMW"];

&nbsp;

## Array Methods

The strength of JavaScript arrays lies in the array methods. Array methods are functions built-in to JavaScript that we can apply to our arrays — Each method has a unique function that performs a change or calculation to our array and saves us from writing common functions from scratch.

One method example .toString()

The JavaScript method .toString() converts an array to a string of (comma separated) array values.

    var fruits = ["Banana", "Orange", "Apple", "Mango"];

    document.getElementById("demo").innerHTML = fruits.toString();

    Result: Banana,Orange,Apple,Mango

&nbsp;

## For Loops

Loops can execute a block of code a number of times.

The for loop has the following syntax:

The JavaScript for loop statement allows you to create a loop with three optional expressions. The following illustrates the syntax of the for loop statement:

    for (initialization; condition; post-expression) {
        // statements
    }


    for (i = 0; i < 5; i++) {
    text += "The number is " + i + "<br>";
    }

From the example above, you can read:

Statement 1, sets a variable before the loop starts (var i = 0).

Statement 2, defines the condition for the loop to run (i must be less than 5).

Statement 3, increases a value (i++) each time the code block in the loop has been executed.

&nbsp;

JavaScript supports different kinds of loops:

- for - loops through a block of code a number of times

- for/in - loops through the properties of an object

- for/of - loops through the values of an iterable object
- while - loops through a block of code while a specified condition is true
- do/while - also loops through a block of code while a specified condition is true

&nbsp;

## For of Loops

for/of - loops through the values of an iterable object

For...of iterates arrays, array-like objects, and generally any iterable (maps, sets, DOM collections). You can destructure the iterated item in place. On top of that, for...of has a short syntax.

Syntax:

    for (variable of iterable) {
    // code block to be executed
    }

For example:

    const products = ['oranges', 'apples'];

    for (const product of products) {
    console.log(product);
    }
    // 'oranges'
    // 'apples'

for...of cycle iterates over every item of products. The iterated item is assigned to the variable product.

&nbsp;

## Truthy & Falsy Values in JavaScript

Internally, JavaScript sets a value to one of six primitive data types:

- Undefined (a variable with no defined value)
- Null (a single null value)
- Boolean (true or false)
- Number (this includes Infinity and NaN – not a number!)
- String (textual data)
- Symbol (a unique and immutable primitive new to ES6/2015)

Everything else is an Object — including arrays.

As well as a type, each value also has an inherent boolean value, generally known as either truthy or falsy. Some of the rules are a little bizarre so understanding the concepts and effect on comparison helps when debugging JavaScript applications.

&nbsp;

The following values are always falsy:

- false
- 0 (zero)
- '' or "" (empty string)
- null
- undefined
- NaN

Everything else is truthy. That includes:

- '0' (a string containing a single zero)
- 'false' (a string containing the text “false”)
- [] (an empty array)
- {} (an empty object)
- function(){} (an “empty” function)

&nbsp;

A single value can therefore be used within conditions, example:

    if (value) {
    // value is truthy
    }
    else {
    // value is falsy
    // it could be false, 0, '', null, undefined or NaN
    }

&nbsp;

## Compound Booleans

We can implement any logic in a program using only nested conditionals. However, we can make shorter and more expressive code by combining simple Boolean expressions using logical operators (and, or, not) to create compound Boolean expressions.

The OR operator

Using the OR ( || ) operator, we can create a compound expression that is true when either of two conditions are true.

    if (cspGrade >= 75 || progGrade >= 75) {
    console.log("You're eligible for AP CS A!");
    }
