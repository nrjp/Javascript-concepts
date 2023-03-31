<h2>Variables</h2>
<p align='right'><a href="https://github.com/nrjp/javascript">Index</a></p>

Variables in Javascript

Variables are use to Store the information

<ul>
    <li>var</li>
    <li>let</li>
    <li>const</li>
</ul>
The var keyword is function-scoped, meaning it is accessible within the function where it is declared. 
Variables declared with let and const are block-scoped, which means they are only accessible within the block where they are declared.
    - within a loop or conditional statement

let keyword creates a mutable variable that can be reassigned a new value
const keyword creates an immutable variable that cannot be reassigned once it is initialized.

<p>
The general rules for constructing names for variables 
</p>
<ol>
    <li>Variable names must start with a letter</li>
    <li>Variable names should be descriptive and give an idea about the data they hold</li>
    <li>Use camelCase convention for variable names</li>
     This means the first word is in lowercase and subsequent words are in uppercase<br>
         Example: firstName, totalAmount, isCompleted
    <li>Variable names are case sensitive</li>
       Example: myVariable and myvariable would be considered as two different variables 
    <li>Avoid using abbreviations or single letters for variable names, except for common abbreviations like i for index in loops or x for coordinates.</li>
</ol>
<br />

<p>var</p>
<pre>
    myName = 'Chris';
    function logName() {
    console.log(myName);
    }
    logName();
    var myName;
</pre>
<p>we can declare the same variable as many times as we like in var, but with let it will not work</p>
<pre>
var myName = 'Chris';
var myName = 'Bob';
<br>
# same result we can get with

let myName = 'Chris';
myName = 'Bob';
</pre>
<br>
const
<pre>const PI = 3.14;</pre>
<br />

| Feature	   | var	         | let	         |  const       | 
|--------------|-----------------|---------------|--------------|
| Scope	       | Function-scoped |  Block-scoped |  Block-scoped|
| Hoisting	   | Yes             |  No           |	No          |
| Reassignment | Yes             |	No           |  No          |
