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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/77d52950-2c5f-48f7-96dc-79099bb3bc39" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/7b718970-680e-40c4-be22-e16ad43ac08b" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/cde1ca7f-1466-48ad-afd8-d5014126facf" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/4666d40c-b86a-4445-80c2-5a464a8e18d4" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/58c8aefb-60a8-45ee-a6e4-039f38c2b4e8" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/f437a1ce-a1b4-410b-a33a-64dfd9ea16e3" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/4f8be781-07c3-4f23-8e1d-2ab7556acc74" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/fa84e2f3-cfe1-4210-b902-e1185a24ba4b" />
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

<img width="1297" height="1010" alt="image" src="https://github.com/user-attachments/assets/8b589424-89f6-463d-9bb8-95be65a110c9" />
<img width="1431" height="1063" alt="image" src="https://github.com/user-attachments/assets/3829796f-9989-474b-b163-240dfbeff5ce" />

</details>
















<details>
  <summary>JS</summary>

### projects-v1/app_js/sample_1/index.html

```html

```

### projects-v1/app_js/sample_1/app.js

```js

```

</details>
















