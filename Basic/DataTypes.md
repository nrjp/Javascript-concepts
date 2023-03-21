<h2>Data Types </h2>

- JavaScript is a dynamically typed language, meaning that you do not need to specify a data type when declaring a variable.
- The data type is automatically determined based on the value assigned to the variable. 
- Additionally, JavaScript supports type coercion, which means it will automatically convert data types when necessary to perform    operations.

<h3>JavaScript has several built-in data types that allow you to store and manipulate different kinds of data.</h3>
<br>
<h4>Primitive types</h4>
<ol>
    <li>number</li>
    <pre>
    # Number
    let age = 27;
    console.log(typeof age);
    </pre>
    <li>string</li>
    <pre>
    # string
    let name = 'John';
    console.log(typeof name);
    </pre>
    <li>boolean</li>
    <pre>
    # boolean
    let isStudent = true;
    console.log(typeof isStudent);
    </pre>
    <li>null</li>
    <pre>
    # null
    let myVar = null;
    console.log(typeof myVar); 
    </pre>
    <li>undefined</li>
    <pre>
    # undefined
    let myVar;
    console.log(typeof myVar); 
    </pre>
    <li>symbol</li>
    <pre>
    # symbol
    const id = Symbol('id');
    console.log(typeof id);
    </pre>
</ol>
<br>
<h4>Object types</h4>
<ol>
    <li>object</li>
    <pre>
    // object
    let person = { name: 'John', age: 27 };
    console.log(typeof person);
    </pre>
    <li>array</li>
    <pre>
    # array
    let numbers = [1, 2, 3];
    console.log(typeof numbers);
    </pre>
    <li>function</li>
    <pre>
    # function
    function add(a, b) { return a + b; }
    console.log(typeof add);
    </pre>
</ol>
<br>

<h4>typeof</h4>
typeof is a built-in operator in JavaScript that returns the data type of an operand.
<pre>
typeof "hello"; 
</pre>
<h4>typeof null returns "object"</h4>
<br />

<h4>Coercion</h4>
 <p>Coercion in JavaScript refers to the automatic type conversion.
 There are two types of coercion in JavaScript</p>
 <ul>
   <li> implicit </li> 
   Implicit coercion happens automatically 
   <pre>
        const value1 = "5";
        const value2 = 9;
        let sum = value1 + value2;
        console.log(sum);
    </pre>
   <li> explicit </li>
   In Explicit coercion one data type converts to another using functions or operators
   <pre>
        const value1 = "5";
        const value2 = 9;
        let newValue1 = Number(value1);
        let sum = value1 + value2;
        console.log(sum);
    </pre>
</ul>
