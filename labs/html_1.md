### [1 - HTML & CSS Fundamentals - Coding Addict](https://www.codingaddict.io/l/products)

<details>
  <summary>Install React</summary>

### Confirm Node Version

```
$ node --version
v22.14.0
```

### Install and run React App with create-react-app

```
npx create-react-app my-app
cd my-app
npm start
```

### Install and run React App with vite

```
npm create vite@latest my-app -- --template react
cd my-app
npm install
npm run dev
```

![image](https://github.com/user-attachments/assets/2b2eabdb-b716-42e0-806f-a83e5a731991)

</details>

<details>
  <summary>Index.js default setup</summary>

### Index.js default setup

```js
import React from "react";
import ReactDOM from "react-dom/client";

function Greeting() {
  return <h1>My First Component</h1>;
}

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<Greeting />);
```

![image](https://github.com/user-attachments/assets/0de638b7-2b78-4636-accf-12718a7847d3)

</details>
