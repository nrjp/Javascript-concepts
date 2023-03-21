<h2>Operators</h2>

<h3>Types of operators</h3>
<ol>
    <li>Arithmetic operators</li>
    <br>
    <ul>
        <li>+ (addition)</li>
        <li>- (subtraction)</li>
        <li>* (multiplication)</li>
        <li>/ (division)</li>
        <li>% (modulus)</li>
        <li>++ (increment)</li>
        <li>-- (decrement)</li>
        <br>
    </ul>
    <br>
    <pre>
        let x = 10;
        let y = 5;
        <br>
        console.log(x + y); 
        console.log(x - y); 
        console.log(x * y); 
        console.log(x / y); 
        console.log(x % y);
        console.log(x ++ y);
        console.log(x -- y);
    </pre>
    <br>
    <li>Comparison  operators</li>
    <br>
    <ul>
        <li>== (equality)
        <li>=== (strict equality)</li>
        <li>!= (inequality)</li>
        <li>!== (strict inequality)</li>
        <li>< (less than)</li>
        <li>> (greater than)</li>
        <li><= (less than or equal to)</li>
        <li>>= (greater than or equal to)</li>
    </ul>
    <br>
    <pre>
        let x = 10;
        let y = 5;
        <br>
        console.log(x == y); 
        console.log(x === y);
        console.log(x != y); 
        console.log(x !== y); 
        console.log(x < y); 
        console.log(x > y); 
        console.log(x <= y); 
        console.log(x >= y);
    </pre>
    <br>
    <li>Logical operators</li>
    <br>
    <ul>
        <li>&& (logical AND)</li>
        <li>|| (logical OR)</li>
        <li>! (logical NOT)</li>
    </ul>
    <br>
    <pre>
        let x = 10;
        let y = 5;
        <br>
        console.log(x > 5 && y < 10); 
        console.log(x > 5 || y > 10); 
        console.log(!(x > 5)); 
    </pre>
    <br>
    <li>Assignment operators</li>
    <br>
    <ul>
        <li>= (assignment)</li>
        <li>+= (add and assign)</li>
        <li>-= (subtract and assign)</li>
        <li>*= (multiply and assign)</li>
        <li>/= (divide and assign)</li>
        <li>%= (modulus and assign)</li>
        <li><<= (left shift and assign)</li>
        <li>>>= (right shift and assign)</li>
        <li>>>>= (unsigned right shift and assign)</li>
        <li>&= (bitwise AND and assign)</li>
        <li>^= (bitwise XOR and assign)</li>
        <li>|= (bitwise OR and assign)</li>
    </ul>
    <br>
    <pre>
        let x = 10;
        let y = 5;
        <br>
        x += y; # x = x + y
        console.log(x); 
        <br>
        x -= y; # x = x - y
        console.log(x); 
    </pre>
    <br>
    <li>Conditional (Ternary) operators</li>
    <br>
    <ul>
        <li>? : (conditional operator)</li>
    </ul>
    <br>
    <pre>
        condition ? val1 : val2
        const status = age >= 18 ? "adult" : "minor";
    </pre>
    <br>
    <li>Bitwise operators</li>
    <br>
    <ul>
        <li>& (bitwise AND)</li>
        <li>| (bitwise OR)</li>
        <li>^ (bitwise XOR)</li>
        <li>~ (bitwise NOT)</li>
        <li><< (left shift)</li>
        <li>>> (right shift)</li>
        <li>>>> (unsigned right shift)</li>
    </ul>
    <br>
</ol>

<br />

<h3>Equality Comparisons</h3>
In JavaScript, there are two types of equality comparisons<br>
<ul>
    <li>strict equality</li>
    <br>
    <p>Strict equality is checked using the triple equals operator (===)
    It compares two values for both their value and their data type</p>
    <br>
    <pre>
    1 === 1 // true
    1 === "1" // false
    </pre>
    <br>
    <li>abstract equality</li>
    <br>
    <p>Abstract equality, on the other hand, is checked using the double equals operator (==)
    It compares two values for their value only, without taking into account their data type</p>
    <br>
    <pre>
    1 == 1 // true
    1 == "1" // true
    </pre>
</ul>

