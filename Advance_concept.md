
 <a href="#README.md">at()</a> 

<p align='right'><a href="#top">&#8593; Back to Top</a></p>
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
