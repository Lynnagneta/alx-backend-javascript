My read me file for 0x00. ES6 Basics
What is ES6?
ES6 stands for ECMAScript 6, which is a major update to JavaScript released in 2015. Think of it like a software update that gave JavaScript superpowers—making it easier to write clean, modern, and powerful code.

New Features Introduced in ES6
Some of the coolest features that came with ES6 include:
let and const for better variable control


Arrow functions: shorter way to write functions


Default function parameters


Template literals (fancy strings with ${} inside)


Spread and rest ... operators


Classes and better ways to make objects


for...of loops for looping through stuff


Promises (for handling async code)


Modules (for organizing code in files)



The Difference Between a Constant and a Variable
let = a variable you can change later.


let age = 16;
age = 17; // This is fine.

const = a constant value that can’t be changed.


const birthYear = 2008;
birthYear = 2009; // ❌ This will cause an error.

Use const when you don't want the value to ever change.

Block-Scoped Variables
Before ES6, variables were "function-scoped," meaning they were visible anywhere inside a function. ES6 brought in let and const, which are block-scoped.
A block is anything inside { }.
if (true) {
  let name = "Silas";
  console.log(name); // Works!
}
console.log(name); // ❌ Doesn't work. 'name' is block-scoped.


Arrow Functions & Default Parameters
Arrow functions are a shorter way to write functions.
// Normal function
function sayHi(name) {
  return `Hi, ${name}`;
}

// Arrow function
const sayHi = (name = "friend") => `Hi, ${name}`;

Notice that we also gave a default parameter: if you don’t give a name, it defaults to “friend”.

Rest and Spread Function Parameters
Rest (...) collects multiple values into an array.


function add(...nums) {
  return nums.reduce((a, b) => a + b);
}
add(1, 2, 3, 4); // 10

Spread (...) spreads an array into individual values.


const nums = [1, 2, 3];
console.log(...nums); // 1 2 3

They look the same (...) but are used differently.

String Templating in ES6
No more messy + signs to join strings!
const name = "Silas";
const age = 16;

console.log(`My name is ${name} and I’m ${age} years old.`);

This is called a template literal—it’s cleaner and easier to read.

Object Creation and Properties in ES6
In ES6, you can create objects more easily.
const name = "Silas";
const age = 16;

const person = {
  name,  // same as name: name
  age,
  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
};

You can also use computed properties:
const key = "score";
const player = {
  [key]: 100 // same as score: 100
};


Iterators and for-of Loops
Iterators are things you can loop through—like arrays, strings, maps.
for...of is a loop that makes this super simple:
const colors = ["red", "blue", "green"];

for (const color of colors) {
  console.log(color);
}

Way nicer than for (let i = 0; i < colors.length; i++) right?

