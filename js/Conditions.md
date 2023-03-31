<h2>Conditions and Loops</h2>
<p align='right'><a href="https://github.com/nrjp/javascript">Index</a></p>

<p> conditions are used to perform different actions based on different conditions </p>

<ol>
<li><a href="#for">for</a></li>
<li><a href="#in">for in</a></li>
<li><a href="#of">for of</a></li>
<li><a href="#while">while</a></li>
<li><a href="#do">do while</a></li>
<li><a href="#if">if else</a></li>
<li><a href="#elseif">else if
<li><a href="#Ternary">Ternary operator</a></li>
<li><a href="#Switch">Switch // statement</a></li>
<li><a href="#trycatch">try...catch</a></li>
<li><a href="#break">break continue</a></li>
<li><a href="#continue">continue continue</a></li>
<li><a href="#return">return</a></li>
<li><a href="#throw">throw</a></li>
</ol>


<ol>
    <span id="for"><li>for</li></span>
    The for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons
    <br>
    <pre>
    for (initialization; condition; afterthought)
    // statement
    <br>
    for (let i = 0; i < 10; i++) {
    console.log(i);
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="in"><li>for in</li></span>
    for in iterates over all the enumerable properties of an object and executes a block of code for each property.
    <br>
    <pre>
    for (variable in object)
      // statement
    <br>
    const person = { name: "John", age: 30, city: "New York" };
    for (let property in person) {
    console.log(`${property}: ${person[property]}`);
    }
    </pre>
    <br>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
     <span id="of"><li>for of</li></span>
    <br>
    for of loop is used to iterate over iterable objects such as arrays, strings, and other collections that provide an iterator method.
    <pre>
    for (variable of object)
        // statement
    <br>
    const arr = [1, 2, 3, 4];
    for (let element of arr) {
    console.log(element);
    }
    </pre>
    <br>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="while"><li>while</li></span>
    <br>
    <pre>
    while (condition)
    // statement
    <br>
    let i = 0;
    while (i < 10) {
    console.log(i);
    i++;
    }
    </pre>
    <br>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="do"><li>do while</li></span>
    <br>
    <pre>
    do
    // statement
    while (condition);
    <br>
    let i = 0;
    do {
    console.log(i);
    i++;
    } while (i < 10);
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="if"><li>if else</li></span>
    <br>
    <pre>
    if (condition) {
    // statement1;
    } else {
    // statement2;
    }
    <br>
    const age = 16;
    if (age >= 18) {
    console.log("You are an adult");
    } else {
    console.log("You are a teenager");
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="elseif"><li>else if</li></span>
    <br>
    <pre>
    if (condition) {
    // statement1;
    } else if{
    // statement2;
    } else {
    // statement3;
    }
    <br>
    const time = 10;
    if (time < 12) {
    console.log("Good morning");
    } else if (time < 18) {
    console.log("Good afternoon");
    } else {
    console.log("Good evening");
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="Ternary"><li>Ternary operator</li></span>
    <br>
    <pre>
    const age = 18;
    const status = age >= 18 ? "adult" : "teenager";
    console.log(status);
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="Switch"><li>Switch statement</li></span>
    <br>
    <pre>
    switch(expression){
    case1:
        // statement1
        break;
    case1:
        // statement1
        break;
    }
    <br>
    const day = "Monday";
    switch (day) {
    case "Monday":
        console.log("Today is Monday");
        break;
    case "Tuesday":
        console.log("Today is Tuesday");
        break;
    default:
        console.log("Today is some other day");
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="trycatch"><li>try...catch</li></span>
    <br>
    <pre>
   try {
    // code that may throw an exception
    } catch (error) {
    // code to handle the exception
    } finally {
    // code that is always executed, regardless of whether or not an exception was thrown
    }
    <br>
    const jsonString = '{ "name": "John", "age": }';
    try {
    const person = JSON.parse(jsonString);
    console.log(person);
    } catch (error) {
    console.error('Error:', error);
    } finally {
    console.log('Parsing complete.');
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="break"><li>break statement</li></span>
    <br>
    <pre>
    break;
    break label;
    <br>
    function testBreak(x) {
    let i = 0;
    <br>
    while (i < 6) {
        if (i === 3) {
        break;
        }
        i += 1;
    }
    return i * x;
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="continue"><li>continue statement</li></span>
    <br>
    <pre>
    continue;
    continue label;
    <br>
    let i = 0;
    let n = 0;
    <br>
    while (i < 5) {
    i++;
    if (i === 3) {
        continue;
    }
    n += i;
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="return"><li>return statement</li></span>
    <br>
    <pre>
    return;
    return expression;
    <br>
    function testBreak(x) {
    let i = 0;
    <br>
    while (i < 6) {
        if (i === 3) {
        break;
        }
        i += 1;
    }
    return i * x;
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    <span id="throw"><li>throw statement</li></span>
    <br>
    <pre>
    throw expression;
    <br>
    function divide(a, b) {
    if (b === 0) {
        throw new Error("Division by zero.");
    }
    return a / b;
    }
    try {
    let result = divide(10, 0);
    console.log(result);
    } catch (error) {
    console.log("An error occurred: " + error.message);
    }
    </pre>
        <p align='right'><a href="#top">&#8593; Back to Top</a></p>
    
    
</ol>