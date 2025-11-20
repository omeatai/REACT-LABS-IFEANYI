### [1 - JS Fundamentals - Coding Addict](https://www.codingaddict.io/l/products)

<details>
  <summary>Inline JS</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Hello World</h1>
    <h2>Welcome to my website</h2>
    <button onclick="alert('Button clicked!')">Click Me!</button>
</body>

</html>
```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/883e841e-8bf1-4e68-9254-a18b0168f136" />

</details>

<details>
  <summary>Internal JS</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Hello World</h1>
    <h2>Welcome to my website</h2>
    <button>Click Me!</button>
    <button>Click Me!</button>
    <script>
        document.querySelectorAll('button').forEach(function (button) {
            button.addEventListener('click', function () {
                alert('Button was clicked!');
            });
        });
    </script>
</body>

</html>
```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/7657a6d9-7ad2-4b60-ae66-47f4799ecaa7" />

</details>


<details>
  <summary>External JS</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Hello World</h1>
    <h2>Welcome to my website</h2>
    <button>Click Me!</button>
    <button>Click Me!</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
document.querySelectorAll('button').forEach(function (button) {
            button.addEventListener('click', function () {
                alert('Button was clicked!');
            });
        });
```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/1e148ad8-1bbf-4376-88f8-34ae423f20c0" />

</details>

<details>
  <summary>JS Debugging Functions</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// Javascript debugging functions
// Write function
document.write("<h2>Welcome to my website</h2>");
document.write('<button onclick="alert(\'Button Clicked!\')">Click Me!</button>');

// Alert function
alert("This is an alert message!");

// Console log function
console.log("This is a message in the console.");

// Prompt function
let userName = prompt("Please enter your name:");
console.log("User's name is: " + userName);

// Confirm function
let isConfirmed = confirm("Do you want to proceed?");
console.log("User confirmed: " + isConfirmed);

```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/b42e38e2-3c4c-418d-8c01-b55217141553" />
<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/bd4b06f2-1068-42e7-b823-e8231dc2cf4f" />
<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/f6b4f6d7-d0e7-4926-bd65-9d68424622e6" />
<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/2afeaa83-3965-49d2-9ebe-e3efe2acb362" />

</details>

<details>
  <summary>JS Single and Multi-line Comments</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// Single Line Comment: This is a single line comment in JavaScript
console.log("A single line comment example");

/*
  Multi-line Comment:
  This is a multi-line comment
  in JavaScript
*/
console.log("A multi-line comment example");

```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/a07b35d3-dc3d-48f7-9302-b9bf5ea14297" />

</details>

<details>
  <summary>JS Variables with Const and Let</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
//Variable Declaration and Assignment
let studentName = "John Doe";
let address, zip, state;
let $studentPassword;
const _StudentID = "A123456";

address = "123 Main St";
zip = "12345";
state = "CA";
studentName = "Jane Smith";
$studentPassword = "password123";

console.log(studentName);
console.log(address, zip, state);
console.log("Student Password:", $studentPassword);
console.log("Student ID:", _StudentID);
```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/4c69f881-4bcd-456e-8805-38af29996494" />

</details>

<details>
  <summary>JS String Concatenation</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const firstName = "John";
const lastName = "Doe";
let fullName = firstName + " " + lastName;
console.log("Hello, your full name is : " + fullName);

