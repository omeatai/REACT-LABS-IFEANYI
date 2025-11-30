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
// filter Method Example
const people = [
  { name: 'Alice', age: 25, position: 'Developer' },
  { name: 'Bob', age: 30, position: 'Designer' },
  { name: 'Charlie', age: 35, position: 'Manager' }
];

const adults = people.filter(person => person.age >= 30);
console.log('Adults:', adults); // [{ name: 'Bob', age: 30, position: 'Designer' }, { name: 'Charlie', age: 35, position: 'Manager' }]

const developers = people.filter(function(person) {
  return person.position === 'Developer';
});
console.log('Developers:', developers); // [{ name: 'Alice', age: 25, position: 'Developer' }]

```

<img width="1437" height="1038" alt="image" src="https://github.com/user-attachments/assets/0c578ecd-c4c3-48c8-90ee-45503a298a73" />

</details>

<details>
  <summary>JS Array Method: find </summary>

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
// find Method Example
const people = [
  { name: 'Alice', age: 25, position: 'Developer', id: 1 },
  { name: 'Bob', age: 30, position: 'Designer', id: 2 },
  { name: 'Charlie', age: 35, position: 'Manager', id: 3 }
];

const person = people.find((person) => person.position === 'Designer');
console.log(person); // { name: 'Bob', age: 30, position: 'Designer', id: 2 }

const person2 = people.find(function(person) {
  return person.id === 3;
});
console.log(person2); // { name: 'Charlie', age: 35, position: 'Manager', id: 3 }

```

<img width="1437" height="1038" alt="image" src="https://github.com/user-attachments/assets/0875d606-24a2-4a16-adf1-3475a52f2c64" />

</details>

<details>
  <summary>JS Array Method: reduce </summary>

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
// reduce Method Example
const people = [
  { name: 'Alice', age: 25, position: 'Developer', salary: 500, id: 1 },
  { name: 'Bob', age: 30, position: 'Designer', salary: 600, id: 2 },
  { name: 'Charlie', age: 35, position: 'Manager', salary: 1000, id: 3 }
];

const totalSalary = people.reduce((total, person) => {
  console.log(`Current Total: ${total}`);
  console.log(`${person.name}: ${person.salary}`);
  total += person.salary;
  return total;
}, 0);

console.log(`Total Salary: $${totalSalary}`); // Output: Total Salary: $2100
```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/d0a1e775-66f3-4838-90ec-e6f458e84e2f" />

</details>

<details>
  <summary>JS Array Method: Map-2</summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/data.js

```js
// student data
const students = [
  { id: 1, name: 'Alice', age: 25, score: 80, favoriteSubject: "math",},
  { id: 2, name: 'Bob', age: 30, score: 85, favoriteSubject: "history" },
  { id: 3, name: 'Charlie', age: 35, score: 34, favoriteSubject: "art" },
  { id: 4, name: 'David', age: 40, score: 95, favoriteSubject: "math" },
  { id: 5, name: 'Eve', age: 28, score: 88, favoriteSubject: "math" }
];
```

### projects-v1/app_js/sample_1/app.js

```js
console.log(students);

const updatedStudents = students.map((student) => {
  return { ...student, role: "student"};
} )
console.log(updatedStudents);
```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/47abb636-774f-48c8-b2e7-5e1b3b770a08" />

</details>


<details>
  <summary>JS Array Method: Filter-2</summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/data.js

```js
// student data
const students = [
  { id: 1, name: 'Alice', age: 25, score: 80, favoriteSubject: "math",},
  { id: 2, name: 'Bob', age: 30, score: 85, favoriteSubject: "history" },
  { id: 3, name: 'Charlie', age: 35, score: 34, favoriteSubject: "art" },
  { id: 4, name: 'David', age: 40, score: 95, favoriteSubject: "math" },
  { id: 5, name: 'Eve', age: 28, score: 88, favoriteSubject: "math" }
];
```

### projects-v1/app_js/sample_1/app.js

```js
console.log(students);

const filteredStudents = students.filter(student => student.score >= 85);
const filteredStudents2 = students.filter(function(student) {
  if(student.score >= 85){
    return student;
  }
});

console.log(filteredStudents);
console.log(filteredStudents2);
```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/96fb960e-3204-47f1-a185-89499796b3a8" />

</details>

<details>
  <summary>JS Array Method: Find-2 </summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/data.js

```js
// student data
const students = [
  { id: 1, name: 'Alice', age: 25, score: 80, favoriteSubject: "math",},
  { id: 2, name: 'Bob', age: 30, score: 85, favoriteSubject: "history" },
  { id: 3, name: 'Charlie', age: 35, score: 34, favoriteSubject: "art" },
  { id: 4, name: 'David', age: 40, score: 95, favoriteSubject: "math" },
  { id: 5, name: 'Eve', age: 28, score: 88, favoriteSubject: "math" }
];
```

### projects-v1/app_js/sample_1/app.js

```js
console.log(students);

const search = students.find(student => student.id === 1);
const search2 = students.find(student => student.favoriteSubject === 'math');

console.log(search);
console.log(search2);

