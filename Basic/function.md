<h2>Function</h2>

`Functions` are objects that can be invoked, or called, to perform a specific task or calculation. A function in JavaScript is defined using the function keyword, followed by the function name, and a set of parentheses

```
function function_name() {
    // body
    return statements
}

function addNumbers(num1, num2) {
  return num1 + num2;
}
```
In this example, the addNumbers function takes two parameters (num1 and num2) and returns their sum.

To call a function in JavaScript, you simply need to invoke it by using its name, followed by a set of parentheses containing any arguments that the function takes
```
function_name()

let sum = addNumbers(3, 5);
console.log(sum); // Output: 8
```
<h3>Scope</h3>
scope refers to the visibility and accessibility of variables within a particular part of a program. There are two main types of scope

- global scope
- local scope

<ol>
<li>global scope</li>
<ul>
<li>Global scope refers to variables or functions that are accessible from anywhere in the program, including inside functions and blocks</li>
<li>Global variables and functions are declared outside of any function or block, and they have a lifespan that is equal to the lifespan of the program itself</li>
</ul>
<pre>
let globalVar = 'I am global';
<br>
function myFunction() {
  console.log(globalVar); // Output: I am global
}

myFunction();
console.log(globalVar); // Output: I am global
</pre>

<li>local scope</li>
<ul>
<li>local scope refers to variables or functions that are only accessible within a specific function or block</li>
<li>Local variables and functions are declared inside a function or block, and they have a lifespan that is limited to the lifespan of that function or block</li>
<li>Local scope is useful because it allows you to create variables and functions that are only needed within a specific part of your program, without affecting the rest of your code</li>
</ul>
<pre>function myFunction() {
  let localVar = 'I am local';
  console.log(localVar); // Output: I am local
}

myFunction();
console.log(localVar); // Output: Uncaught ReferenceError: localVar is not defined
</pre>
<h3>Function scope</h3>
<p>Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.</p>

```
let globalVar = 'I am global';

function myFunction() {
  console.log(globalVar); // Output: I am global
}
myFunction();
```
<h4>closure</h4>
a closure is a feature that allows a function to access variables from an outer function that has already returned. This means that even after the outer function has finished executing and its variables are no longer in memory, the inner function can still access and use those variables

```
function outerFunction() {
  let name = 'John';

  function innerFunction() {
    console.log(`Hello ${name}`);
  }

  return innerFunction;
}

let greeting = outerFunction();
greeting(); // Output: Hello John
```

<h4>Arrow functions</h4>
An arrow function expression is a compact alternative to a traditional function expression, with some semantic differences and deliberate limitations in usage

```
() => expression

(param1, paramN) => {
  // statements
}

const multiply = (a, b) => a * b;

```
<h4>Recursion</h4>
The act of a function calling itself, recursion is used to solve problems that contain smaller sub-problems. A recursive function can receive two inputs: a base case (ends recursion) or a recursive case (resumes recursion)


```
const factorial = (n) => {
  if (n === 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
};
console.log(factorial(10));
// 3628800
```
<h4>IIFE</h4>

- An IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined. 

- It often used to create a private scope for a block of code to avoid naming conflicts with other scripts on the page

```
(function () {
  // statements
})();

(() => {
  // statements
})();

(async () => {
  // statements
})();
```
Example
```
var result = (function () {
  var x = 5;
  return x * x;
})();

console.log(result);
```