const website = "youtube";
const url = "https://www." + website + ".com";
console.log("Visit website at : " + url);
```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/94813faf-d429-4821-bbeb-e0c9c46c2dd7" />

</details>

<details>
  <summary>JS Type Conversion and Data Types</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
/*
DATA TYPES IN JAVASCRIPT
### Primitive - String, Number, Boolean, Null, Undefined, Symbol
### Non-Primitive (Object) - Object, Array, Function
*/

// String
const fullName = "John Doe";
console.log("Hello, " + fullName);
console.log(`Hello, ${fullName}`);
console.log("typeof: ", typeof fullName);

// Number
const age = 30;
const height = 5.9;
console.log("Age:", age);
console.log("Height:", height);
console.log("typeof: ", typeof age);
console.log("typeof: ", typeof height);

// Boolean
const isStudent = false;
console.log("Is Student:", isStudent);
console.log("typeof: ", typeof isStudent);

// Null
const middleName = null;
console.log("Middle Name:", middleName);
console.log("typeof: ", typeof middleName);

// Undefined
let address;
console.log("Address:", address);
console.log("typeof: ", typeof address);

// Symbol
const uniqueId = Symbol("id");
console.log("Unique ID:", uniqueId.toString());
console.log("typeof: ", typeof uniqueId);

// Object
const person = {
    name: "Jane Doe",
    age: 25,
    isEmployed: true
};
console.log("Person Object:", person);
console.log("typeof: ", typeof person);

// Array
const colors = ["Red", "Green", "Blue"];
console.log("Colors Array:", colors);
console.log("typeof: ", typeof colors);

// Function
function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("Alice"));
console.log("typeof: ", typeof greet);

// Convert string to number
const number1 = "5";
const number2 = 10;
const sum = Number(number1) + number2;
const sum2 = parseInt(number1) + number2;

console.log("The sum is:", sum);
console.log("The sum2 is:", sum2);

```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/807d915c-9e05-40a7-96dd-4478dcd05640" />

</details>

<details>
  <summary>JS Arrays</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const friends = ['Alice', 'Bob', 'Charlie', 45, true, undefined, null];
console.log(friends);

// Accessing elements
console.log(friends[0]); // Alice
console.log(friends[3]); // 45
console.log(friends[7]); // undefined

// Modifying elements
friends[1] = 'Bobby';
console.log(friends); // ['Alice', 'Bobby', 'Charlie', 45, true, undefined, null]

// Adding new elements
friends.push('David');
console.log(friends); // ['Alice', 'Bobby', 'Charlie', 45, true, undefined, null, 'David']

// Adding new elements at the beginning
friends.unshift('Zara');
console.log(friends); // ['Zara', 'Alice', 'Bobby', 'Charlie', 45, true, undefined, null, 'David']

// Adding new elements at a specific index
friends.splice(3, 0, 'Eve'); // Adding 'Eve' at index 3
console.log(friends); // ['Zara', 'Alice', 'Bobby', 'Eve', 'Charlie', 45, true, undefined, null, 'David']

// Removing the last element
friends.pop();
console.log(friends); // ['Zara', 'Alice', 'Bobby', 'Eve', 'Charlie', 45, true, undefined, null]

// Removing the first element
friends.shift();
console.log(friends); // ['Alice', 'Bobby', 'Eve', 'Charlie', 45, true, undefined, null]

// Removing elements from a specific index
friends.splice(2, 2); // Removing 2 elements starting from index 2
console.log(friends); // ['Alice', 'Bobby', 45, true, undefined, null]

// Checking the length of the array
console.log(friends.length); // 6

// Iterating through the array
for (let i = 0; i < friends.length; i++) {
    console.log(friends[i]);
}

// Using for...of loop
for (const friend of friends) {
    console.log(friend);
}

// Checking if an element exists
console.log(friends.includes('Charlie')); // true
console.log(friends.includes(45)); // true

// Finding the index of an element
console.log(friends.indexOf('Alice')); // 0
console.log(friends.indexOf('David')); // -1
```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/3829796f-9989-474b-b163-240dfbeff5ce" />

</details>

<details>
  <summary>JS Functions</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// JS Function
function hello(){
    console.log("Hello, Bob!");
    console.log("Hello, Anna!");
    console.log("Hello, Charlie!");
    return
}

hello();
hello();

// Function with Parameters 1
function greetPerson(name="Peter") {
    console.log("Hello my friend, " + name + "!");
    return;
}

greetPerson();
greetPerson("Bob");
greetPerson("Anna");
greetPerson("Charlie");

// Function with Parameters 2
function displayFriends(friends) {
    let allFriends = [];
    friends.forEach(function(friend) {
        console.log(friend.name);
        allFriends.push(friend.name);
    });
    return allFriends;
}

const myFriends = [
    { name: 'Alice' },
    { name: 'Bob' },
    { name: 'Charlie' }
];

const myGroupedFriends = displayFriends(myFriends);
console.log(myGroupedFriends);

```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/faea414f-83e0-48b4-8c7f-14895baee1bf" />

</details>

<details>
  <summary>JS Objects</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// JS Objects