```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/18155648-d50f-4438-b155-2ee1ecf3a784" />

</details>

 
<details>
  <summary>JS Array Method: Reduce-2 </summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/data.js

```js
// student data
const students = [
  { id: 1, name: 'Alice', age: 25, score: 80, favoriteSubject: "math",},
  { id: 2, name: 'Bob', age: 30, score: 85, favoriteSubject: "history" },
  { id: 3, name: 'Charlie', age: 35, score: 34, favoriteSubject: "art" },
  { id: 4, name: 'David', age: 40, score: 95, favoriteSubject: "math" },
  { id: 5, name: 'Eve', age: 28, score: 88, favoriteSubject: "math" }
];
```

### projects-v1/app_js/sample_1/app.js

```js
console.log(students);

const numberOfStudents = students.length;
console.log("Number of students:", numberOfStudents);

const totalScore = students.reduce((total, student) => {
  total += student.score;
  return total;
}, 0)
console.log("Total score:", totalScore);

const averageScore = totalScore / numberOfStudents;
console.log("Average score:", averageScore);

// return Object with favorite subject as key and number of students as value
const favoriteSubjectCount = students.reduce( (obj, student) => {
  const favouriteSub = student.favoriteSubject;
  if(obj[favouriteSub]){
    obj[favouriteSub] += 1;
  } else {
    obj[favouriteSub] = 1;
  }
  return obj;
}, {});

console.log("Favorite subject count:", favoriteSubjectCount);

```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/c70d22f9-5cca-47b9-a652-885bb46c69d0" />

</details>


<details>
  <summary>JS Math Object </summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
//Math Object
console.log("Math.round(4.56789):", Math.round(4.56789)); // 5
console.log("Math.ceil(4.333):", Math.ceil(4.333)); // 5
console.log("Math.floor(4.666):", Math.floor(4.666)); // 4
console.log("Math.sqrt(25):", Math.sqrt(25)); // 5
console.log("Math.pow(2, 3):", Math.pow(2, 3)); // 8
console.log("Math.abs(-10):", Math.abs(-10)); // 10
console.log("Math.PI:", Math.PI); // 3.141592653589793
console.log("Math.min(3, 1, 4, 2):", Math.min(3, 1, 4, 2)); // 1
console.log("Math.max(3, 1, 4, 2):", Math.max(3, 1, 4, 2)); // 4
console.log("Math.random():", Math.random()); // Random number between 0 and 1

console.log("Numbers btw 1 and 10", Math.floor(Math.random() * 10) + 1); // Random number between 1 and 10

```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/cfcad96b-e416-4095-880b-8d928259c641" />

</details>

<details>
  <summary>JS Date Object </summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const months = ['January','February','March','April','May','June','July','August','September','October','November','December'];
const days = ['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'];

const now = new Date();
const nowFormatted = new Date().toLocaleString();
const nowFormatted2 = new Date().toISOString();
const nowFormatted3 = new Date('2025-08-20T14:30:00Z');
const nowFormatted4 = new Date('11/20/2025 14:30:00');
const nowDate = now.getDate();
const nowYear = now.getFullYear();
const nowMonth = now.getMonth();
const nowDay = now.getDay();
const nowHours = now.getHours();
const nowMinutes = now.getMinutes();
const nowSeconds = now.getSeconds();

console.log('now:', now);
console.log('nowFormatted:', nowFormatted);
console.log('nowFormatted2:', nowFormatted2);
console.log('nowFormatted3:', nowFormatted3);
console.log('nowFormatted4:', nowFormatted4);
console.log('nowDate:', nowDate);
console.log('nowYear:', nowYear);
console.log('nowMonth:', nowMonth);
console.log('nowDay:', nowDay);
console.log('nowHours:', nowHours);
console.log('nowMinutes:', nowMinutes);
console.log('nowSeconds:', nowSeconds);

const month = months[nowMonth];
const day = days[nowDay];
const date = nowDate;
const year = nowYear;

console.log(`Today is ${day}, ${month} ${date}, ${year}`);
console.log(`Current Time: ${nowHours}:${nowMinutes < 10 ? '0' + nowMinutes : nowMinutes}:${nowSeconds < 10 ? '0' + nowSeconds : nowSeconds}`);

```

<img width="1554" height="1042" alt="image" src="https://github.com/user-attachments/assets/1efd1b89-d41c-4fe5-b5ec-7de2f49b1599" />

</details>

<details>
  <summary>JS DOM: getElementByID </summary>

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
    <h1 id="title">Hello</h1>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>

```

### projects-v1/app_js/sample_1/app.js

```js
const h1 = document.getElementById('title');
h1.style.color = 'red';

const btn = document.getElementById('btn');
btn.style.backgroundColor = 'black';
btn.style.color = 'white';
btn.style.padding = '10px 20px';
btn.style.border = 'none';
btn.style.borderRadius = '5px';
btn.style.cursor = 'pointer';

btn.addEventListener('click', () => {
    alert('Button Clicked!');
});

```

<img width="1557" height="1020" alt="image" src="https://github.com/user-attachments/assets/0ffba66f-61b7-4bf1-9c38-4a6635bdcf37" />

</details>


<details>
  <summary>JS DOM: getElementsByTagName </summary>

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
    <h1 id="title">Hello</h1>
    <h2>List of students</h2>
    <ul>
        <li>Student 1</li>
        <li>Student 2</li>
        <li>Student 3</li>
        <li>Student 4</li>
        <li>Student 5</li>
    </ul>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const h1 = document.getElementById('title');
