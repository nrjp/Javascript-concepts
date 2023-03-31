<h2>Array</h2>
<p align='right'><a href="https://github.com/nrjp/javascript">Index</a></p>

 <p><b>Array</b> is a data structure used to store multiple values in a single variable. Arrays are declared using square brackets ([]), with each value separated by a comma</p>


| Method                                         | Description                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| <a href="#at">at()</a>                         | Returns the element at the specified position in an array    |
| <a href="#concat">concat()</a>                 | Joins two or more arrays and returns a new array             |
| <a href="#copyWithin">copyWithin()</a>         | Copies elements from an array to another position in the same array |
| <a href="#entries">entries()</a>               | Returns an array iterator object with key/value pairs        |
| <a href="#every">every()</a>                   | Tests whether all elements in an array pass a specified test  |
| <a href="#fill">fill()</a>                     | Fills the elements in an array with a static value            |
| <a href="#filter">filter()</a>                 | Creates a new array with all elements that pass a specified test |
| <a href="#find">find()</a>                     | Returns the value of the first element that passes a specified test |
| <a href="#findIndex">findIndex()</a>           | Returns the index of the first element that passes a specified test |
| <a href="#findLast">findLast()</a>             | Returns the value of the last element that passes a specified test |
| <a href="#findLastIndex">findLastIndex()</a>   | Returns the index of the last element that passes a specified test |
| <a href="#flat">flat()</a>                     | Returns a new array with all sub-array elements concatenated into it |
| <a href="#flatMap">flatMap()</a>               | Returns a new array with the results of calling a function for every element |
| <a href="#forEach">forEach()</a>               | Calls a function for each element in an array                 |
| <a href="#from">from()</a>                     | Creates a new Array instance from an array-like or iterable object |
| <a href="#includes">includes()</a>             | Determines whether an array contains a specified element     |
| <a href="#indexOf">indexOf()</a>               | Returns the index of the first occurrence of a specified value in an array |
| <a href="#isArray">isArray()</a>               | Determines whether a value is an array                        |
| <a href="#join">join()</a>                     | Joins all elements of an array into a string                  |
| <a href="#keys">keys()</a>                     | Returns an array iterator with the keys of an array           |
| <a href="#lastIndexOf">lastIndexOf()</a>       | Returns the index of the last occurrence of a specified value in an array |
| <a href="#map">map()</a>                       | Creates a new array with the results of calling a function for every element |
| <a href="#of">of()</a>                         | Creates a new Array instance with a variable number of arguments |
| <a href="#pop">pop()</a>                       | Removes the last element from an array and returns it         |
| <a href="#push">push()</a>                     | Adds one or more elements to the end of an array  |
| <a href="#reduce">reduce()</a>                 | Reduces an array to a single value by calling a function for each element |
| <a href="#reduceRight">reduceRight()</a>       | Reduces an array to a single value (from right-to-left) by calling a function for each element |
| <a href="#reverse">reverse()</a>               | Reverses the order of the elements in an array |
| <a href="#shift">shift()</a>                   | Removes the first element from an array and returns it |
| <a href="#slice">slice()</a> 	                 | Extracts a section of an array and returns a new array |
| <a href="#some">some()</a> 	                   | Tests whether at least one element in an array passes a specified test
| <a href="#sort">sort()</a> 	                   | Sorts the elements of an array |
| <a href="#splice">splice()</a> 	               | Adds or removes elements from an array |
| <a href="#toLocaleString">toLocaleString()</a> | Returns a string representation of the array, formatted according to the current locale |
| <a href="#toString">toString()</a> 	           | Returns a string representation of an array |
| <a href="#unshift">unshift()</a> 	             | Adds one or more elements to the beginning of an array |
| <a href="#values">values()</a> 	               | Returns an array iterator with the values of an |

  <p align='right'><a href="#top">&#8593; Back to Top</a></p>