const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    education: false,
    married: true,
    siblings: ["Jane", "Mark", "Paul"],
    fullName: function() {
        return this.firstName + " " + this.lastName;
    },
    greeting() {
        console.log("Hello, " + this.firstName + "!");
    }
};

// Accessing object properties
const age = person.age;
console.log("Age:", age); // Age: 30

// Calling object method
console.log("Full Name:", person.fullName());  // Full Name: John Doe

// Modifying object properties
person.age = 31;
console.log("Updated Age:", person.age);       // Updated Age: 31

// Adding new property
person.gender = "Male";
console.log("Gender :", person.gender);          // Gender : Male

// Deleting a property
delete person.lastName;
console.log("Last Name after deletion:", person.lastName); // Last Name after deletion: undefined

// Iterating over object properties
for (let key in person) {
    console.log(key + ": " + person[key]);
}

// Checking if a property exists
console.log("Has age property:", 'age' in person); // Output: true
console.log("Has lastName property:", 'lastName' in person); // Output: false

// Object.keys() method
const keys = Object.keys(person);
console.log("Object Keys:", keys); // ['firstName', 'age', 'education', 'married', 'siblings', 'fullName', 'greeting', 'gender']

// Object.values() method
const values = Object.values(person);
console.log("Object Values:", values); // [ 'John', 31, false, true, [ 'Jane', 'Mark', 'Paul' ], [Function: fullName], [Function: greeting], 'Male' ]

// Object.entries() method
const entries = Object.entries(person);
console.log("Object Entries:", entries); // [ [ 'firstName', 'John' ], [ 'age', 31 ], [ 'education', false ], [ 'married', true ], [ 'siblings', [Array] ], [ 'fullName', [Function: fullName] ], [ 'greeting', [Function: greeting] ], [ 'gender', 'Male' ] ]

// Creating a new object using Object.create()
const employee = Object.create(person);
employee.jobTitle = "Software Engineer";
console.log("Employee Job Title:", employee.jobTitle);   // Output: Software Engineer
console.log("Employee Age:", employee.age);             // Output: 31

// Checking prototype chain
console.log("Is employee prototype of person?", person.isPrototypeOf(employee)); // Output: true

// Freezing the object
Object.freeze(person);
person.age = 35; // This will not change the age property
console.log("Age after freeze attempt:", person.age); // Output: 31

// Sealing the object
Object.seal(person);
delete person.firstName; // This will not delete the firstName property
console.log("First Name after seal attempt:", person.firstName); // Output: John

// Preventing extensions
Object.preventExtensions(person);
person.middleName = "Michael"; // This will not add a new property
console.log("Middle Name after preventExtensions attempt:", person.middleName); // Output: undefined

```

<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/e8c45b37-fdbd-4990-adb2-5c6789cdea51" />

</details>

<details>
  <summary>JS If, Else If and Switch Statements</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// if conditions
if (true) {
    console.log("This condition is true.");
} else {
    console.log("This condition is false.");
}

const value1 = 10;
const value2 = 20;

if (value1 < value2) {
    console.log("value1 is less than value2.");
} else if (value1 > value2) {
    console.log("value1 is greater than value2.");
} else {
    console.log("value1 is equal to value2.");
}

const studentName = "John";
const age = 25;

if (studentName === "John" && age === 25) {
    console.log("Name is John and age is 25.");
}
if (studentName === "John" || age === 30) {
    console.log("Either name is John or age is 30.");
}

// switch case
let fruit = "apple";
switch (fruit) {
    case "banana":
        console.log("This is a banana.");
        break;
    case "apple":
        console.log("This is an apple.");
        break;
    default:
        console.log("Unknown fruit.");
}

// Voting System
const person1 = { name: "Alice", age: 25, status: "resident" };
const person2 = { name: "Bob", age: 17, status: "tourist" };

if (person1.age >= 18 && person1.status === "resident") {
    console.log(`${person1.name} is eligible to vote.`);
} else {
    console.log(`${person1.name} is not eligible to vote.`);
}

if (person2.age >= 18 && person2.status === "resident") {
    console.log(`${person2.name} is eligible to vote.`);
} else {
    console.log(`${person2.name} is not eligible to vote.`);
}

switch (person1.age >= 18 && person1.status === "resident") {
    case true:
        console.log(`${person1.name} can vote.`);
        break;
    case false:
        console.log(`${person1.name} cannot vote.`);
        break;
}

switch (person2.age >= 18 && person2.status === "resident") {
    case true:
        console.log(`${person2.name} can vote.`);
        break;
    case false:
        console.log(`${person2.name} cannot vote.`);
        break;
}

```