h1.style.color = 'red';

const headings = document.getElementsByTagName('h2');
console.log(headings);
console.log(headings.length);
headings[0].style.color = 'blue';

const items = document.getElementsByTagName('li');
console.log(items);

const listedItems = Array.from(items);
const listedItems2 = [...items];
console.log(listedItems);
console.log(listedItems2);

listedItems[1].style.fontWeight = 'bold';
listedItems.forEach((item) => {
    item.style.color = 'green';
    item.style.fontSize = '20px';
});

```

<img width="2067" height="1352" alt="image" src="https://github.com/user-attachments/assets/af0f6ad4-12ac-4238-9000-34abe38b6bbc" />

</details>

<details>
  <summary>JS DOM: getElementsByClassName </summary>

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
    <h1 id="title">Hello</h1>
    <h2>List of students</h2>
    <ul>
        <li class="special">Student 1</li>
        <li>Student 2</li>
        <li class="special">Student 3</li>
        <li>Student 4</li>
        <li class="special">Student 5</li>
    </ul>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const h1 = document.getElementById("title");
h1.style.color = "red";

const headings = document.getElementsByTagName("h2");
console.log(headings);
console.log(headings.length);
headings[0].style.color = "blue";

const items = document.getElementsByClassName("special");
console.log(items);

items[2].style.fontWeight = "bold";
Array.from(items).forEach((item) => {
  item.style.color = "red";
  item.style.fontSize = "20px";
});
```

<img width="2067" height="1352" alt="image" src="https://github.com/user-attachments/assets/76ad9abd-4bee-49a5-91e2-8c65ba37e78a" />

</details>

<details>
  <summary>JS DOM: QuerySelector and QuerySelectorAll </summary>

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
    <h1 id="title">Hello</h1>
    <h2>List of students</h2>
    <ul id="result">
        <li class="special">Student 1</li>
        <li>Student 2</li>
        <li class="special">Student 3</li>
        <li>Student 4</li>
        <li class="special last">Student 5</li>
    </ul>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const h1 = document.getElementById("title");
h1.style.color = "red";

const headings = document.getElementsByTagName("h2");
console.log(headings);
console.log(headings.length);
headings[0].style.color = "blue";

const result = document.querySelector("#result");
result.style.backgroundColor = "black";
result.style.color = "white";

const students = document.querySelectorAll(".special");
console.log(students);
students.forEach((student) => {
  student.style.color = "pink";
});

const lastStudent = document.querySelector(".last");
console.log(lastStudent);
lastStudent.style.fontSize = "30px";

const lastStudent2 = document.querySelector("li:last-child");
console.log(lastStudent2);
lastStudent2.innerHTML += " - color is pink.";
```

<img width="2067" height="1352" alt="image" src="https://github.com/user-attachments/assets/335ed919-14a5-4d38-9ca1-c614807a9f4a" />

</details>

<details>
  <summary>JS DOM: Children - firstChild, firstElementChild, lastChild, lastElementChild </summary>

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
    <h1 id="title">Javascript Basics</h1>
    <h2>List of students</h2>
    <ul id="result">
        <li>Student 1</li>
        <li>Student 2</li>
        <li>Student 3</li>
        <li>Student 4</li>
        <li>Student 5</li>
    </ul>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const h1 = document.getElementById("title");
h1.style.color = "red";

const headings = document.getElementsByTagName("h2");
console.log(headings);
console.log(headings.length);
headings[0].style.color = "blue";

const result = document.querySelector("#result");
console.log(result);
result.style.backgroundColor = "wheat";

const children = result.children;
console.log(children);

const firstElementChild = result.firstElementChild;
console.log(firstElementChild);
firstElementChild.style.color = "green";
firstElementChild.style.fontWeight = "bold";

const firstChild = result.firstChild;
console.log(firstChild);

const lastElementChild = result.lastElementChild;
console.log(lastElementChild);
lastElementChild.style.color = "blue";
lastElementChild.style.fontWeight = "bold";

const lastChild = result.lastChild;
console.log(lastChild);

```

<img width="2067" height="1352" alt="image" src="https://github.com/user-attachments/assets/64bb71bc-584c-415c-bcf5-ad2141cf9063" />

</details>

<details>
  <summary>JS DOM: parentElement </summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const heading = document.querySelector("h2");
console.log(heading);
console.log(heading.parentElement);
console.log(heading.parentElement.parentElement);
console.log(heading.parentElement.parentElement.parentElement);
console.log(heading.parentElement.parentElement.parentElement.parentElement);

const parentOfH2 = heading.parentElement;
console.log(parentOfH2);
parentOfH2.style.color = "red";
```

<img width="2067" height="1352" alt="image" src="https://github.com/user-attachments/assets/2ab35d54-982c-4efa-a858-86f260d2278f" />

</details>

<details>
  <summary>JS DOM: Sibling - nextSibling, nextElementSibling, previousSibling, previousElementSibling </summary>

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
    <ul id="result">
        <li class="first">first</li>
        <li>list item 2</li>
        <li>list item 3</li>
        <li id="last">last</li>
    </ul>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const first = document.querySelector(".first");
console.log(first);

const last = document.querySelector("#last");
console.log(last);

const second = first.nextElementSibling;
console.log(second);

const second2 = first.nextSibling.nextSibling;
console.log(second2);

second.style.color = "red";
second.style.fontSize = "1.5rem";

const third = last.previousElementSibling;
console.log(third);
third.style.color = "blue";
third.style.fontSize = "1.5rem";
```

