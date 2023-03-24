
<span id="Classes"></span>
<h3>Classes</h3>

`Classes` are a way to create reusable objects with properties and methods. They are a type of syntactical sugar that provides a more structured way to define object-oriented programming in JavaScript.

```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

let person1 = new Person("Alice", 25);
let person2 = new Person("Bob", 30);

person1.greet(); // logs "Hello, my name is Alice and I am 25 years old."
person2.greet(); // logs "Hello, my name is Bob and I am 30 years old."
```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>
<span id="Getters and setters"></span>
<h3>Getters and setters</h3>

`Getters and setters` are a way to define and access object properties in JavaScript. Getters are used to access the properties of an object, while setters are used to change the properties of an object.

```
class Person {
  constructor(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
  }

  get fullName() {
    return `${this.firstName} ${this.lastName}`;
  }

  set fullName(name) {
    const names = name.split(' ');
    this.firstName = names[0];
    this.lastName = names[1];
  }
}

const person = new Person('John', 'Doe');

console.log(person.fullName); // Output: "John Doe"

person.fullName = 'Jane Smith';

console.log(person.firstName); // Output: "Jane"
console.log(person.lastName); // Output: "Smith"
console.log(person.fullName); // Output: "Jane Smith"
```
<p align='right'><a href="#top">&#8593; Back to Top</a></p>
<span id="promis"></span>
<h3>promis</h3>

- The `Promise` object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
- Promises in JavaScript are a way of handling asynchronous operations. They are objects that represent the eventual completion (or failure) of an asynchronous operation and allow you to handle the result once it's available.
<p align='right'><a href="#top">&#8593; Back to Top</a></p>
<span id="async and await"></span>
<h3>async and await</h3>

`async` is a keyword that can be used to define an asynchronous function. When a function is marked as async, it always returns a promise, and the value of the promise is the value that the function returns, or the error that it throws.

`await` is a keyword that can only be used inside of an async function. It is used to wait for a promise to resolve or reject before continuing with the execution of the function. When await is used with a promise, it suspends the execution of the async function until the promise is settled. Once the promise is settled, the result of the promise is returned or the error is thrown

```
async function fetchUser(userId) {
  const response = await fetch(`https://jsonplaceholder.typicode.com/users/${userId}`);
  const user = await response.json();
  return user;
}

fetchUser(1)
  .then(user => console.log(user))
  .catch(error => console.error(error));
```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>
<!-- <span id="Event loop"></span>
<h3>Event loop</h3>

```

``` -->

<p align='right'><a href="#top">&#8593; Back to Top</a></p>
<span id="module exports"></span>
<h3>module exports</h3>

he `module.exports` object is used to define what parts of a module should be exported or made available to other parts of the application.

```
// module "my-module.js"
function cube(x) {
  return x * x * x;
}

const foo = Math.PI + Math.SQRT2;

const graph = {
  options: {
    color: "white",
    thickness: "2px",
  },
  draw() {
    console.log("From graph draw function");
  },
};

export { cube, foo, graph };

```

<p align='right'><a href="#top">&#8593; Back to Top</a></p>
<span id="Spread and REST operators"></span>
<h3>Spread and REST operators</h3>

The `spread` operator (...) is used to "spread" the elements of an array or an object literal
```
const original = [1, 2, 3];
const copy = [...original];
console.log(copy); // [1, 2, 3]
```
The `REST` operator (...) is used to represent an indefinite number of arguments as an array.

```
const arr = [1, 2, 3, 4];
const [first, second, ...rest] = arr;
console.log(first, second, rest); // 1 2 [3, 4]
```