<img width="1555" height="1077" alt="image" src="https://github.com/user-attachments/assets/7aaac0a4-eeea-456e-b00a-100247812b33" />

</details>


<details>
  <summary>JS While Loop</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// while loops
let count = 0;
while (count <= 5) {
    console.log("Count is: " + count);
    count++;
}

```

<img width="1555" height="1077" alt="image" src="https://github.com/user-attachments/assets/f7f082bf-b598-42ee-b940-aa53ddc36882" />

</details>

<details>
  <summary>JS Do While Loop</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// do while loops
let money = 0;

do {
  console.log("You have $" + money + " available.");
  money++;
} while (money < 10);
console.log("End at: $" + money + ".");

```

<img width="1871" height="1338" alt="image" src="https://github.com/user-attachments/assets/911b0fb6-4e34-4c03-a655-49e0af70587f" />

</details>

<details>
  <summary>JS For Loop</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// for loops
for (let i = 0; i < 10; i++) {
    console.log("Iteration number: " + i);
}

for (let j = 10; j > 0; j--) {
    console.log("Countdown: " + j);
}
```

<img width="1555" height="1074" alt="image" src="https://github.com/user-attachments/assets/26e82425-0583-44e9-8548-03cb712e8034" />

</details>

<details>
  <summary>JS String Properties and Methods</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// string properties and methods
let text = " Sample Text";

console.log(text.length); // length property
console.log(text.toLowerCase()); // toLowerCase() method
console.log(text.toUpperCase()); // toUpperCase() method
console.log(text.charAt(3)); // charAt() method
console.log(text.charAt(text.length - 1)); // charAt() method for last character
console.log(text.charCodeAt(2)); // charCodeAt() method
console.log(text.indexOf("T")); // indexOf() method
console.log(text.lastIndexOf("e")); // lastIndexOf() method

console.log(text.includes("Text")); // includes() method
console.log(text.trim()); // trim() method
console.log(text.split(" ")); // split() method
console.log(text.slice(1, 6)); // slice() method
console.log(text.substring(1, 6)); // substring() method
console.log(text.replace("Sample", "Example")); // replace() method
console.log(text.concat(" Added Text")); // concat() method
console.log(text.repeat(2)); // repeat() method
console.log(text.startsWith(" S")); // startsWith() method
console.log(text.endsWith("t")); // endsWith() method

console.log(text.padStart(15, "-")); // padStart() method
console.log(text.padEnd(15, "*")); // padEnd() method
console.log(text.match(/e/g)); // match() method
console.log(text.normalize()); // normalize() method
console.log(text.valueOf()); // valueOf() method
console.log(text.localeCompare(" Another Text")); // localeCompare() method
console.log(String.fromCharCode(83, 97, 109, 112, 108, 101)); // fromCharCode() method

```

<img width="1555" height="1074" alt="image" src="https://github.com/user-attachments/assets/61153410-e9f9-4e72-9ece-09190afbb9a5" />

</details>

<details>
  <summary>JS String Literals</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// string Literals

const studentName = "John Doe";
const age = 25;
const sentence =
  "Hey there! My name is " + studentName + " and I am " + age + " years old.";

const value = `Hey there! My name is ${studentName} and I am ${age} years old.`;

console.log(sentence);
console.log(value);

```

<img width="2187" height="1331" alt="image" src="https://github.com/user-attachments/assets/77980cf5-0e5d-43bc-b30f-ce111a4b5ea6" />

</details>

<details>
  <summary>JS String Parameters as Objects</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// Basic Function parameters
function fullName(firstName, lastName) {
  return `${firstName} ${lastName}`.toUpperCase();
}

console.log(fullName("John", "Doe")); // Output: "JOHN DOE"
console.log(fullName("Jane", "Smith")); // Output: "JANE SMITH"

// Object Destructuring in Function parameters
function fullName2({ firstName, lastName }) {
  return `${firstName} ${lastName}`.toUpperCase();
}

console.log(fullName2({ firstName: "John", lastName: "Doe" })); // Output: "JOHN DOE"
console.log(fullName2({ firstName: "Jane", lastName: "Smith" })); // Output: "JANE SMITH"

```

