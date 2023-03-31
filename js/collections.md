<h2>Keyed Collections</h2>
<br>
<p align='right'><a href="https://github.com/nrjp/javascript">Index</a></p>

<span id="top"><h3>Keyed collections are data collections that are ordered by key not index</h3></span>
<ol>
    <li><a href="#object">object</a></li>
    <li><a href="#Map">Map</a></li>
    <li><a href="#set">Set</a></li>
    <li><a href="#WeakMap">WeakMap</a></li>
    <li><a href="#object">object</a></li>
    <li><a href="#Convert">Convert</a></li>
</ol>
<br>
<ol>
<span id="object"><li>Object</li></span>
    - An object is a collection of key-value pairs<br>
    - You can define an object using curly braces {} and add properties to it using the dot notation or square bracket notation<br>
<ul>
<li>Keys must be strings</li>
<br>
<li>Objects don't maintain the order of the elements inserted into them</li>
<br>
<li>Keys are unique</li>
<br>
<li>Properties can be added or removed</li>
<br>
<li>Properties can be accessed using dot notation or square bracket notation</li>
<br>
<li>Objects are mutable</li>
<br>
<li>Properties can be nested</li>
<br>
<pre>
const person = {
name: 'John',
age: 30,
address: {
    street: '123 Main St',
    city: 'Anytown',
    state: 'CA',
}
};
<br>
# accessed object
console.log(person['name']); 
console.log(person.address.city);
# Add 
person.address.zip = '12345';
# Remove 
delete person['age'];
# loop over objects
for (let prop in person) {
console.log(prop + ': ' + person[prop]);}
# check if a property exists in an object
console.log('name' in person);
<br>
# merged two objects
const person = { name: 'John', age: 30 };
const address = { street: '123 Main St', city: 'Anytown' };
const merged = Object.assign({}, person, address);
console.log(merged);
</pre>
</ul>
<br>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Map"><li>Map</li></span>
<pre>
# Creating a Map
const sayings = new Map();
<br>
# Adding values
sayings.set("dog", "woof");
sayings.set("cat", "meow");
sayings.set("elephant", "toot");
<br>
# size for an Object
sayings.size; // 3
<br>
# Getting values
sayings.get("dog"); // woof
sayings.get("fox"); // undefined
<br>
# Checking for keys
sayings.has("bird"); // false
<br>
# Removing values
sayings.delete("dog");
sayings.has("dog"); // false
<br>
# Iterating over a Map
for (const [key, value] of sayings) {
  console.log(`${key} goes ${value}`);
}
// "cat goes meow"
// "elephant goes toot"
<br>
sayings.clear();
sayings.size; // 0
</pre>
<h4>Object and Map compared</h4>
<ul>
    <li>The keys of an Object are Strings or Symbols, where they can be of any value for a Map</li>
    <li>You can get the size of a Map easily, while you have to manually keep track of size for an Object</li>
    <li>The iteration of maps is in insertion order of the elements</li>
    <li>An Object has a prototype, so there are default keys in the map. (This can be bypassed using map = Object.create(null))</li>
</ul>
<br>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="set"><li>Set</li></span>
Set objects are collections of unique values.
<br />
<pre>
# Creating new set
const mySet = new Set();
<br>
# Adding values
mySet.add(1);
mySet.add("some text");
mySet.add("foo");
<br>
# Checking for values
mySet.has(1); // true
<br>
# Removing values
mySet.delete("foo");
<br>
# Checking size
mySet.size; // 2
<br>
# Iterating over
for (const item of mySet) {
  console.log(item);
}
</pre>