<img width="2067" height="1352" alt="image" src="https://github.com/user-attachments/assets/5bd4ede8-8bcd-4c24-8ece-f4e183e3e1ca" />

</details>

<details>
  <summary>JS DOM: nodeValue, childNodes, textContent </summary>

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
    <h1 id="special">This is a special content</h1>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const item = document.getElementById("special");

const value = item.nodeValue;
console.log(value);

const childNode = item.childNodes[0];
console.log(childNode);

const childNode2 = item.firstChild;
console.log(childNode2);

const childValue = childNode.nodeValue;
console.log(childValue);

const itemValue = item.textContent;
console.log(itemValue);

```

<img width="1982" height="1339" alt="image" src="https://github.com/user-attachments/assets/70682f6b-0ffb-409e-abf6-de3193ddf6a6" />

</details>

<details>
  <summary>JS DOM: getAttribute() and setAttribute() </summary>

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
    <ul>
        <li class="first mylist" id="special">I have class of first</li>
        <li class="mylist" id="linklist">
            <a href="first.html" id="link">random link</a>
        </li>
        <li class="mylist">I have no attributes</li>
    </ul>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const first = document.querySelector(".first");
console.log(first);

const classValue = first.getAttribute("class");
console.log(classValue);

const idValue = first.getAttribute("id");
console.log(idValue);

const link = document.getElementById("link");
const showLink = link.getAttribute("href");
console.log(showLink);

const linkList = document.getElementById("linklist");
console.log(linkList);

const last = linkList.nextElementSibling;
console.log(last);
last.setAttribute("class", "first");
last.textContent = "I also have a class of first";

const links = document.querySelectorAll(".first");
console.log(links);
```

<img width="1982" height="1339" alt="image" src="https://github.com/user-attachments/assets/ce924252-b261-45fd-823e-4d38bd79334f" />

</details>

<details>
  <summary>JS DOM: ClassList and ClassName </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .colors {
            color: white;
            background-color: red;
        }

        .colors2 {
            color: white;
            background-color: black;
        }

        .text {
            font-size: 30px;
            font-weight: bold;
            letter-spacing: 1rem;
        }
    </style>
</head>

<body>
    <h1 id="first" class="colors">I'm First Element</h1>
    <h1 id="second">I'm Second Element</h1>
    <h1 id="third">I'm Third Element</h1>
    <h1 id="forth">I'm Fourth Element</h1>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const first = document.getElementById('first');
const second = document.getElementById('second');
const third = document.getElementById('third');
const forth = document.getElementById('forth');

const classValue = first.className;
console.log('Class value of first element:', classValue);

second.className = 'colors2';
const classValue2 = second.className;
console.log('Class value of second element:', classValue2);

third.classList.add('colors');
third.classList.add('text')
const classValue3 = third.className;
console.log('Class value of third element:', classValue3);

forth.classList.add('colors2', 'text');
const classValue4 = forth.className;
console.log('Class value of forth element:', classValue4);
forth.classList.remove('colors2');
const classValue5 = forth.className;
console.log('Class value of forth element after removing colors2 class:', classValue5);

const hasTextClass = third.classList.contains('text');
console.log('Does third element have "text" class?', hasTextClass);
```

<img width="1488" height="1020" alt="image" src="https://github.com/user-attachments/assets/a25006dd-2305-4916-a253-3421f37909d7" />

</details>

<details>
  <summary>JS DOM: createElement, createTextNode, appendChild </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .red {
            color: white;
            background-color: red;
        }

        .blue {
            color: white;
            background-color: blue;
        }
    </style>
</head>

<body>
    <div id="result">
        <h1 class="red">I'm the child of result</h1>
    </div>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const result = document.querySelector("#result");

// create empty h2 element
const h2 = document.createElement("h2");

// append text to h2
// h2.innerText = "I'm the new created element";
const h2textNode = document.createTextNode("I'm the new created Text element");
h2.appendChild(h2textNode);

// manipulate classList and style for h2
h2.classList.add("red");
h2.classList.toggle("blue");
console.log(h2.classList);
console.log(h2.className);
h2.style.fontSize = "40px";
h2.style.backgroundColor = "green";
h2.style.color = "white";
h2.style.padding = "10px";
h2.style.textAlign = "center";

// append h2 to result
result.appendChild(h2);

// create empty div and p element
const div = document.createElement("div");
const p = document.createElement("p");

// create Text Node
const textNode = document.createTextNode("I'm the second created element");

// append textNode to p
p.appendChild(textNode);

// manipulate classList for p
p.classList.add("blue");
p.style.fontSize = "40px";
p.style.color = "white";
p.style.padding = "10px";
p.style.textAlign = "center";

// append p to div
div.appendChild(p);

// append div to result
result.appendChild(div);

console.log(result.children);
console.log(Array.from(result.children)[0]);
console.log(Array.from(result.children)[1]);
console.log(Array.from(result.children)[2]);

// for (node of result.children) {
//   console.log(node);
// }

```