<img width="2187" height="1331" alt="image" src="https://github.com/user-attachments/assets/7cf226d9-c142-43e6-8830-dc67b00bb9ba" />

</details>

<details>
  <summary>JS Array Properties and Methods</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
//JS Array Properties and Methods
let fruits = ["Apple", "Banana", "Cherry"];

// Length Property
fruits = ["Apple", "Banana", "Cherry"];
console.log("Number of fruits:", fruits.length); // Output: 3

// At Method
fruits = ["Apple", "Banana", "Cherry"];
let firstFruitAt = fruits.at(0);
let lastFruitAt = fruits.at(-1);
console.log("First fruit using at():", firstFruitAt); // Output: "Apple"
console.log("Last fruit using at():", lastFruitAt); // Output: "Cherry"

// Push Method
fruits = ["Apple", "Banana", "Cherry"];
fruits.push("Date");
console.log("After push:", fruits); // Output: ["Apple", "Banana", "Cherry", "Date"]

// Pop Method
fruits = ["Apple", "Banana", "Cherry"];
let lastFruit = fruits.pop();
console.log("Popped fruit:", lastFruit); // Output: "Cherry"
console.log("After pop:", fruits); // Output: ["Apple", "Banana"]

// Shift Method
fruits = ["Apple", "Banana", "Cherry"];
let firstFruit = fruits.shift();
console.log("Shifted fruit:", firstFruit); // Output: "Apple"
console.log("After shift:", fruits); // Output: ["Banana", "Cherry"]

// Unshift Method
fruits = ["Apple", "Banana", "Cherry"];
fruits.unshift("Apricot");
console.log("After unshift:", fruits); // Output: ['Apricot', 'Apple', 'Banana', 'Cherry']

// IndexOf Method
fruits = ["Apple", "Banana", "Cherry"];
let index = fruits.indexOf("Banana");
console.log("Index of Banana:", index); // Output: 1

// Slice Method
fruits = ["Apple", "Banana", "Cherry"];
let citrusFruits = fruits.slice(0, 2);
console.log("Sliced fruits:", citrusFruits); // Output: ["Apple", "Banana"]

// Splice Method
fruits = ["Apple", "Banana", "Cherry"];
let splicedFruit = fruits.splice(1, 1, "Blueberry", "Apricot");
console.log("splicedFruit:", splicedFruit); // Output: ['Banana']
console.log("After splice:", fruits); // Output: ['Apple', 'Blueberry', 'Apricot', 'Cherry']

// Join Method
fruits = ["Apple", "Banana", "Cherry"];
let fruitString = fruits.join(", ");
console.log("Joined fruits:", fruitString); // Output: "Apple, Banana, Cherry"

// Reverse Method
fruits = ["Apple", "Banana", "Cherry"];
fruits.reverse();
console.log("Reversed fruits:", fruits); // Output: ["Cherry", "Banana", "Apple"]

// Sort Method
fruits = ["Cherry", "Banana", "Apple"];
fruits.sort();
console.log("Sorted fruits:", fruits); // Output: ["Apple", "Banana", "Cherry"]

// Concat Method
fruits = ["Apple", "Banana", "Cherry"];
let moreFruits = ["Grapes", "Peach"];
let combinedFruits = fruits.concat(moreFruits);
console.log("Combined fruits:", combinedFruits); // Output: ["Apple", "Banana", "Cherry", "Grapes", "Peach"]

// ToString Method
fruits = ["Apple", "Banana", "Cherry"];
let fruitsString = fruits.toString();
console.log("Fruits as string:", fruitsString); // Output: "Apple,Banana,Cherry"

// ForEach Method
fruits = ["Apple", "Banana", "Cherry"];
console.log("Fruits list:");
fruits.forEach(function (fruit) {
  console.log(fruit);
});

