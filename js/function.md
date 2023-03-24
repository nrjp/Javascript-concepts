<h2>Function</h2>

<ul>
<li><a href="#Functions">Functions</a></li>
<li><a href="#Scope">Scope</a></li>
<li><a href="#Function scope">Functions Scope</a></li>
<li><a href="#closure">Closure</a></li>
<li><a href="#Anonymous">Anonymous Functions</a></li>
<li><a href="#Arrow">Arrow Function</a></li>
<li><a href="#Recursion">Recursion Functions</a></li>
<li><a href="#IIFE">IIFE Functions</a></li>
<li><a href="#Lexical">Lexical Scope</a></li>
<li><a href="#Recursion">Recursion</a></li>
<li><a href="#new">new Keyword</a></li>
<li><a href="#this">this Keyword</a></li>
<li><a href="#apply">apply()</a></li>
<li><a href="#bind">bind()</a></li>
<li><a href="#call">call()</a></li>
<li><a href="#toString">toString()</a></li>
<li><a href="#Text Node">Text Node</a></li>
<li><a href="#Template literals">Template literals</a></li>
</ul>
<br />
<span id="Functions"></span>

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
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Scope"></span>
<h3>Scope</h3>

`scope` refers to the visibility and accessibility of variables within a particular part of a program. There are two main types of scope

- global scope
- local scope

<ol>

<li>global scope</li>

- Global scope refers to variables or functions that are accessible from anywhere in the program, including inside functions and blocks
- Global variables and functions are declared outside of any function or block, and they have a lifespan that is equal to the lifespan of the program itself
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

- local scope refers to variables or functions that are only accessible within a specific function or block
- Local variables and functions are declared inside a function or block, and they have a lifespan that is limited to the lifespan of that function or block
- Local scope is useful because it allows you to create variables and functions that are only needed within a specific part of your program, without affecting the rest of your code
<pre>function myFunction() {
  let localVar = 'I am local';
  console.log(localVar); // Output: I am local
}

myFunction();
console.log(localVar); // Output: Uncaught ReferenceError: localVar is not defined
</pre>
</ol>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Function scope"></span>
<h3>Function scope</h3>

Variables defined inside a `function` cannot be accessed from anywhere outside the function, because the variable is defined only in the `scope `of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.</p>

```
let globalVar = 'I am global';

function myFunction() {
  console.log(globalVar); // Output: I am global
}
myFunction();
```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="closure"></span>

<h3>closure</h3>

A `closure` is a feature that allows a function to access variables from an outer function that has already returned. This means that even after the outer function has finished executing and its variables are no longer in memory, the inner function can still access and use those variables

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
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Anonymous"></span>

<h3>Anonymous function</h3>

An `anonymous function` is a function without a function name. Only function expressions can be anonymous, function declarations must have a name

```
// Anonymous function created as a function expression
(function () {});

// Anonymous function created as an arrow function
() => {};


setTimeout(function() {
    console.log('Execute later after 1 second')
}, 1000);
```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Arrow"></span>

<h3>Arrow functions</h3>

An `arrow function` expression is a compact alternative to a traditional function expression, with some semantic differences and deliberate limitations in usage

```
() => expression

(param1, paramN) => {
  // statements
}

const multiply = (a, b) => a * b;

```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Recursion"></span>

<h3>Recursion Functions</h3>

The act of a function calling itself, `recursion` is used to solve problems that contain smaller sub-problems. A recursive function can receive two inputs: a base case (ends recursion) or a recursive case (resumes recursion)


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
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="IIFE"></span>

<h3>IIFE Functions</h3>

- An `IIFE` (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined. 

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
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Lexical"></span>

<h3>Lexical scoping</h3>

`Lexical scoping` in JavaScript is a mechanism that determines how variable names are resolved in nested functions. The term "lexical" refers to the fact that the scope of a variable is determined by its position in the source code, or its lexeme. In other words, the scope of a variable is determined by its location in the code, rather than its value or context of execution.

```
function outer() {
  const a = 1;

  function inner() {
    const b = 2;

    console.log(a + b); // Output: 3
  }

  inner();
}

outer();
```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="new"></span>

<h3>new Keyword</h3>

The `new` keyword is used to create new instances of objects that are defined using constructor functions.

```
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const person1 = new Person('John', 30);
const person2 = new Person('Jane', 25);
```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="this"></span>

<h3>this Keyword</h3>

`this` keyword refers to the current execution context, which can be different depending on how and where the function is invoked.

```
// Example 1: this inside a function
function foo() {
  console.log(this);
}

foo(); // logs the global object (e.g. window in a browser, global in Node.js)

// Example 2: this inside an object method
const obj = {
  name: 'John',
  greet: function() {
    console.log(`Hello, my name is ${this.name}`);
  }
};

obj.greet(); // logs "Hello, my name is John"

// Example 3: this inside a constructor function
function Person(name) {
  this.name = name;
}

const person = new Person('Jane');
console.log(person.name); // logs "Jane"

// Example 4: this with call() or apply()
function greet() {
  console.log(`Hello, my name is ${this.name}`);
}

const john = { name: 'John' };
const jane = { name: 'Jane' };

greet.call(john); // logs "Hello, my name is John"
greet.apply(jane); // logs "Hello, my name is Jane"
```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="apply"></span>

<h3>apply</h3>

The `apply()` method is used to call a function with a given this value and arguments provided as an array.

```
function sum(x, y) {
  return x + y;
}

let numbers = [2, 3];

let result = sum.apply(null, numbers);

console.log(result); // Output: 5
```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="bind"></span>

<h3>bind</h3>

The `bind()` method creates a new function that has this keyword set to a particular value, and returns that function. 

```
const person = {
  firstName: 'John',
  lastName: 'Doe'
};

function fullName() {
  console.log(this.firstName + ' ' + this.lastName);
}

const logFullName = fullName.bind(person);

logFullName(); // Output: John Doe

```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="call"></span>

<h3>call</h3>

the `call()` method is a way to invoke a function with a specified this value and arguments provided individually

```
function.call(thisArg, arg1, arg2, ...)

const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}

const person1 = {
  firstName: "John",
  lastName: "Doe"
}

const person2 = {
  firstName: "Mary",
  lastName: "Smith"
}

// Use call() to invoke the fullName function on person1 and person2 objects
const fullName1 = person.fullName.call(person1); // "John Doe"
const fullName2 = person.fullName.call(person2); // "Mary Smith"

```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="toString"></span>

<h3>toString</h3>

The `toString()` method returns a string representing the source code of the specified Function
```
// define a custom object
const person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 30,
  toString: function() {
    return `${this.firstName} ${this.lastName}, age ${this.age}`;
  }
};

// call the toString() method on the object
console.log(person.toString()); // output: "John Doe, age 30"

```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Text Node"></span>

<h3>Text Node</h3>

 A `text node` refers to a type of node that is used to represent textual content within an HTML element. A text node is a child node of an HTML element, and it contains only text. It cannot have child nodes of its own.

```
<p>This is a paragraph.</p>

const pElement = document.querySelector('p');
const textContent = pElement.textContent;
console.log(textContent); // Output: This is a paragraph.

```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Template literals"></span>

<h3>Template literals</h3>

`Template literals` are literals delimited with backtick (`) characters, allowing for multi-line strings, string interpolation with embedded expressions, and special constructs called tagged templates.

```
`string text`

`string text line 1
 string text line 2`

`string text ${expression} string text`

tagFunction`string text ${expression} string text`
```
