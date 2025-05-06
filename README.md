# REACT-LABS-IFEANYI
by Ifeanyi Omeata

<details>
  <summary>Install React</summary>

  ### Confirm Node Version
  
  ```
  $ node --version
  v22.14.0
  ```

  ### Install React App

  ```
  npx create-react-app my-app
  npx create-react-app my-app@latest
  ```

  ### Start React App

  ```
  cd my-app
  npm start
  ```

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

<details>
  <summary>Using React.createElement()</summary>

  ### Using React.createElement()

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  function Greeting() {
    return (
      <div>
        <h1>My First Component</h1>
        <Greeting2 />
      </div>
    );
  }
  
  const Greeting2 = () => {
    return React.createElement(
      "div",
      {},
      React.createElement("h1", {}, "My Second Component")
    );
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<Greeting />);
  ```

  ![image](https://github.com/user-attachments/assets/13dc2db3-257b-4f9b-a23b-1343a91b604a)


</details>

<details>
  <summary>Nested Components with React Fragments</summary>

  ### Nested Components with React Fragments

  ```js
import React from "react";
import ReactDOM from "react-dom/client";

// Nested Components with React Fragments
function Greeting() {
  return (
    <React.Fragment>
      <h2>Message Board</h2>
      <hr />
      <div>
        <h3>Person: {<Person />}</h3>
        <h3>Message: {<Message />}</h3>
      </div>
    </React.Fragment>
  );
}

const Person = () => {
  return <span>John Doe</span>;
};
const Message = () => {
  return <span>This is a message.</span>;
};

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<Greeting />);
  ```

![image](https://github.com/user-attachments/assets/d4c5ec68-4bf3-4490-9c15-094b0c94c6f7)

</details>

<details>
  <summary>Project - Booklist</summary>

  ### 1-Create Structure

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  function BookList() {
    return (
      <React.Fragment>
        <section>
          <Book />
        </section>
      </React.Fragment>
    );
  }
  
  const Book = () => {
    return (
      <article>
        <Image />
        <Title />
        <Author />
      </article>
    );
  };
  
  const Image = () => <h2>Image Placeholder</h2>;
  const Title = () => <h2>Book Title</h2>;
  const Author = () => {
    return <h3>Author</h3>;
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/ad46c540-c7f4-4378-b7f7-28f7515537d2)

  ### 2-Add Image, Title and Author from Amazon

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  function BookList() {
    return (
      <React.Fragment>
        <section>
          <Book />
          <Book />
          <Book />
          <Book />
        </section>
      </React.Fragment>
    );
  }
  
  const Book = () => {
    return (
      <article>
        <Image />
        <Title />
        <Author />
      </article>
    );
  };
  
  const Image = () => (
    <img
      src={"https://m.media-amazon.com/images/I/91ZVf3kNrcL._AC_UL320_.jpg"}
      alt="book"
    />
  );
  const Title = () => <h2>The Let Them Theory</h2>;
  const Author = () => {
    return <h3>by Mel Robbins and Sawyer Robbins</h3>;
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/37a278ce-a028-4969-9fbf-73d9f4a2547a)


</details>



