// Map Method
fruits = ["Apple", "Banana", "Cherry"];
let fruitFirstChar = fruits.map(function (fruit) {
  return fruit.at(0);
});
console.log("Fruit first characters:", fruitFirstChar); // Output: ["A", "B", "C"]

// Filter Method
fruits = ["Apple", "Banana", "Cherry"];
let longFruits = fruits.filter(function (fruit) {
  return fruit.length > 5;
});
console.log("Long fruits:", longFruits); // Output: ['Banana', 'Cherry']

// Reduce Method
fruits = ["Apple", "Banana", "Cherry"];
let totalLength = fruits.reduce(function (total, fruit) {
  return total + fruit.length;
}, 0);
console.log("Total length of all fruits:", totalLength); // Output: 17

// Find Method
fruits = ["Apple", "Banana", "Cherry"];
let foundFruit = fruits.find(function (fruit) {
  return fruit.startsWith("B");
});
console.log("Found fruit:", foundFruit); // Output: "Banana"

// FindIndex Method
fruits = ["Apple", "Banana", "Cherry"];
let indexOfLongFruit = fruits.findIndex(function (fruit) {
  return fruit.length > 5;
});
console.log("Index of long fruit:", indexOfLongFruit); // Output: 1

// Includes Method
fruits = ["Apple", "Banana", "Cherry"];
let hasCherry = fruits.includes("Cherry");
console.log("Contains Cherry:", hasCherry); // Output: true

// Flat Method
fruits = ["Apple", "Banana", "Cherry"];
let nestedArray = [fruits, ["Mango", "Pineapple"]];
let flatArray = nestedArray.flat();
console.log("Flattened array:", flatArray); // Output: ["Apple", "Banana", "Cherry", "Mango", "Pineapple"]

// FlatMap Method
fruits = ["Apple", "Banana", "Cherry"];
let flatMappedFruits = fruits.flatMap(function (fruit) {
  return [fruit, fruit.length];
});
console.log("Flat mapped fruits:", flatMappedFruits); // Output: ["Apple", 5, "Banana", 6, "Cherry", 6]

// Fill Method
let filledArray = new Array(5).fill("Kiwi");
console.log("Filled array:", filledArray); // Output: ["Kiwi", "Kiwi", "Kiwi", "Kiwi", "Kiwi"]

// Some Method
fruits = ["Apple", "Banana", "Cherry"];
let hasLongFruit = fruits.some(function (fruit) {
  return fruit.length > 5;
});
console.log("Has long fruit:", hasLongFruit); // Output: true

// Every Method
fruits = ["Apple", "Banana", "Cherry"];
let allShortFruits = fruits.every(function (fruit) {
  return fruit.length > 5;
});
console.log("All fruits are short:", allShortFruits); // Output: false


```

<img width="1252" height="946" alt="image" src="https://github.com/user-attachments/assets/d146e945-a13b-4e0d-b3b5-cedc0a0b9857" />

</details>

<details>
  <summary>JS Looping through Arrays</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const names = ["Alice", "Bob", "Charlie", "Diana"];
const lastname = "Smith";

// looping solution 1
const fullNames = names.map((name) => `${name} ${lastname}`);
console.log(fullNames);

// looping solution 2
let fullNames2 = [];
names.forEach((name) => {
  fullNames2.push(`${name} ${lastname}`);
});
console.log(fullNames2);

// looping solution 3
let fullNames3 = [];
for (let i = 0; i < names.length; i++) {
  fullNames3.push(`${names[i]} ${lastname}`);
}
console.log(fullNames3);

// looping solution 4
let fullNames4 = [];
for (const name of names) {
  fullNames4.push(`${name} ${lastname}`);
}
console.log(fullNames4);

// looping solution 5
let fullNames5 = [];
let index = 0;
while (index < names.length) {
  fullNames5.push(`${names[index]} ${lastname}`);
  index++;
}
console.log(fullNames5);

```

<img width="1252" height="912" alt="image" src="https://github.com/user-attachments/assets/2a17a5e5-6145-4bcd-8f03-1800ed5b18bf" />

</details>

<details>
  <summary>JS Using Ternary Operators</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const value = 2 > 1;

if (value) {
  console.log("Condition is true");
} else {
  console.log("Condition is false");
}