<img width="1318" height="965" alt="image" src="https://github.com/user-attachments/assets/2804cbbb-3822-4117-88f7-07d07147c9f0" />

</details>

<details>
  <summary>JS DOM: insertBefore and replaceChild </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .red {
            color: white;
            background-color: red;
        }

        .blue {
            color: white;
            background-color: blue;
        }

        .black {
            color: white;
            background-color: black;
        }
    </style>
</head>

<body>
    <div id="result">
        <h1 class="red">I'm the child of result</h1>
    </div>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const result = document.querySelector("#result");

// create empty div and p element
const div = document.createElement("div");
const p = document.createElement("p");

// create Text Node
const textNode = document.createTextNode("I'm the created Text element");

// append textNode to p
p.appendChild(textNode);

// manipulate classList for p
p.classList.add("blue");
p.style.fontSize = "40px";
p.style.color = "white";
p.style.padding = "10px";
p.style.textAlign = "center";

// append p to div
div.appendChild(p);

// append div to result
document.body.insertBefore(div, result);

const siblingBeforeResult = result.previousElementSibling;
console.log(siblingBeforeResult);
console.log(Array.from(siblingBeforeResult.children));

const h6 = document.createElement("h6");
const h6Text = document.createTextNode("I'm a H6 replacment Text");
h6.appendChild(h6Text);
h6.classList.add("black");
h6.style.padding = "10px";
h6.style.textAlign = "center";
document.body.replaceChild(h6, result);

```

<img width="1318" height="965" alt="image" src="https://github.com/user-attachments/assets/9d8509a7-8935-47e4-949b-6786206d3706" />

</details>

<details>
  <summary>JS DOM: Prepend and InnerText </summary>

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
    <h2>first heading</h2>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// create empty heading element
const h1 = document.createElement("h1");

// prepend with InnerText
h1.innerText = "I'm the created Text element";
document.body.prepend(h1);
console.log(document.body.children);

```

<img width="1318" height="965" alt="image" src="https://github.com/user-attachments/assets/5b5bf161-a6cd-4c04-8147-cc476d39eb97" />

</details>

<details>
  <summary>JS DOM: Remove and Remove Child </summary>

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
    <h1 id="header">hello world</h1>
    <div id="result">
        <h1>second heading</h1>
    </div>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
// create empty heading element
const h1 = document.createElement("h1");

// prepend with InnerText
h1.innerText = "I'm the created Text element";
document.body.prepend(h1);
console.log(document.body.children);

// remove
const header = document.querySelector("#header");
header.remove();

// removeChild
const result = document.querySelector("#result");
const heading = result.querySelector("h1");
result.removeChild(heading);
console.log(result.children);

```

<img width="1314" height="930" alt="image" src="https://github.com/user-attachments/assets/b1817b38-1408-443b-9081-98464933a921" />

</details>

<details>
  <summary>JS DOM: InnerHTML and TextContent </summary>

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
    <h1 id="header">hello world</h1>
    <ul id="first">
        <li class="item">list item</li>
        <li>list item</li>
    </ul>
    <div id="second">
        i have some text content
    </div>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const list = document.getElementById('first');
const items = list.querySelector('.item');
const div = document.getElementById('second');
const btn = document.querySelector('.btn');

console.log(div.textContent);
console.log(list.innerHTML);

const ul = document.createElement('ul');
ul.innerHTML = `
    <li>New Item 1</li>
    <li>New Item 2</li>
    <li>New Item 3</li>
`;

document.body.insertBefore(ul, btn);

```

<img width="1506" height="1025" alt="image" src="https://github.com/user-attachments/assets/2a2bbdf1-135d-4b95-95a7-3d0f831a6c7b" />

</details>

<details>
  <summary>JS Events: Click Events</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .red {
            background-color: red;
            color: white;
            text-transform: uppercase;
            font-size: 2rem;
        }

        .blue {
            background-color: blue;
            color: white;
            text-transform: capitalize;
            font-size: 10px;
        }
    </style>
</head>

<body>
    <h1 id="header">hello world</h1>
    <p>I can trigger an event!</p>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector('.btn');
const header = document.querySelector('#header');
const p = document.querySelector('p');

btn.addEventListener('click', function() {
    console.log('Button was clicked!');
    header.className === '' ? header.classList.add('red') : header.classList.remove('red');
    console.log(`Header.className: ${header.className}`);
});

function changeParagraphColors() {
    let hasClass = p.classList.contains('blue');
    hasClass ? p.classList.remove('blue') : p.classList.add('blue');
    console.log(`p.className: ${p.className}`);
}
btn.addEventListener('click', changeParagraphColors);