<br>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="WeakMap"><li>WeakMap</li></span>
A WeakMap is a built-in class that allows you to create collections of key-value pairs, where the keys are weakly referenced. 
This means that the keys must be objects, and if there are no other references to an object used as a key, it can be garbage collected.
<br />
<p>
We use WeakMap to store metadata for objects in memory, without causing memory leaks. A memory leak happens when an object is no longer needed by our code, but it still exists in memory because it is referenced somewhere else. This can happen when we store object metadata in a regular Map object, as the keys in a Map are stored as strong references.
<br>
WeakMap stores keys as weak references, which means that they can be automatically removed from memory by the garbage collector when they are no longer referenced by any other part of the code. This makes WeakMap particularly useful for scenarios where we want to store metadata for objects, but we don't want to keep those objects alive in memory longer than necessary.
</p>
<pre>
const myWeakMap = new WeakMap();
<br>
const key1 = {};
const key2 = {};
const value1 = 'foo';
const value2 = 'bar';
<br>
myWeakMap.set(key1, value1);
myWeakMap.set(key2, value2);
<br>
console.log(myWeakMap.get(key1)); // 'foo'
console.log(myWeakMap.get(key2)); // 'bar'
<br>
key1 = null; // The key object is no longer referenced
console.log(myWeakMap.get(key1)); // undefined - the key-value pair has been garbage collected
</pre>
<p>Map nad WeekMap</p>

| Feature               | Map                           | WeakMap                                 |
|-----------------------|-------------------------------|-----------------------------------------|
| Key type              | Any                           | Object                                  |
| Garbage collection    | No                            | Yes                                     |
| Iterable              | Yes                           | No                                      |
| Size                  | Available through `size`      | Not available                           |
| Key equality check    | Uses `Object.is` for comparison| Uses `WeakRef` for comparison           |
| Usage example         | Storing key-value pairs       | Storing metadata for objects in memory  |
| Key reference         | Strong                        | Weak                                    |
| Key removal           | Manual removal required       | Automatically removed on garbage collect|
| Performance           | Faster for small collections  | Faster for large collections            |
| Memory usage          | More memory used over time    | Less memory used over time              |


<br>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="WeakMap"><li>WeakMap</li></span>
In a WeakSet, only objects can be added as elements, and those objects are held by weak references. This means that if the object is no longer referenced anywhere else in the code, it can be automatically garbage collected, and will be removed from the WeakSet
<pre>
const myWeakSet = new WeakSet();
<br>
const obj1 = { name: 'Alice' };
const obj2 = { name: 'Bob' };
const obj3 = { name: 'Charlie' };
<br>
myWeakSet.add(obj1);
myWeakSet.add(obj2);
<br>
console.log(myWeakSet.has(obj1)); // true
console.log(myWeakSet.has(obj2)); // true
console.log(myWeakSet.has(obj3)); // false
<br>
obj1 = null; // The object is no longer referenced
console.log(myWeakSet.has(obj1)); // false - the object has been garbage collected and removed from the WeakSet
</pre>
<p>Set and weekSet</p>

| Set | WeakSet |
| --- | --- |
| Holds elements using strong references | Holds elements using weak references |
| Can store any type of value as an element, including primitive values | Can only store objects as elements |
| Provides methods for adding, deleting, and checking for the presence of elements | Provides methods for adding and checking for the presence of elements, but not for deleting them |
| Elements are not automatically removed from the Set when they are no longer used | Elements are automatically removed from the WeakSet when they are no longer used anywhere else in the code |
| Useful for storing collections of values that need to be checked or manipulated | Useful for storing collections of objects without causing memory leaks |

<br>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="Convert"><li>Convert</li></span>
<ul>
<li>Convert an Object into a Map </li>
<pre>const myObj = {a: 1, b: 2, c: 3};
// Convert the object to a Map
const myMap = new Map(Object.entries(myObj));
</pre>
<br>
<li>Convert a Map into an Object</li>
<pre>const myMap = new Map([
  ['a', 1],
  ['b', 2],
  ['c', 3]
]);
// Convert the Map to an object
const myObj = Object.fromEntries(myMap);</pre>
<br>
<li>Convert a Map into an Array </li>
<pre>const myMap = new Map([
  ['a', 1],
  ['b', 2],
  ['c', 3]
]);
// Convert the Map to an array
const myArray = Array.from(myMap);
</pre>
<br>
</ul>
<br>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>