// Using Ternary Operator
const result = value ? "Condition is true" : "Condition is false";
console.log(result);

```

<img width="1252" height="912" alt="image" src="https://github.com/user-attachments/assets/4590250d-2289-4d29-ace7-2da59996714f" />

</details>

<details>
  <summary>JS Global and Local Scope</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// Understanding Global vs Local scope in JavaScript
let userName = "Alice";
let age = 25;
console.log("Initial userName: ", userName);
console.log("Initial age: ", age);

function calculate() {
  // some other code
  console.log("call 1: ", userName);
  userName = "Charlie";
  let age = 30;
  console.log("Inside calc function - age: ", age);
}
calculate();

if (true) {
  //some other code
  console.log("call 2: ", userName);
  userName = "David";
  console.log("Outside calc function - age: ", age);
}

console.log("call 3: ", userName);

```

<img width="1474" height="931" alt="image" src="https://github.com/user-attachments/assets/9fa8e445-94ce-410d-b7b7-a2b7caeed934" />

</details>

<details>
  <summary>JS Higher Order and Callback Functions </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
//  Callback function
function morning(name) {
    return `Good morning ${name.toUpperCase()}`;
}
function evening(name) {
    return `Good evening ${name.toUpperCase()}`;
}

// Higher-order function
function greet(name, callback, person) {
    console.log(`${callback(name)}, my name is ${person}.`);
}

// Using the higher-order function with the callback
greet('Alice', morning, 'John');
greet('Bob', evening, 'Peter');
```

<img width="1437" height="1038" alt="image" src="https://github.com/user-attachments/assets/8a93f1fd-c35b-4dc2-93ea-a26dd8e2fb02" />

</details>

<details>
  <summary>JS Array Method: forEach</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// forEach Array Method Example
const people = [
  { name: 'Alice', age: 25, position: 'Developer' },
  { name: 'Bob', age: 30, position: 'Designer' },
  { name: 'Charlie', age: 35, position: 'Manager' }
];

// Method 1: Using a named function
function showPerson(person) {
  console.log(person.name.toUpperCase());
}
people.forEach(showPerson);

// Method 2: Using an anonymous function
people.forEach(function(person) {
    console.log(person.name.toLowerCase());
});

// Output:
// ALICE
// BOB
// CHARLIE
// alice
// bob
// charlie

```

<img width="1437" height="1038" alt="image" src="https://github.com/user-attachments/assets/60e85d4b-7ec9-43ab-ac97-cb5f93597d64" />

</details>

<details>
  <summary>JS Array Method: map</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
</head>

<body>
    <h1>Javascript Basics</h1>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// map Method Example
const people = [
  { name: 'Alice', age: 25, position: 'Developer' },
  { name: 'Bob', age: 30, position: 'Designer' },
  { name: 'Charlie', age: 35, position: 'Manager' }
];

const names = people.map(person => person.name);
const ages = people.map(person => person.age);
const positions = people.map(function(person) {
  return person.position;
});
const updatedPeople = people.map(person => {
  return {
    ...person,
    age: person.age + 100,
    position: 'Senior ' + person.position
  };
});

console.log('Names:', names); // Output: Names: [ 'Alice', 'Bob', 'Charlie' ]
console.log('Ages:', ages); // Output: Ages: [ 25, 30, 35 ]
console.log('Positions:', positions); // Output: Positions: [ 'Developer', 'Designer', 'Manager' ]
console.log('Updated People:', updatedPeople);
// Output: Updated People: [
// { name: 'Alice', age: 125, position: 'Senior Developer' },
// { name: 'Bob', age: 130, position: 'Senior Designer' },
// { name: 'Charlie', age: 135, position: 'Senior Manager' } ]
```

<img width="1437" height="1038" alt="image" src="https://github.com/user-attachments/assets/59aabd87-cb18-4dfa-916d-1fd17584281b" />

</details>

<details>
  <summary>JS Array Method: filter </summary>

### projects-v1/app_js/sample_1/index.html

```html

```

### projects-v1/app_js/sample_1/app.js

```js

```

</details>


















<details>
  <summary>JS Array Method: </summary>

### projects-v1/app_js/sample_1/index.html

```html

```

### projects-v1/app_js/sample_1/app.js

```js

```

</details>




