<br />
<h3>Callback function</h3>

- A callback is a function that is passed as an argument to another function and is invoked when the other function has completed its operation. The purpose of a callback is to allow a function to call another function and pass in some behavior as an argument, so that the behavior can be executed after the first function has completed its task.
- Callbacks are commonly used in asynchronous programming
```
function greeting(name) {
  alert(`Hello, ${name}`);
}

function processUserInput(callback) {
  const name = prompt("Please enter your name.");
  callback(name);
}

processUserInput(greeting);
```
<br />
<h3>Array Methods</h3>
<ol>
<span id="at"><li>at()</li></span>

The `at()` method takes an integer value and returns the item at that index, allowing for positive and negative integers.
<pre>
const arr = ['apple', 'banana', 'cherry'];
<br>
# accessing element at specific index
console.log(arr.at(1)); // banana
<br>
# accessing element using negative index
console.log(arr.at(-3)); // apple
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="concat"><li>concat()</li></span>
The `concat()` method is used to merge two or more arrays.
<pre>
const letters = ["a", "b", "c"];
const numbers = [1, 2, 3];
<br>
const alphaNumeric = letters.concat(numbers);
console.log(alphaNumeric); // results in ['a', 'b', 'c', 1, 2, 3]
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="copyWithin"><li>copyWithin()</li></span>
The `copyWithin()` method allows you to copy a sequence of elements within the same array, optionally overwriting existing elements.
<pre>
array.copyWithin(target, start, end)
<br>
const array1 = [1, 2, 3, 4, 5];
<br>
// Copy the elements at index 0 and 1 and paste them at index 3
console.log(array1.copyWithin(3, 0, 2)); // Output: [1, 2, 3, 1, 2]
<br>
// Copy the last 3 elements to the beginning of the array
console.log(array1.copyWithin(0, -3)); // Output: [3, 4, 5, 4, 5]
<br>
// Copy the elements at index 1 and 2 and paste them at the end of the array
console.log(array1.copyWithin(3, 1, 3)); // Output: 
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="entries"><li>entries()</li></span>
The `entries()` method returns an array iterator object with each item in the array being an array containing the index and value of each element in the array

<pre>
const a = ["a", "b", "c"];
<br>
for (const [index, element] of a.entries()) {
  console.log(index, element);
}
<br>
// 0 'a'
// 1 'b'
// 2 'c'
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="every"><li>every()</li></span>
The `every()` method tests whether all elements in the array pass the test implemented by the provided function
<pre>
const array1 = [1, 2, 3, 4, 5];
<br>
const GreaterThanZero = (currentValue) => currentValue > 0;
console.log(array1.every(GreaterThanZero)); // output: true
<br>
const LessThanZero = (currentValue) => currentValue < 0;
console.log(array1.every(LessThanZero)); // output: false
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="fill"><li>fill()</li></span>
The `fill()` method changes all elements in an array to a static value, from a start index (default 0) to an end index (default array.length)
<pre>
fill(value)
fill(value, start)
fill(value, start, end)
<br>
const array = [1, 2, 3]
<br>
console.log(array.fill(4)); // [4, 4, 4]
console.log(array.fill(4, 1)); // [1, 4, 4]
console.log(array.fill(4, 1, 2)); // [1, 4, 3]
</pre>

</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="filter"><li>filter()</li></span>
The `filter()` method cllows you to create a new array with all elements that pass a certain condition, based on a provided callback function..

<pre>
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // output: [2, 4]
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="find"><li>find()</li></span>
The `find()` method returns the first element in the provided array that satisfies the provided testing function.
<pre>
const fruits = ['apple', 'banana', 'orange', 'mango'];
const foundFruit = fruits.find(fruit => fruit === 'banana');
console.log(foundFruit); // output: 'banana'
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="findIndex"><li>findIndex()</li></span>