```

<img width="1506" height="1025" alt="image" src="https://github.com/user-attachments/assets/b3e75314-ec47-422a-a5f8-b9b4fb8fa360" />

</details>

<details>
  <summary>JS Events: Mouse Events </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .red {
            background-color: red;
            color: white;
            text-transform: uppercase;
            font-size: 2rem;
        }

        .blue {
            background-color: blue;
            color: white;
            text-transform: capitalize;
            font-size: 10px;
        }
    </style>
</head>

<body>
    <h1 id="header">hello world</h1>
    <p>I can trigger an event!</p>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector('.btn');
const header = document.querySelector('#header');
const p = document.querySelector('p');

function clickEvent() {
   console.log('Button was clicked!');
}

function mouseDownEvent() {
    console.log('Mouse is Down');
}

function mouseUpEvent() {
    console.log('Mouse is Up');
}

btn.addEventListener('click', clickEvent);
btn.addEventListener('mousedown', mouseDownEvent);
btn.addEventListener('mouseup', mouseUpEvent);

header.addEventListener('mouseenter', function() {
    console.log('Mouse entered the header');
    header.classList.add('red');
});

header.addEventListener('mouseleave', function() {
    console.log('Mouse left the header');
    header.classList.remove('red');
});

```

<img width="1506" height="1025" alt="image" src="https://github.com/user-attachments/assets/a805f0e8-a50a-4cc2-9ebb-86e902946594" />

</details>

<details>
  <summary>JS Events: Key Events </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .red {
            background-color: red;
            color: white;
            text-transform: uppercase;
            font-size: 2rem;
        }

        .blue {
            background-color: blue;
            color: white;
            text-transform: capitalize;
            font-size: 10px;
        }
    </style>
</head>

<body>
    <input type="text" id="name">
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js

const btn = document.querySelector('.btn');
const nameInput = document.querySelector('#name');

nameInput.addEventListener('keypress', function(e) {
    console.log(`You pressed a key: "${e.key}"`);
});

nameInput.addEventListener('keydown', function(e) {
    console.log(`Key down: "${e.key}"`);
});

nameInput.addEventListener('keyup', function(e) {
    console.log(`Key up: "${e.key}"`);
});

```

<img width="1506" height="1025" alt="image" src="https://github.com/user-attachments/assets/ca709b20-4157-4a1c-a944-6a6281b20c18" />

</details>

<details>
  <summary>JS Events: The Event Object and e.preventDefault() </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        a {
            display: inline-block;
            margin-top: 80vh;
        }
    </style>
</head>

<body>
    <button class="btn" id="btn">Click Me</button>
    <h1>some <span>spanned heading</span></h1>
    <a href="#" id="link">random link</a>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const heading = document.querySelector("h1");
const btn = document.querySelector(".btn");
const link = document.getElementById("link");

heading.addEventListener("click", function (e) {
  console.log(e.currentTarget);
  console.log(e.target);
  console.log(e.type);
  console.log(e);
});

link.addEventListener("click", function (e) {
  e.preventDefault();
  console.log("link clicked, prevented default behavior");
});

```

<img width="2052" height="1447" alt="image" src="https://github.com/user-attachments/assets/5eccaa42-3c25-4130-bf62-1375d3c426d7" />

</details>

<details>
  <summary>JS Events: Event Propagation, Bubbling and Capturing </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>

<body>
    <div class="container">
        <ul class="list-items">
            <li class="item"><a href="#" class="link">link</a></li>
            <li class="item"><a href="#" class="link">link</a></li>
            <li class="item"><a href="#" class="link">link</a></li>
        </ul>
    </div>
    <button class="btn" id="btn">Click Me</button>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const link = document.getElementById("link");
const container = document.querySelector(".container");
const list = document.querySelector(".list-items");

function preventPropagation(e) {
  console.log("Link clicked, propagation stopped.");
  e.stopPropagation();
}

function showBubbling(e) {
  console.log("#######################################");
  console.log("Current Target:", e.currentTarget);
  console.log("Target:", e.target);
}

// Event Bubbling
list.addEventListener("click", showBubbling);
container.addEventListener("click", showBubbling);
document.addEventListener("click", showBubbling);
window.addEventListener("click", showBubbling);

// Event Propagation Prevention
// list.addEventListener("click", preventPropagation);
// container.addEventListener("click", showBubbling);
// document.addEventListener("click", showBubbling);
// window.addEventListener("click", showBubbling);

// Event Capturing
// list.addEventListener("click", showBubbling, { capture: true });
// container.addEventListener("click", showBubbling, { capture: true });
// document.addEventListener("click", showBubbling, { capture: true });
// window.addEventListener("click", showBubbling, { capture: true });

btn.addEventListener("click", function () {
  const element = document.createElement("h1");
  element.classList.add("heading");
  element.textContent = "New Heading Added inside container!";
  container.appendChild(element);
});

container.addEventListener("click", function (e) {
  if (e.target.classList.contains("heading")) {
    console.log("#######################################");
    console.log("Hello there from heading!");
  }
});

```

<img width="2138" height="1386" alt="image" src="https://github.com/user-attachments/assets/08af2f31-ed28-45ee-b627-288f633e1786" />

</details>

<details>
  <summary>JS Forms: Basics </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="password" id="password" placeholder="Enter Password" /><br /><br />
        <input type="submit" value="Submit" class="btn" />
    </form>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const form = document.querySelector("form");
const name = document.querySelector("#name");
const password = document.querySelector("#password");

// console.log(btn, form, name, password);
form.addEventListener("submit", function (e) {
  e.preventDefault();
  console.log("Form submitted!");
  console.log(e.target)
  console.log(e.target.name)
  console.log("Name:", e.target.name.value);
  console.log("Password:", e.target.password.value);
  console.log("Name:", name.value);
  console.log("Password:", password.value);
});

```

