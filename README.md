# Quiz #2

## Instructions

1. Fork this repo
2. Clone your fork
3. Fill in your answers by writing in the appropriate area, or placing an 'x' in
the square brackets (for multiple-choice questions).
4. Add/Commit/Push your changes to Github.
5. Open a pull request.

## JavaScript

### Question #1

**What of the following are JavaScript Data Types?**

Select all that apply:
```
[X] Strings
[X] Booleans
[X] Undefined
[] NaN
[X] Integers
[] Arrays
[X] Null
```

## Question #2

Explain what is a REPL, and why is it important for us as developers and help with debugging?

```
REPL stands for Read-Evaluate-Print-Loop. It is a programming environment that lets developers run Javascript code one line at a time. This is important because when developers encounter a bug or error, they need to carefully comb through the code to figure out how to fix the problem.

```
### Question #3

**Given the Following Array**

var foods = [ ["apple","banana","strawberry"], ["pizza","fries","hamburger"] ];

Create a For Loop that outputs the following string for each piece of fruit in the console. "I want to eat a [fruit]"

```js
foods[0].forEach(function (foods) {
  console.log("I want to eat a " + foods);
}); //I know this technically is not a "for loop".
```
### Question #4

**Given the Following Array**

var foods = [ ["apple","banana","strawberry"], ["pizza","fries","hamburger"] ];

How would I go about accessing the string "pizza" in the above array?

```js
foods[1][0];
```

## Scope/Context/Closures

### Question #5

Describe the rules of scope in JavaScript.

Your Answer:
```
Scope is the list of all the variables that can be accessed from the current line of code. Global variables can be accessed anywhere. Conversely, variables that are defined within a function using 'var =' cannot be accessed globally; they can only be accessed within that function and any child functions.
```

### Question #6

Define an object and store it in a variable `pizza`. The object should have 2
properties: a temperature (set to 70), and a method called `bake`. When called,
this method should set the pizza's temperature to be 300. Note: you may not use
the variable pizza inside your method.

Your Answer:
```js
var pizza = {
  temperature: 70,
  bake: function() {
    console.log("Pizza baked to 300 degrees.");
     this.temperature = 300;
  }
};
console.log(pizza.temperature);
pizza.bake();
console.log(pizza.temperature);
```

### Question #7

Define a global variable instructor and set it equal to your Squad Instructor's Name. Then, define the same as a local variable instead.

Your Answer:
```js
instructor = Becky; //global variable
var instructor = Becky;
```

## Objects and Functions

### Question #8

What are the differences between calling and referencing a function? Please provide examples of each.

```text
Once a function is defined, we can either call it or reference it. When you call a function, it performs the duties prescribed to it. When you reference a function, it prints out the details of what that function does upon being called.

For example:
var pizza = {
  temperature: 70,
  bake: function() {
    console.log("Pizza baked to 300 degrees.");
     this.temperature = 300;
  }
};
pizza.bake(); //CALLING the function
  performs function and changes temperature from 70 to 300.
pizza.bake; //REFERENCING the function
prints out the following:
  function () {
    console.log("Pizza baked to 300 degrees.");
    this.temperature = 300;
}
```
### Question #9

Using the object literal notation, Define an object called student and give it the properties (your attributes) of name, age, and a method sayHello, that outputs "Hi, my name is [your_name]".

Your Answer:
```js
var student = {
  name: "Christine",
  age: 24,
  sayHello: function() {
    console.log("Hi, my name is " + this.name +".");
  }
}
student.sayHello();
```

## Callbacks

### Question #10

**What is the difference between synchronous and asynchronous program execution?**

Select all that apply:
```
[] Synchronous code runs at an even pace, asynchronous code runs with uneven pacing.
[] Synchronous code runs all at the same time, asynchronous code runs completely randomly
[X] Synchronous code runs in order (as appears in the source), asynchronous code may run at a later time.
```