The `findIndex()` method returns the index of the first element in the array that satisfies the provided testing function. If no elements in the array satisfy the testing function, -1 is returned.
<pre>
const numbers = [1, 3, 5, 8, 9, 10];
const index = numbers.findIndex(function(number) {
  return number % 5 === 0;
});
console.log(index); // Output: 2
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="findLast"><li>findLast()</li></span>

The `findLast()` method iterates the array in reverse order and returns the value of the first element that satisfies the provided testing function.
<pre>
const numbers = [1, 3, 5, 8, 9, 10];
const lastEven = numbers.findLast(function(number) {
  return number % 2 === 0;
});
console.log(lastEven); // Output: 10
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="findLastIndex"><li>findLastIndex()</li></span>
The `findLastIndex()` method iterates the array in reverse order and returns the index of the first element that satisfies the provided testing function
<pre>
const numbers = [1, 3, 5, 8, 9, 10];
const lastIndex = numbers.findLastIndex(function(number) {
  return number % 2 === 0;
});
console.log(lastIndex); // Output: 5
</pre>

<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="flat"><li>flat()</li></span>

The `flat()` method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
<pre>
const arr1 = [1, 2, [3, 4]];
arr1.flat(); // [1, 2, 3, 4]
<br>
const arr2 = [1, 2, [3, 4, [5, 6]]];
arr2.flat(); // [1, 2, 3, 4, [5, 6]]
<br>
const arr3 = [1, 2, [3, 4, [5, 6]]];
arr3.flat(2); // [1, 2, 3, 4, 5, 6]
<br>
const arr4 = [1, 2, [3, 4, [5, 6, [7, 8, [9, 10]]]]];
arr4.flat(Infinity); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="flatMap"><li>flatMap()</li></span>

`flatMap()`ombines the functionality of map() and flat() methods. It creates a new flattened array by first applying a mapping function to each element in the original array, and then flattening the result to a depth of 1.
<pre>
array.flatMap(callback[, thisArg])
<br>
const numbers = [1, 2, 3, 4];
const transformedNumbers = numbers.flatMap((num) => [num * 2]);
console.log(transformedNumbers); // Output: [2, 4, 6, 8]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="forEach"><li>forEach()</li></span>
The `forEach()` method is a method is used to execute a provided function once for each element in an array. 
<pre>
const numbers = [1, 2, 3, 4];
numbers.forEach((number) => {
  console.log(number);
});
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="from"><li>from()</li></span>
The `from()` static method creates a new, shallow-copied Array instance from an iterable or array-like object.
<pre>
const str = 'hello';
const arr = Array.from(str);
console.log(arr); // Output: ["h", "e", "l", "l", "o"]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="includes"><li>includes()</li></span>

The `includes()` method is a method is used to determine whether an array includes a certain value, returning true or false as appropriate.
<pre>
[1, 2, 3].includes(2); // true
[1, 2, 3].includes(4); // false
[1, 2, 3].includes(3, 3); // false
[1, 2, 3].includes(3, -1); // true
[1, 2, NaN].includes(NaN); // true
["1", "2", "3"].includes(3); // false
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="indexOf"><li>indexOf()</li></span>

The `indexOf()` method returns the first index at which a given element can be found in the array, or -1 if it is not present
<pre>
const array = [2, 9, 9];
array.indexOf(2); // 0
array.indexOf(7); // -1
array.indexOf(9, 2); // 2
array.indexOf(2, -1); // -1
array.indexOf(2, -3); // 0
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="isArray"><li>isArray()</li></span>
The `isArray()` static method determines whether the passed value is an Array.
<pre>
// all following calls return true
Array.isArray([]);
Array.isArray([1]);
Array.isArray(new Array());
Array.isArray(new Array("a", "b", "c", "d"));
Array.isArray(new Array(3));
// Little known fact: Array.prototype itself is an array:
Array.isArray(Array.prototype);
<br>
// all following calls return false
Array.isArray();
Array.isArray({});
Array.isArray(null);
Array.isArray(undefined);
Array.isArray(17);
Array.isArray("Array");
Array.isArray(true);
Array.isArray(false);
Array.isArray(new Uint8Array(32));
// This is not an array, because it was not created using the
// array literal syntax or the Array constructor
Array.isArray({ __proto__: Array.prototype });
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="join"><li>join()</li></span>

