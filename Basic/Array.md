<h2>Array</h2>

 <p>Array is a data structure used to store multiple values in a single variable. Arrays are declared using square brackets ([]), with each value separated by a comma</p>


| Method         | Description                                                  |
|----------------|--------------------------------------------------------------|
| at()          | Returns the element at the specified position in an array    |
| concat()      | Joins two or more arrays and returns a new array             |
| copyWithin()  | Copies elements from an array to another position in the same array |
| entries()     | Returns an array iterator object with key/value pairs        |
| every()       | Tests whether all elements in an array pass a specified test  |
| fill()        | Fills the elements in an array with a static value            |
| filter()      | Creates a new array with all elements that pass a specified test |
| find()        | Returns the value of the first element that passes a specified test |
| findIndex()   | Returns the index of the first element that passes a specified test |
| findLast()    | Returns the value of the last element that passes a specified test |
| findLastIndex() | Returns the index of the last element that passes a specified test |
| flat()        | Returns a new array with all sub-array elements concatenated into it |
| flatMap()     | Returns a new array with the results of calling a function for every element |
| forEach()     | Calls a function for each element in an array                 |
| from()        | Creates a new Array instance from an array-like or iterable object |
| group()       | (Experimental) Returns an array of arrays grouped by a given criterion |
| groupToMap()  | (Experimental) Returns a Map object with arrays grouped by a given criterion |
| includes()    | Determines whether an array contains a specified element     |
| indexOf()     | Returns the index of the first occurrence of a specified value in an array |
| isArray()     | Determines whether a value is an array                        |
| join()        | Joins all elements of an array into a string                  |
| keys()        | Returns an array iterator with the keys of an array           |
| lastIndexOf() | Returns the index of the last occurrence of a specified value in an array |
| map()         | Creates a new array with the results of calling a function for every element |
| of()          | Creates a new Array instance with a variable number of arguments |
| pop()         | Removes the last element from an array and returns it         |
| push()        | Adds one or more elements to the end of an array  |
| reduce()      | Reduces an array to a single value by calling a function for each element |
| reduceRight() | Reduces an array to a single value (from right-to-left) by calling a function for each element |
| reverse()     | Reverses the order of the elements in an array |
| shift()       | Removes the first element from an array and returns it |
| slice()	    | Extracts a section of an array and returns a new array |
| some()	    | Tests whether at least one element in an array passes a specified test
| sort()	    | Sorts the elements of an array |
| splice()	    | Adds or removes elements from an array |
| toLocaleString()| Returns a string representation of the array, formatted according to the current locale |
| toString()	| Returns a string representation of an array |
| unshift()	    | Adds one or more elements to the beginning of an array |
| values()	    | Returns an array iterator with the values of an |

 

<br />
- concat()<br>
The concat() method is used to merge two or more arrays

const letters = ["a", "b", "c"];
const numbers = [1, 2, 3];

const alphaNumeric = letters.concat(numbers);
console.log(alphaNumeric);
// results in ['a', 'b', 'c', 1, 2, 3]

- copyWithin()<br>
The copyWithin() method shallow copies part of an array to another location in the same array and returns it without modifying its length

console.log([1, 2, 3, 4, 5].copyWithin(-2));
// [1, 2, 3, 1, 2]

console.log([1, 2, 3, 4, 5].copyWithin(0, 3));
// [4, 5, 3, 4, 5]

console.log([1, 2, 3, 4, 5].copyWithin(0, 3, 4));
// [4, 2, 3, 4, 5]

console.log([1, 2, 3, 4, 5].copyWithin(-2, -3, -1));
// [1, 2, 3, 3, 4]

- entries()<br>
The entries() method returns a new Array Iterator object that contains the key/value pairs for each index in the array

const a = ["a", "b", "c"];

for (const [index, element] of a.entries()) {
  console.log(index, element);
}

// 0 'a'
// 1 'b'
// 2 'c'

- every()<br>
The every() method tests whether all elements in the array pass the test implemented by the provided function

function isBigEnough(element, index, array) {
  return element >= 10;
}
[12, 5, 8, 130, 44].every(isBigEnough); // false
[12, 54, 18, 130, 44].every(isBigEnough); // true


- fill()<br>
The fill() method changes all elements in an array to a static value, from a start index (default 0) to an end index (default array.length)

console.log([1, 2, 3].fill(4)); // [4, 4, 4]
console.log([1, 2, 3].fill(4, 1)); // [1, 4, 4]
console.log([1, 2, 3].fill(4, 1, 2)); // [1, 4, 3]
console.log([1, 2, 3].fill(4, 1, 1)); // [1, 2, 3]
console.log([1, 2, 3].fill(4, 3, 3)); // [1, 2, 3]
console.log([1, 2, 3].fill(4, -3, -2)); // [4, 2, 3]
console.log([1, 2, 3].fill(4, NaN, NaN)); // [1, 2, 3]
console.log([1, 2, 3].fill(4, 3, 5)); // [1, 2, 3]
console.log(Array(3).fill(4)); // [4, 4, 4]



- filter()<br>
The filter() method creates a shallow copy of a portion of a given array, filtered down to just the elements from the given array that pass the test implemented by the provided function.


// Arrow function
filter((element) => { /* … */ })
filter((element, index) => { /* … */ })
filter((element, index, array) => { /* … */ })

// Callback function
filter(callbackFn)
filter(callbackFn, thisArg)

// Inline callback function
filter(function (element) { /* … */ })
filter(function (element, index) { /* … */ })
filter(function (element, index, array) { /* … */ })
filter(function (element, index, array) { /* … */ }, thisArg)


- find()<br>
The find() method returns the first element in the provided array that satisfies the provided testing function
- findIndex()
- findLast()
- findLastIndex()
- flat()
- flatMap()
- forEach()
- Array.from()
- group() (Experimental)
- groupToMap() (Experimental)
- includes()
- indexOf()
- Array.isArray()
- join()
- keys()
- lastIndexOf()
- map()
- Array.of()
- pop()
- push()
- reduce()
- reduceRight()
- reverse()
- shift()
- slice()
- some()
- sort()
- splice()
- toLocaleString()
- toString()
- unshift()
- values()

 