<img width="1564" height="1031" alt="image" src="https://github.com/user-attachments/assets/968b3cb4-2d63-49b6-888e-8435c94dd0cd" />

</details>

<details>
  <summary>JS Forms: Local Storage/ Session Storage API </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="password" id="password" placeholder="Enter Password" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <input type="button" value="Retrieve Data" class="btn" id="retrieve-btn" />
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const retrieveBtn = document.querySelector("#retrieve-btn");
const form = document.querySelector("form");
const name = document.querySelector("#name");
const password = document.querySelector("#password");

// Web Storage API - Local Storage, Session Storage

// Set Item
// localStorage.setItem("name", "John Doe");
// sessionStorage.setItem("name", "John Doe Session");

// Get Item
// const nameFromLocalStorage = localStorage.getItem("name");
// const nameFromSessionStorage = sessionStorage.getItem("name");
// console.log(nameFromLocalStorage);
// console.log(nameFromSessionStorage);

// Remove Item
// localStorage.removeItem("name");
// sessionStorage.removeItem("name");

// Clear Storage
// localStorage.clear();
// sessionStorage.clear();

form.addEventListener("submit", function (e) {
  e.preventDefault();
  // Save data to Local Storage
  localStorage.setItem("name", name.value);
  localStorage.setItem("password", password.value);

  // Save data to Session Storage
  // sessionStorage.setItem("name", name.value);
  // sessionStorage.setItem("password", password.value);

  alert("Data saved!");
});

retrieveBtn.addEventListener("click", function () {
  // Retrieve data from Local Storage
  const storedName = localStorage.getItem("name");
  const storedPassword = localStorage.getItem("password");

  // Retrieve data from Session Storage
  // const storedName = sessionStorage.getItem("name");
  // const storedPassword = sessionStorage.getItem("password");

  alert(`Name: ${storedName}\nPassword: ${storedPassword}`);
});

```

<img width="1564" height="1031" alt="image" src="https://github.com/user-attachments/assets/095175ff-b26a-473e-9d4e-b2f95c50dcbb" />

</details>

<details>
  <summary>JS Forms: Local Storage API with JSON.stringify() and JSON.parse() </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="fruit" placeholder="Enter Fruit Name" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <input type="button" value="Retrieve Friend Data" class="btn" id="retrieve-friend-btn" /> <br /><br />
    <input type="button" value="Retrieve Fruit Data" class="btn" id="retrieve-fruit-btn" /><br /><br />
    <input type="button" value="Clear Local Storage" class="btn" id="clear-storage-btn" /><br /><br />
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const retrieveFriendsBtn = document.querySelector("#retrieve-friend-btn");
const retrieveFruitBtn = document.querySelector("#retrieve-fruit-btn");
const clearStorageBtn = document.querySelector("#clear-storage-btn");
const form = document.querySelector("form");
const fruit = document.querySelector("#fruit");

// Web Storage API - Local Storage, Session Storage

// Set Item
// localStorage.setItem("name", "John Doe");

// Get Item
// const nameFromLocalStorage = localStorage.getItem("name");
// console.log(nameFromLocalStorage);

// Remove Item
// localStorage.removeItem("name");

// Clear Storage
// localStorage.clear();

//. JSON.stringy() and JSON.parse()

const friends = ["Mike", "Jessie", "John"];

// Set Array in Local Storage with JSON.stringify()
localStorage.setItem("friends", JSON.stringify(friends));

// Get Array from Local Storage with JSON.parse()
const friendsFromLocalStorage = JSON.parse(localStorage.getItem("friends"));

retrieveFriendsBtn.addEventListener("click", function() {
    alert(friendsFromLocalStorage);
});


let fruits;

if (localStorage.getItem("fruits")) {
    fruits = JSON.parse(localStorage.getItem("fruits"));
} else {
    fruits = [];
}

// Retrieve Fruit Data
retrieveFruitBtn.addEventListener("click", function() {
    alert(fruits);
});

// Add Fruit Data
form.addEventListener("submit", function(e) {
    e.preventDefault();
    const fruitValue = fruit.value.trim();
    if (fruitValue !== "") {
        fruits.push(fruitValue);
        localStorage.setItem("fruits", JSON.stringify(fruits));
        fruit.value = "";
        alert("Fruit added!");
    } else {
        alert("Please enter a fruit name.");
    }
});

// Clear Local Storage
clearStorageBtn.addEventListener("click", function() {
    localStorage.clear();
    alert("Local storage cleared!");
});

```

<img width="1564" height="1031" alt="image" src="https://github.com/user-attachments/assets/cbdaa836-7db9-4df8-b19d-8035f7a54e40" />

</details>

<details>
  <summary>JS setTimeout </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const form = document.querySelector("form");
const nameInput = document.querySelector("#name");

function sayHello() {
    console.log(`Hello ${nameInput.value || "Jasmine!"}`);
}

function showScore(name, score) {
    console.log(`${name}, your score is ${score}%.`);
}

form.addEventListener("submit", function (e) {
    e.preventDefault();
    const firstID = setTimeout(sayHello, 1000);
    const secondID = setTimeout(function () {
        console.log("Would you like to know your score?");
    }, 3000);
    const thirdID = setTimeout(showScore, 5000, nameInput.value || "Jasmine", 95);

    // To cancel the timeouts, uncomment the lines below
    // clearTimeout(firstID);
    // clearTimeout(secondID);
    // clearTimeout(thirdID);
});