The `join()` method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the separator.
<pre>
const a = ["Wind", "Water", "Fire"];
a.join(); // 'Wind,Water,Fire'
a.join(", "); // 'Wind, Water, Fire'
a.join(" + "); // 'Wind + Water + Fire'
a.join(""); // 'WindWaterFire'
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="keys"><li>keys()</li></span>

The `keys()` method returns a new Array Iterator object that contains the keys for each index in the array.
<pre>
const person = {
  name: 'Alice',
  age: 30,
  gender: 'female'
};
const keys = Object.keys(person);
console.log(keys); // ['name', 'age', 'gender']
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="lastIndexOf"><li>lastIndexOf()</li></span>

The `lastIndexOf()` method returns the last index at which a given element can be found in the array, or -1 if it is not present. The array is searched backwards.
<pre>
const numbers = [1, 2, 3, 4, 2, 5, 2];
console.log(numbers.lastIndexOf(6)); // -1
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="map"><li>map()</li></span>
The `map()` method is used to create a new array by applying a function to each element of an existing array.
<pre>
const numbers = [1, 2, 3, 4];
const squares = numbers.map(function(num) {
  return num * num;
});
console.log(squares); // [1, 4, 9, 16]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="of"><li>of()</li></span>

The `of()` static method creates a new Array instance from a variable number of arguments, regardless of number or type of the arguments.
<pre>
Array.of(1); // [1]
Array.of(1, 2, 3); // [1, 2, 3]
Array.of(undefined); // [undefined]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="pop"><li>pop()</li></span>

The `pop()` method removes the last element from an array and returns that element. This method changes the length of the array.
<pre>
const myFish = ["angel", "clown", "mandarin", "sturgeon"];
const popped = myFish.pop();
console.log(myFish); // ['angel', 'clown', 'mandarin' ]
console.log(popped); // 'sturgeon'
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="push"><li>push()</li></span>
The `push()` method adds one or more elements to the end of an array and returns the new length of the array.
<pre>
const sports = ["soccer", "baseball"];
const total = sports.push("football", "swimming");
console.log(sports); // ['soccer', 'baseball', 'football', 'swimming']
console.log(total); // 4
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="reduce"><li>reduce()</li></span>

The `reduce()` method is used to reduce an array to a single value. It executes a provided function for each element of the array, and accumulates the result of each function call into a single value.
<pre>
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
});
console.log(sum); // 15
</pre>

- accumulator: The accumulated value.
- currentValue: The value of the current element being processed.
- currentIndex (optional): The index of the current element being processed.
- array (optional): The array on which reduce() was called.
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="reduceRight"><li>reduceRight()</li></span>

The `reduceRight()` method is similar to the reduce() method, but it reduces an array from right to left instead of left to right. It takes a callback function as its first argument, which is executed for each element in the array, along with an optional initial value.
<pre>
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduceRight((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);
console.log(sum); // Output: 15
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="reverse"><li>reverse()</li></span>

The `reverse()` method is used to reverse the order of the elements in an array. It modifies the original array and returns the reversed array.
<pre>
arr.reverse()
<br>
const arr = [1, 2, 3, 4, 5];
arr.reverse();
console.log(arr); // Output: [5, 4, 3, 2, 1]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="shift"><li>shift()</li></span>

The `shift()` method removes the first element from an array and returns that removed element. This method changes the length of the array.
<pre>
const myFish = ["angel", "clown", "mandarin", "surgeon"];
console.log("myFish before:", JSON.stringify(myFish));  // myFish before: ['angel', 'clown', 'mandarin', 'surgeon']
# shift
const shifted = myFish.shift();
# after shift
console.log("myFish after:", myFish); // myFish after: ['clown', 'mandarin', 'surgeon']
# shifted element
console.log("Removed this element:", shifted); // Removed this element: angel
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="slice"><li>slice()</li></span>

The `slice()` method is used to extract a section of an array and return a new array. It takes two arguments: the starting index and the ending index (exclusive) of the section to be extracted
<pre>
arr.slice(startIndex, endIndex)
<br>
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3);
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="some"><li>some()</li></span>