```

<img width="1564" height="1031" alt="image" src="https://github.com/user-attachments/assets/99a0e041-3040-40cf-97ac-a1d7e1d90355" />

</details>

<details>
  <summary>JS setInterval </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <input type="button" value="Stop Interval" class="btn" id="stop-btn" /><br /><br />
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const stopBtn = document.querySelector("#stop-btn");
const form = document.querySelector("form");
const nameInput = document.querySelector("#name");

function sayHello() {
  console.log(`Hello ${nameInput.value || "Jasmine!"}`);
}

let firstID;

form.addEventListener("submit", function (e) {
  e.preventDefault();
  firstID = setInterval(sayHello, 2000);
});

stopBtn.addEventListener("click", function () {
  // To cancel the interval
  clearInterval(firstID);
});

function showScore(name, score) {
  console.log(`${name} scored ${score}.`);
}
setInterval(showScore, 4000, "Jasmine", 95);

```

<img width="1328" height="941" alt="image" src="https://github.com/user-attachments/assets/2c805087-e9cd-45ea-9c2a-8372f04a5f45" />

</details>

<details>
  <summary>JS Events: DOMContentLoaded </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const stopBtn = document.querySelector("#stop-btn");
const form = document.querySelector("form");
const nameInput = document.querySelector("#name");

// DOMContentLoaded is fired when the initial HTML document has been completely loaded and parsed
// without waiting for stylesheets, images, and subframes to finish loading.
window.addEventListener("DOMContentLoaded", () => {
  console.log("DOM fully loaded and parsed.....");
});

```

<img width="1328" height="941" alt="image" src="https://github.com/user-attachments/assets/920cea2d-db64-459e-a525-81ddad424698" />

</details>

<details>
  <summary>JS Events: Load </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const stopBtn = document.querySelector("#stop-btn");
const form = document.querySelector("form");
const nameInput = document.querySelector("#name");

// Load event is fired when the whole HTML is loaded and parsed, including all deferred stylesheets and Images.
window.addEventListener("load", () => {
  console.log("Page fully loaded and parsed.....");
});

```

<img width="1328" height="941" alt="image" src="https://github.com/user-attachments/assets/b6e82a23-f5d1-442d-9cf6-38deabb49609" />

</details>

<details>
  <summary>JS Events: Scroll </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input {
            font-size: 1.2rem;
            padding: 10px;
            width: 250px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }

        .footer {
            margin-top: 100vh;
            text-align: center;
        }
    </style>
</head>

<body>
    <form action="" id="form">
        <input type="text" id="name" placeholder="Enter Name" /><br /><br />
        <input type="submit" value="Submit" class="btn" /><br /><br />
    </form>
    <p class="footer">This is the Footer</p>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const stopBtn = document.querySelector("#stop-btn");
const form = document.querySelector("form");
const nameInput = document.querySelector("#name");

// Scroll Event
window.addEventListener("scroll", () => {
  console.log("Scrolling...");
  console.log(`Scroll Y: ${window.scrollY} px`);
  console.log(`Scroll X: ${window.scrollX} px`);
});
```

<img width="1200" height="909" alt="image" src="https://github.com/user-attachments/assets/9c12f894-11d0-487f-95e6-b588c094e1a9" />

</details>


<details>
  <summary>JS Window Height, WIdth and getBoundingClientRect()</summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .box {
            width: 200px;
            height: 200px;
            background-color: gray;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <div class="box"></div><br /><br />
    <input type="button" value="Get Dimensions" class="btn" /><br /><br />
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const box = document.querySelector(".box");

console.log("height: ", window.innerHeight);
console.log("width: ", window.innerWidth);

btn.addEventListener("click", () => {
  const values = box.getBoundingClientRect();
  console.log(values);
});

```

<img width="1338" height="909" alt="image" src="https://github.com/user-attachments/assets/bdf9ce3b-9912-4e41-9fe7-a42c71167e3c" />

</details>

<details>
  <summary>JS Events: Resize </summary>

### projects-v1/app_js/sample_1/index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Basics</title>
    <style>
        .btn {
            background-color: #f15025;
            color: white;
            font-size: 1.2rem;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .box {
            width: 200px;
            height: 200px;
            background-color: gray;
            border-radius: 5px;
        }
    </style>
</head>

<body>
    <div class="box"></div><br /><br />
    <input type="button" value="Get Dimensions" class="btn" /><br /><br />
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js
const btn = document.querySelector(".btn");
const box = document.querySelector(".box");

console.log("First height: ", window.innerHeight);
console.log("First width: ", window.innerWidth);

window.addEventListener("resize", () => {
  console.log("height: ", window.innerHeight);
  console.log("width: ", window.innerWidth);
});

```

<img width="1338" height="910" alt="image" src="https://github.com/user-attachments/assets/9b44bb8d-c590-4551-b281-94a49afcf3fb" />

</details>





























<details>
  <summary>JS  </summary>

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
    <script src="./data.js"></script>
    <script src="./app.js"></script>
</body>

</html>
```

### projects-v1/app_js/sample_1/app.js

```js

```

</details>