The `some()` method is used to test whether at least one element in an array passes a given test condition. It takes a callback function as an argument and returns a boolean value
<pre>
arr.some(callback)
<br>
function isBiggerThan10(element, index, array) {
  return element > 10;
}
[2, 5, 8, 1, 4].some(isBiggerThan10); // false
[12, 5, 8, 1, 4].some(isBiggerThan10); // true
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="sort"><li>sort()</li></span>

The `sort()` method is used to sort the elements of an array in place and returns the sorted array. By default, it sorts the elements in ascending order, but you can provide a comparison function as an argument to customize the sorting behavior.
<pre>
arr.sort([compareFunction])
<br>
const arr = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5];
arr.sort();
console.log(arr); // Output: [1, 1, 2, 3, 3, 4, 5, 5, 5, 6, 9]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="splice"><li>splice()</li></span>

The `splice()` method is used to add or remove elements from an array. It modifies the array in place and returns an array containing the removed elements (if any)
<pre>
array.splice(startIndex, deleteCount, item1, item2, ...)
<br>
const arr = [1, 2, 3, 4, 5];
// Remove two elements starting from index 2, and add two elements in their place
const removed = arr.splice(2, 2, 'a', 'b');
console.log(arr); // Output: [1, 2, 'a', 'b', 5]
console.log(removed); // Output: [3, 4]
// added 8 at index 1
arr.splice(1,0,'8');
console.log(arr); // Output: [1, '8', 2, 'a', 'b', 5]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="toLocaleString"><li>toLocaleString()</li></span>

The `toLocaleString()` method is used to return a string representing the elements of an array in a localized format.
<pre>
array.toLocaleString([locales[, options]])
<br>
const array1 = [1, 'a', new Date('21 Dec 1997 14:12:00 UTC')];
const localeString = array1.toLocaleString('en', { timeZone: 'UTC' });
console.log(localeString);
<br>
const prices = ["￥7", 500, 8123, 12];
prices.toLocaleString("ja-JP", { style: "currency", currency: "JPY" });  // "￥7,￥500,￥8,123,￥12"
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="toString"><li>toString()</li></span>

The `toString()` method returns a string representing the specified array and its elements
<pre>
const array1 = [1, 2, "a", "1a"];
console.log(array1.toString()); // "1,2,a,1a"
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="unshift"><li>unshift()</li></span>

The `unshift()` method adds one or more elements to the beginning of an array and returns the new length of the array.
<pre>
let arr = [4, 5, 6];
arr.unshift(1, 2, 3);
console.log(arr);  // [1, 2, 3, 4, 5, 6]
<br>
arr = [4, 5, 6]; 
arr.unshift(1);
arr.unshift(2);
arr.unshift(3);
console.log(arr); // [3, 2, 1, 4, 5, 6]
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

<span id="values"><li>values()</li></span>

The `values()` method is used to return an iterator of the values in an array. It returns a new iterator object that contains the values of each element in the array
<pre>
array.values()
<br>
const array = ['a', 'b', 'c'];
const iterator = array.values();
console.log(iterator.next().value); // Output: "a"
console.log(iterator.next().value); // Output: "b"
console.log(iterator.next().value); // Output: "c"
</pre>
<p align='right'><a href="#top">&#8593; Back to Top</a></p>

 