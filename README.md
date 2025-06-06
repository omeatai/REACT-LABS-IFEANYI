# REACT-LABS-IFEANYI
by Ifeanyi Omeata

# React

## [React Course 1](https://www.codingaddict.io/l/products)

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
  <summary>Project Booklist - Create Structure</summary>

  ### Create Structure

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

</details>

<details>
  <summary>Project Booklist - Add Image, Title and Author from Amazon</summary>

  ### Add Image, Title and Author from Amazon

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

<details>
  <summary>Project Booklist - Add CSS Styling with Grid</summary>

  ### Add CSS Styling with Grid

  ##### lab\react\my-app\src\index.css:
  
  ```css
  * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
  }
  
  body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
          Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      background: #f1f5f8;
      color: #222;
  }
  
  .booklist {
      width: 90vw;
      max-width: 1170px;
      margin: 5rem auto;
      display: grid;
      gap: 2rem;
  }
  
  @media screen and (min-width: 768px) {
      .booklist {
          grid-template-columns: repeat(3, 1fr);
      }
  }
  
  .book {
      background: #fff;
      border-radius: 1rem;
      padding: 2rem;
      text-align: center;
  }
  
  .book img {
      width: 100%;
      object-fit: cover;
  }
  
  .book h2 {
      margin-top: 1rem;
      font-size: 1rem;
  }
  
  .book h3 {
      color: #617d98;
      font-size: 0.75rem;
      margin-top: 0.5rem;
  }
  ```

  ##### lab\react\my-app\src\index.js:

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  import "./index.css";
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
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
      <article className="book">
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

  ![image](https://github.com/user-attachments/assets/361deb16-d9d5-4371-a946-67d02d0dab3f)

</details>

<details>
  <summary>Project Booklist - Local images in Public Folder (Less Performant)</summary>

  ### Local images in Public Folder (Less Performant)

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  import "./index.css";
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
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
      <article className="book">
        <Image />
        <Title />
        <Author />
      </article>
    );
  };
  
  const Image = () => <img src={"./images/the_let_them_theory.jpg"} alt="book" />;
  const Title = () => <h2>The Let Them Theory</h2>;
  const Author = () => {
    return <h3>by Mel Robbins and Sawyer Robbins</h3>;
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/8f5d223f-8848-499f-9fa0-a05b88384d6a)

</details>

<details>
  <summary>Project Booklist - CSS in JSX</summary>

  ### CSS in JSX

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  import "./index.css";
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
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
      <article className="book">
        <Image />
        <Title />
        <Author />
      </article>
    );
  };
  
  const Image = () => <img src={"./images/the_let_them_theory.jpg"} alt="book" />;
  const Title = () => (
    <h2 style={{ color: "red", fontSize: "1rem", marginTop: "0.5rem" }}>
      The Let Them Theory
    </h2>
  );
  const Author = () => {
    const inlineStyleForAuthor = {
      color: "#617d98",
      fontSize: "0.75rem",
      marginTop: "0.25rem",
    };
    return (
      <h3 style={inlineStyleForAuthor}>by Mel Robbins and Sawyer Robbins</h3>
    );
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/837a43c4-29aa-47da-8284-ad94fe4660f4)

</details>

<details>
  <summary>Project Booklist - Javascript in JSX</summary>

  ###   ### Javascript in JSX

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const title = "The Let Them Theory";
  const author = "Mel Robbins and Sawyer Robbins";
  const image = "./images/the_let_them_theory.jpg";
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
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
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>by {author.toUpperCase()}</h3>
      </article>
    );
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/9c5628ca-fc79-4963-a183-45c16d51d183)

</details>

<details>
  <summary>Project Booklist - JSX Props</summary>

  ### JSX Props

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const firstBook = {
    title: "The Let Them Theory",
    author: "Mel Robbins and Sawyer Robbins",
    image: "./images/the_let_them_theory.jpg",
  };
  
  const secondBook = {
    title: "The Lost Bookshop",
    author: "Evie Woods",
    image: "./images/the_lost_bookshop.jpg",
  };
  
  const thirdBook = {
    title: "Hello Beautiful",
    author: "Ann Napolitano",
    image: "./images/hello_beautiful.jpg",
  };
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
          <Book {...firstBook} />
          <Book {...secondBook} />
          <Book
            title={thirdBook.title}
            author={thirdBook.author}
            image={thirdBook.image}
          />
        </section>
      </React.Fragment>
    );
  }
  
  const Book = (props) => {
    const { title, author, image } = props;
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : ""}
        </h3>
      </article>
    );
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/70695be6-264f-4dba-8895-2833c6df31c9)

</details>

<details>
  <summary>Project Booklist - Children Props</summary>

  ### Children Props

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const firstBook = {
    title: "The Let Them Theory",
    author: "Mel Robbins and Sawyer Robbins",
    image: "./images/the_let_them_theory.jpg",
  };
  
  const secondBook = {
    title: "The Lost Bookshop",
    author: "Evie Woods",
    image: "./images/the_lost_bookshop.jpg",
  };
  
  const thirdBook = {
    title: "Hello Beautiful",
    author: "Ann Napolitano",
    image: "./images/hello_beautiful.jpg",
  };
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
          <Book {...firstBook} />
          <Book {...secondBook} />
          <Book
            title={thirdBook.title}
            author={thirdBook.author}
            image={thirdBook.image}
          >
            <p>This is a text from the children prop.</p>
            <button type="button">Click me</button>
          </Book>
        </section>
      </React.Fragment>
    );
  }
  
  const Book = (props) => {
    const { title, author, image, children } = props;
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : ""}
        </h3>
        {children}
      </article>
    );
  };
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/98fe992f-bc75-4e77-a06b-6e36d5bb0825)

</details>

<details>
  <summary>Project Booklist - Displaying Lists</summary>

  ### Displaying Lists

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: "./images/the_let_them_theory.jpg",
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: "./images/the_lost_bookshop.jpg",
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: "./images/hello_beautiful.jpg",
    },
  ];
  
  const bookListMap = books.map((book) => {
    const { id, title, author, image, caption } = book;
    return (
      <Book title={title} author={author} image={image} key={id}>
        <p>{caption}</p>
        <button type="button">Click Button: {id}</button>
      </Book>
    );
  });
  
  function Book(props) {
    const { title, author, image, children } = props;
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : ""}
        </h3>
        {children}
      </article>
    );
  }
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">{bookListMap}</section>
      </React.Fragment>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/c5eb3bd8-c510-4b85-85ec-540f4cdb0e78)

</details>

<details>
  <summary>Project Booklist - Spread Objects as Props</summary>

  ### Spread Objects as Props

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: "./images/the_let_them_theory.jpg",
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: "./images/the_lost_bookshop.jpg",
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: "./images/hello_beautiful.jpg",
    },
  ];
  
  const bookListMap = books.map((book) => {
    // const { id, title, author, image, caption } = book;
    return (
      <Book {...book} key={book.id}>
        <p>{book.caption}</p>
        <button type="button">Click Button: {book.id}</button>
      </Book>
    );
  });
  
  function Book({ title, author, image, children }) {
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : ""}
        </h3>
        {children}
      </article>
    );
  }
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">{bookListMap}</section>
      </React.Fragment>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/c5eb3bd8-c510-4b85-85ec-540f4cdb0e78)

</details>


<details>
  <summary>Project Booklist - Form Events Basics</summary>

  ### Form Events Basics

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };

  const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: "./images/the_let_them_theory.jpg",
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: "./images/the_lost_bookshop.jpg",
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: "./images/hello_beautiful.jpg",
    },
  ];

  const handleFormInput = (e) => {
    const { name, value } = e.target;
    console.log(`Input Name: ${name}`);
    console.log(`Input Value: ${value}`);
  };
  
  const handleButtonClick = (e) => {
    console.log("handle button click");
  };
  
  const handleFormSubmission = (e) => {
    e.preventDefault();
    console.log("Form submitted");
  };

  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
          <form onSubmit={handleFormSubmission}>
            <input
              type="text"
              placeholder="Search for a book"
              name="search"
              onChange={handleFormInput}
            />
            <button type="submit" onClick={handleButtonClick}>
              Search
            </button>
          </form>
        </section>
        <section className="booklist">
          {books.map((book) => (
            <Book {...book} key={book.id}>
              <p>{book.caption}</p>
              <button
                type="button"
                onClick={(e) => console.log(`Clicked Button ${book.id}.`)}
              >
                Click Button: {book.id}
              </button>
            </Book>
          ))}
        </section>
      </React.Fragment>
    );
  }
  
  function Book({ title, author, image, children }) {
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : ""}
        </h3>
        {children}
      </article>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/9952f949-1138-4cc3-b9cc-d37c88eb24bd)


</details>

<details>
  <summary>Project Booklist - Component Specificity</summary>

  ### Component Specificity

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: "./images/the_let_them_theory.jpg",
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: "./images/the_lost_bookshop.jpg",
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: "./images/hello_beautiful.jpg",
    },
  ];
  
  const handleFormInput = (e) => {
    const { name, value } = e.target;
    console.log(`Input Name: ${name}`);
    console.log(`Input Value: ${value}`);
  };
  
  const handleButtonClick = (e) => {
    console.log("handle button click");
  };
  
  const handleFormSubmission = (e) => {
    e.preventDefault();
    console.log("Form submitted");
  };
  
  function BookList() {
    return (
      <React.Fragment>
        <section className="booklist">
          <form onSubmit={handleFormSubmission}>
            <input
              type="text"
              placeholder="Search for a book"
              name="search"
              onChange={handleFormInput}
            />
            <button type="submit" onClick={handleButtonClick}>
              Search
            </button>
          </form>
        </section>
        <section className="booklist">
          {books.map((book) => (
            <Book {...book} key={book.id}>
              <p>{book.caption}</p>
            </Book>
          ))}
        </section>
      </React.Fragment>
    );
  }
  
  function Book({ id, title, author, image, children }) {
    const displayTitle = () => {
      console.log(title);
      console.log(`Clicked Button ${id}.`);
      return "No Title";
    };
  
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : "No Author"}
        </h3>
        {children}
        <button type="button" onClick={(e) => displayTitle()}>
          Click Button: {id}
        </button>
      </article>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/7d3d49a4-2a3e-43a0-afd5-ee074b76f9e9)

</details>


<details>
  <summary>Project Booklist - Prop Drilling</summary>

  ### Prop Drilling

  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: "./images/the_let_them_theory.jpg",
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: "./images/the_lost_bookshop.jpg",
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: "./images/hello_beautiful.jpg",
    },
  ];
  
  const handleFormInput = (e) => {
    const { name, value } = e.target;
    console.log(`Input Name: ${name}`);
    console.log(`Input Value: ${value}`);
  };
  
  const handleButtonClick = (e) => {
    console.log("handle button click");
  };
  
  const handleFormSubmission = (e) => {
    e.preventDefault();
    console.log("Form submitted");
  };
  
  function BookList() {
    const getBook = (id) => {
      const book = books.find((book) => book.id === id);
      console.log(book);
    };
  
    return (
      <React.Fragment>
        <section className="booklist">
          <form onSubmit={handleFormSubmission}>
            <input
              type="text"
              placeholder="Search for a book"
              name="search"
              onChange={handleFormInput}
            />
            <button type="submit" onClick={handleButtonClick}>
              Search
            </button>
          </form>
        </section>
        <section className="booklist">
          {books.map(({ id, ...book }) => (
            <Book {...book} getBook={() => getBook(id)} key={id}>
              <p>{book.caption}</p>
            </Book>
          ))}
        </section>
      </React.Fragment>
    );
  }
  
  function Book({ id, title, author, image, getBook, children }) {
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : "No Author"}
        </h3>
        {children}
        <BookButton id={id} text="Get Book Title" onGetBook={getBook} />
      </article>
    );
  }
  
  function BookButton({ id, text, onGetBook }) {
    return (
      <button type="button" onClick={onGetBook}>
        {text}
      </button>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ![image](https://github.com/user-attachments/assets/eae07dd7-57d6-4af9-b093-d1a2b75a1f5f)

</details>


<details>
  <summary>Project Booklist - Split Components with ES6 Modules</summary>

  ### Split Components with ES6 Modules

  ##### index.js:
  
  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  import { books } from "./books";
  
  import {
    handleFormInput,
    handleButtonClick,
    handleFormSubmission,
  } from "./handleFunctions";
  
  import Book from "./Book";
  
  function BookList() {
    const getBook = (id) => {
      const book = books.find((book) => book.id === id);
      console.log(book);
    };
  
    return (
      <React.Fragment>
        <section className="booklist">
          <form onSubmit={handleFormSubmission}>
            <input
              type="text"
              placeholder="Search for a book"
              name="search"
              onChange={handleFormInput}
            />
            <button type="submit" onClick={handleButtonClick}>
              Search
            </button>
          </form>
        </section>
        <section className="booklist">
          {books.map(({ id, ...book }) => (
            <Book {...book} getBook={() => getBook(id)} key={id}>
              <p>{book.caption}</p>
            </Book>
          ))}
        </section>
      </React.Fragment>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ##### Book.jsx:

  ```jsx
  import { inlineStyleForAuthor, inlineStyleForTitle } from "./indexStyles";
  import BookButton from "./BookButton";
  
  const Book = ({ id, title, author, image, getBook, children }) => {
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : "No Author"}
        </h3>
        {children}
        <BookButton id={id} text="Get Book Title" onGetBook={getBook} />
      </article>
    );
  };
  
  export default Book;
  ```

  ##### BookButton.jsx:

  ```jsx
  const BookButton = ({ id, text, onGetBook }) => {
    return (
      <button type="button" onClick={onGetBook}>
        {text}
      </button>
    );
  };
  
  export default BookButton;
  ```

  ##### books.js:

  ```js
  export const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: "./images/the_let_them_theory.jpg",
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: "./images/the_lost_bookshop.jpg",
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: "./images/hello_beautiful.jpg",
    },
  ];
  ```

  ##### handleFunctions.js:

  ```js
  const handleFormInput = (e) => {
    const { name, value } = e.target;
    console.log(`Input Name: ${name}`);
    console.log(`Input Value: ${value}`);
  };
  
  const handleButtonClick = (e) => {
    console.log("handle button click");
  };
  
  const handleFormSubmission = (e) => {
    e.preventDefault();
    console.log("Form submitted");
  };
  
  export { handleFormInput, handleButtonClick, handleFormSubmission };
  ```

  ##### indexStyles.js:

  ```js
  const inlineStyleForTitle = {
    color: "red",
    fontSize: "1rem",
    marginTop: "0.5rem",
  };
  
  const inlineStyleForAuthor = {
    color: "#617d98",
    fontSize: "0.75rem",
    marginTop: "0.25rem",
  };
  
  export { inlineStyleForTitle, inlineStyleForAuthor };
  ```

</details>

<details>
  <summary>Project Booklist - Local Images in src Folder (More Performant) </summary>

  ### Local Images in src Folder

  ##### books.js:
  
  ```js
  import book1 from "./images/book1.jpg";
  import book2 from "./images/book2.jpg";
  import book3 from "./images/book3.jpg";
  
  export const books = [
    {
      id: 1,
      title: "The Let Them Theory",
      author: "Mel Robbins and Sawyer Robbins",
      image: book1,
      caption: "This is a caption from the Let Them Theory.",
    },
    {
      id: 2,
      title: "The Lost Bookshop",
      author: "Evie Woods",
      image: book2,
      caption: "This is a caption from the Lost Bookshop.",
    },
    {
      id: 3,
      title: "Hello Beautiful",
      author: "Ann Napolitano",
      image: book3,
    },
  ];
  ```

![image](https://github.com/user-attachments/assets/bbca7ff8-2bee-434f-bd23-9c1b6b91cb7c)
![image](https://github.com/user-attachments/assets/479a8283-0edc-4117-92cb-283378649368)

</details>

<details>
  <summary>Project Booklist - Book Number Tags </summary>

  ### Book Number Tags

  ##### index.js:
  
  ```js
  import React from "react";
  import ReactDOM from "react-dom/client";
  import "./index.css";
  import { books } from "./books";
  
  import {
    handleFormInput,
    handleButtonClick,
    handleFormSubmission,
  } from "./handleFunctions";
  
  import Book from "./Book";
  
  function BookList() {
    const getBook = (id) => {
      const book = books.find((book) => book.id === id);
      console.log(book);
    };
  
    return (
      <React.Fragment>
        <h1>Amazon Best Sellers</h1>
        <section className="booklist">
          <form onSubmit={handleFormSubmission}>
            <input
              type="text"
              placeholder="Search for a book"
              name="search"
              onChange={handleFormInput}
            />
            <button type="submit" onClick={handleButtonClick}>
              Search
            </button>
          </form>
        </section>
        <section className="booklist">
          {books.map(({ id, ...book }, index) => (
            <Book {...book} number={index} getBook={() => getBook(id)} key={id}>
              <p>{book.caption}</p>
            </Book>
          ))}
        </section>
      </React.Fragment>
    );
  }
  
  const root = ReactDOM.createRoot(document.getElementById("root"));
  root.render(<BookList />);
  ```

  ##### Book.jsx:
  
  ```jsx
  import { inlineStyleForAuthor, inlineStyleForTitle } from "./indexStyles";
  import BookButton from "./BookButton";
  
  const Book = ({ id, title, author, image, getBook, children, number }) => {
    return (
      <article className="book">
        <img src={image} alt="book" />
        <h2 style={inlineStyleForTitle}>{title}</h2>
        <h3 style={inlineStyleForAuthor}>
          by {author ? author.toUpperCase() : "No Author"}
        </h3>
        <span className="number">{`# ${number + 1}`}</span>
        {children}
        <BookButton
          id={id}
          text={`Get Book Title ${number + 1}`}
          onGetBook={getBook}
        />
      </article>
    );
  };
  
  export default Book;
  ```

  ##### index.css:
  
  ```css
  .book {
      background: #fff;
      border-radius: 1rem;
      padding: 2rem;
      text-align: center;
      position: relative;
  }
  
  .number {
      position: absolute;
      top: 0;
      left: 0;
      padding: 0.75rem;
      font-size: 1rem;
      border-top-left-radius: 1rem;
      border-bottom-right-radius: 1rem;
      background: red;
      color: #fff;
  }
  
  h1 {
      text-align: center;
      margin-top: 4rem;
      text-transform: capitalize;
  }
  ```

  ![image](https://github.com/user-attachments/assets/0afa0b6d-0286-4dc7-b8bf-c42f72a5e179)

</details>

<details>
  <summary>Project Booklist - Build Application and Deploy</summary>

  ### Build Application and Deploy

  ##### build App:
  
  ```
  npm run build
  ```

  ##### package.json:
  
  ```json
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
  ```

</details>

<details>
  <summary>React Hooks - Setup React App with Vite </summary>

  ### Setup React App with Vite

  ```
  npm create vite@latest my-app -- --template react
  cd my-app
  npm install
  npm run dev
  ```

  ##### main.jsx:
  
  ```jsx
  import { StrictMode } from "react";
  import { createRoot } from "react-dom/client";
  import "./index.css";
  import App from "./App.jsx";
  
  createRoot(document.getElementById("root")).render(
    // <StrictMode>
    <App />
    // </StrictMode>
  );
  ```

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import reactLogo from "./assets/react.svg";
  import viteLogo from "/vite.svg";
  import "./App.css";
  
  function App() {
    const [count, setCount] = useState(0);
  
    return (
      <>
        <div>
          <a href="https://vite.dev" target="_blank">
            <img src={viteLogo} className="logo" alt="Vite logo" />
          </a>
          <a href="https://react.dev" target="_blank">
            <img src={reactLogo} className="logo react" alt="React logo" />
          </a>
        </div>
        <h1>Vite + React</h1>
        <div className="card">
          <button onClick={() => setCount((count) => count + 1)}>
            count is {count}
          </button>
          <p>
            Edit <code>src/App.jsx</code> and save to test HMR
          </p>
        </div>
        <p className="read-the-docs">
          Click on the Vite and React logos to learn more
        </p>
      </>
    );
  }
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/2b2eabdb-b716-42e0-806f-a83e5a731991)

</details>

<details>
  <summary>React Hooks - UseState Basics </summary>

  ### UseState Basics

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <UseStateBasics />;
  }
  
  const UseStateBasics = () => {
    const [value, setValue] = useState(101);
    const [count, setCount] = useState(0);
    const rooms = [101, 103, 107, 109, 112];
  
    const toggleRooms = () => {
      if (value === rooms[rooms.length - 1]) {
        setValue(rooms[0]);
        setCount((prevCount) => prevCount + 1);
      } else {
        setValue(rooms[rooms.indexOf(value) + 1]);
        setCount((prevCount) => prevCount + 1);
      }
      console.log(`count: ${count}, value: ${value}`);
    };
  
    return (
      <>
        <h2>useState basics - Room {value}</h2>
        <h3>You have clicked {count} times</h3>
        <button onClick={toggleRooms}>Toggle Rooms</button>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/a5c2b148-0f44-4567-9e0f-56e6ed770f8f)

</details>

<details>
  <summary>React Hooks - UseState on Arrays </summary>

  ### UseState on Arrays

  ##### data.js:
  
  ```js
  export const data = [
    { id: 1, name: "john" },
    { id: 2, name: "peter" },
    { id: 3, name: "susan" },
    { id: 4, name: "anna" },
  ];
  
  export const people = [
    { id: 1, name: "bob", nickName: "Stud Muffin" },
    { id: 2, name: "peter" },
    {
      id: 3,
      name: "oliver",
      images: [
        {
          small: {
            url: "https://res.cloudinary.com/diqqf3eq2/image/upload/ar_1:1,bo_5px_solid_rgb:ff0000,c_fill,g_auto,r_max,w_1000/v1595959121/person-1_aufeoq.jpg",
          },
        },
      ],
    },
    { id: 4, name: "david" },
  ];
  ```

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  import { data } from "./db/data";
  
  function App() {
    return <UseStateArray />;
  }
  
  const UseStateArray = () => {
    const [people, setPeople] = useState(data);
    const [name, setName] = useState("");
  
    const handleRemoveItem = (id) => {
      const newPeople = people.filter((person) => {
        return person.id !== id;
      });
      setPeople(newPeople);
    };
  
    const handleClearAllItems = () => {
      setPeople([]);
    };
  
    const handleReset = () => {
      setPeople(data);
    };
  
    const handleAddItem = () => {
      if (name) {
        setPeople([...people, { id: people.length + 1, name: name }]);
        setName("");
      }
    };
  
    return (
      <>
        <h1>Team Members</h1>
        <section style={{ display: "flex", gap: "10px", marginBottom: "10px" }}>
          <button
            style={{ backgroundColor: "red" }}
            onClick={handleClearAllItems}
          >
            Clear All
          </button>
          <button onClick={handleReset}>Reset All</button>
          <input
            type="text"
            placeholder="Name"
            name="personName"
            value={name}
            onChange={(e) => setName(e.target.value)}
          />
          <button onClick={handleAddItem}>Add Item</button>
        </section>
        <section>
          {people.map((person) => {
            const { id, name } = person;
            return (
              <div key={id}>
                <h2>{name[0].toUpperCase() + name.slice(1)}</h2>
                <button onClick={() => handleRemoveItem(id)}>Delete</button>
              </div>
            );
          })}
        </section>
      </>
    );
  };
  
  export default App;
  ```

![image](https://github.com/user-attachments/assets/7e145447-b6cd-4c1e-89ff-0e104f9a74f7)


</details>

<details>
  <summary>React Hooks - UseState on Objects </summary>

  ### useState on Objects 

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <UseStateObject />;
  }
  
  const UseStateObject = () => {
    const [person, setPerson] = useState({
      name: "John",
      age: 20,
      message: "Hello, John!",
    });
  
    const handleChangeMessage = () => {
      setPerson({
        ...person,
        message: "Yey! That's great! Welcome to the team!",
      });
    };
  
    return (
      <>
        <h1>Team Members</h1>
        <section>
          <h2>{person.name}</h2>
          <h2>{person.age}</h2>
          <h2>{person.message}</h2>
          <button onClick={handleChangeMessage}>Change Message</button>
        </section>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/716cb596-2068-4991-88a0-1ff27ca98304)

</details>

<details>
  <summary>React Hooks - UseState on setTimeout </summary>

  ### UseState on setTimeout

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <UseStateSetTimeout />;
  }
  
  const UseStateSetTimeout = () => {
    const [value, setValue] = useState(0);
  
    const handleClick = () => {
      setTimeout(() => {
        setValue((prevValue) => prevValue + 1);
      }, 2000);
    };
  
    return (
      <>
        <h1>Number of people</h1>
        <section>
          <h2>{value}</h2>
          <button onClick={handleClick}>Click me</button>
        </section>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/f059f306-d026-42e1-b221-6f1c6a6b63d5)

</details>

<details>
  <summary>React Hooks - useEffect Basics </summary>

  ### useEffect Basics

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  
  function App() {
    return <UseEffectBasics />;
  }
  
  const UseEffectBasics = () => {
    const [value, setValue] = useState(0);
    const [count, setCount] = useState(0);
  
    const handleClick = () => {
      setValue((prevValue) => prevValue + 2);
    };
  
    const handleCount = () => {
      setCount((prevCount) => prevCount + 1);
    };
  
    useEffect(() => {
      console.log("Welcome to first render.");
    }, []);
  
    useEffect(() => {
      console.log("Value is: ", value);
      console.log("Count is: ", count);
    }, [value, count]);
  
    return (
      <>
        <h1>Let's count!</h1>
        <section>
          <h2>Value: {value}</h2>
          <button onClick={handleClick}>Increase Value</button>
          <h2>Count: {count}</h2>
          <button onClick={handleCount}>IncreaseCount</button>
        </section>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/9157fa26-a378-46c1-b09f-ea07caa2091a)

</details>

<details>
  <summary>React Hooks - useEffect with Fetch Data </summary>

  ### useEffect with Fetch Data

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  
  function App() {
    return <UseEffectFetchData />;
  }
  
  const styles = {
    card: {
      display: "flex",
      gap: "10px",
      backgroundColor: "#f0f0f0",
      padding: "10px",
      margin: "10px",
    },
  };
  
  const UseEffectFetchData = () => {
    const [users, setUsers] = useState([]);
    const url = "https://api.github.com/users";
  
    useEffect(() => {
      // fetch(url)
      //   .then((response) => response.json())
      //   .then((data) => console.log(data))
      //   .catch((error) => console.log(error));
  
      const fetchUsers = async () => {
        try {
          const response = await fetch(url);
          const users = await response.json();
          console.log(users);
          setUsers(users);
        } catch (error) {
          console.log(error);
        }
      };
  
      fetchUsers();
    }, []);
  
    return (
      <>
        <h1>Fetch Data Example</h1>
        <h2>Github Users</h2>
  
        {users.map((user) => {
          const { id, login, avatar_url, html_url } = user;
          return (
            <section key={id} style={styles.card}>
              <div className="img-container">
                <img src={avatar_url} alt={login} width={150} height={150} />
              </div>
              <div className="user-info">
                <h3>{login}</h3>
                <h4>
                  <a href={html_url}>Profile</a>
                </h4>
              </div>
            </section>
          );
        })}
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/95f998ce-a027-4331-8bd2-70bc544881bc)

</details>

<details>
  <summary>React Hooks - useEffect with Conditional Rendering (isLoading) </summary>

  ### useEffect with Conditional Rendering (isLoading)

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  
  function App() {
    return <UseEffectConditionalRendering />;
  }
  
  const UseEffectConditionalRendering = () => {
    const [isLoading, setIsLoading] = useState(true);
  
    useEffect(() => {
      setTimeout(() => {
        setIsLoading(false);
      }, 3000);
    }, []);
  
    if (isLoading) {
      return <h1>Loading...</h1>;
    }
  
    return (
      <>
        <h1>Fetch Data Example</h1>
        <h2>Github Users</h2>
      </>
    );
  };
  
  export default App;  
  ```

  ![image](https://github.com/user-attachments/assets/a2a77087-bf6f-462c-a484-a5bfe861209d)
  ![image](https://github.com/user-attachments/assets/d7420c66-f474-4d7f-92bb-cd4ed3bec29a)

</details>

<details>
  <summary>React Hooks - useEffect with Multiple Promises and Returns (isLoading, setIsError) </summary>

  ### useEffect with Multiple Promises and Returns (isLoading, setIsError)

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  const url = "https://api.github.com/users/QuincyLarson";
  
  function App() {
    return <UseEffectMultipleReturns />;
  }
  
  const UseEffectMultipleReturns = () => {
    const [user, setUser] = useState(null);
    const [isLoading, setIsLoading] = useState(true);
    const [isError, setIsError] = useState(false);
  
    useEffect(() => {
      const fetchUsers = async () => {
        try {
          const timeoutPromise = new Promise((resolve) =>
            setTimeout(resolve, 3000)
          );
          const fetchPromise = fetch(url);
          const [response] = await Promise.all([fetchPromise, timeoutPromise]);
  
          if (!response.ok) {
            setIsError(true);
            setIsLoading(false);
            return;
          }
          const user = await response.json();
          setUser(user);
          setIsError(false);
        } catch (error) {
          console.log(error);
          setIsError(true);
        }
        setIsLoading(false);
      };
      fetchUsers();
    }, []);
  
    if (isLoading) {
      return <h1>Loading...</h1>;
    }
  
    if (isError) {
      return <h1>There was an error...</h1>;
    }
  
    return (
      <>
        <h1>Fetch Data Example</h1>
        <h2>Github Users</h2>
  
        <img
          src={user.avatar_url}
          alt={user.name}
          width={150}
          height={150}
          style={{ borderRadius: "25px" }}
        />
        <h3>{user.name}</h3>
        <h4>Works at {user.company}</h4>
        <p>{user.bio}</p>
        <h5>
          Followers: {user.followers} | Following: {user.following} | Public
          Repos: {user.public_repos} | Public Gists: {user.public_gists}
        </h5>
        <a href={user.html_url} className="btn">
          View Profile
        </a>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/865ba73e-f806-4408-a114-cefe97205fad)

</details>

<details>
  <summary>React Hooks - Falsy and Truthy Logical Operators </summary>

  ### Falsy and Truthy Logical Operators

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  // import { useState, useEffect } from "react";
  import "./App.css";
  // const url = "https://api.github.com/users/QuincyLarson";
  
  function App() {
    return <TruthyFalsyLogicalOperators />;
  }
  
  const TruthyFalsyLogicalOperators = () => {
    function displayUser(name1, name2) {
      return name1 || name2;
    }
  
    function displayNumber(number1, number2) {
      return number1 && number2;
    }
  
    return (
      <>
        <h1>Display Users</h1>
        <h2>{displayUser("Frank Bourges", "John Smith")}</h2>
        <h2>{displayUser("Frank Bourges", null)}</h2>
        <h2>{displayUser(null, "Frank Bourges")}</h2>
        <h2>{displayNumber(1, 2)}</h2>
        <h2>{displayNumber(1, 0)}</h2>
        <h2>{displayNumber(0, 1)}</h2>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/fa9ce44f-370c-419b-96e6-2f4086d57def)

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <TruthyFalsyLogicalOperators />;
  }
  
  const TruthyFalsyLogicalOperators = () => {
    const [text, setText] = useState("");
    const [name, setName] = useState("John Smith");
  
    return (
      <>
        <h1>Truthy Falsy Logical Operators</h1>
        <h2>Falsy OR : {text || "default value"}</h2>
        <h2>Falsy AND : {text && "Hello World"}</h2>
        <h2>Truthy OR : {name || "default value"}</h2>
        <h2>Truthy AND : {name && "Hello World"}</h2>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/3a60cec9-c913-416d-9abf-2305dcfba923)

</details>

<details>
  <summary>React Hooks - Short Circuit Operators </summary>

  ### Short Circuit Operators

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <ShortCircuitOperators />;
  }
  
  const ShortCircuitOperators = () => {
    const [greeting, setGreeting] = useState("Welcome to my Website!");
    const [name, setName] = useState("Susan Jones");
    const [isOpen, setIsOpen] = useState(true);
  
    return (
      <>
        <h1>{greeting || "default value"}</h1>
        {isOpen && <div>{name && <SomeComponent personsName={name} />}</div>}
        <button onClick={() => setIsOpen(!isOpen)}>Toggle Show Name</button>
      </>
    );
  };
  
  const SomeComponent = ({ personsName }) => {
    return (
      <>
        <h2>{`My name is ${personsName}`}</h2>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/c26965c5-645d-48a3-84f4-1215bee68748)

</details>

<details>
  <summary>React Hooks - Ternary Operator </summary>

  ### Ternary Operator

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <TernaryOperator />;
  }
  
  const TernaryOperator = () => {
    const [greeting, setGreeting] = useState("Welcome to my Website!");
    const [name, setName] = useState("Susan Jones");
    const [isOpen, setIsOpen] = useState(true);
  
    return (
      <>
        <h1>{greeting || "default value"}</h1>
        {isOpen ? (
          <div>{name && <SomeComponent personsName={name} />}</div>
        ) : (
          <div>
            <SomeComponent personsName="********" />
          </div>
        )}
        <button
          onClick={() => setIsOpen(!isOpen)}
          style={{
            backgroundColor: !isOpen ? "red" : "indigo",
            color: "white",
            padding: "10px 20px",
            borderRadius: "5px",
            border: "none",
            cursor: "pointer",
          }}
        >
          {isOpen ? "Hide Name" : "Show Name"}
        </button>
      </>
    );
  };
  
  const SomeComponent = ({ personsName }) => {
    return (
      <>
        <h2>{`My name is ${personsName}`}</h2>
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/ffc49c8e-735a-447a-9a6a-4712ac47568f)
  ![image](https://github.com/user-attachments/assets/b22903a4-0b43-4a19-8530-0db4b6cab635)

</details>

<details>
  <summary>React Hooks - Login and Logout User </summary>

  ### Login and Logout User

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return <LoginAndLogoutUser />;
  }
  
  const LoginAndLogoutUser = () => {
    const [dbUser, setDbUser] = useState({
      name: "John Doe",
      email: "john.doe@gmail.com",
      password: "123456",
    });
  
    const [user, setUser] = useState(null);
    const [formData, setFormData] = useState({
      email: "",
      password: "",
    });
  
    const handleLogin = () => {
      if (
        formData.email === dbUser.email &&
        formData.password === dbUser.password
      ) {
        setUser(dbUser);
        setFormData({ email: "", password: "" });
      } else {
        alert("Invalid credentials");
      }
    };
  
    const handleFormChange = (e) => {
      console.log(e.target.name, e.target.value);
      setFormData({ ...formData, [e.target.name]: e.target.value });
    };
  
    const handleLogout = () => {
      setUser(null);
    };
  
    return (
      <>
        {!user ? (
          <>
            <h1>Welcome, Please Login</h1>
            <form
              onSubmit={handleLogin}
              style={{
                display: "flex",
                flexDirection: "column",
                gap: "10px",
                width: "300px",
                margin: "0 auto",
              }}
            >
              <input
                type="text"
                placeholder="Email"
                name="email"
                value={formData.email}
                onChange={handleFormChange}
              />
              <input
                type="password"
                placeholder="Password"
                name="password"
                value={formData.password}
                onChange={handleFormChange}
              />
              <button
                type="submit"
                style={{
                  backgroundColor: "blue",
                  color: "white",
                  cursor: "pointer",
                  border: "none",
                  padding: "10px 20px",
                }}
              >
                Login
              </button>
            </form>
          </>
        ) : (
          <>
            <h1>Welcome to your Account, {user.name?.toUpperCase()}</h1>
            <h3>Name: {user.name}</h3>
            <h3>Email: {user.email}</h3>
            <button
              onClick={handleLogout}
              style={{
                backgroundColor: "red",
                color: "white",
                cursor: "pointer",
                border: "none",
                padding: "10px 80px",
              }}
            >
              Logout
            </button>
          </>
        )}
      </>
    );
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/323de8e1-d13d-42e2-a55f-07b1ec14baea)
  ![image](https://github.com/user-attachments/assets/01c334da-8182-4780-9a16-2ee2a00ae059)

</details>

<details>
  <summary>React Hooks - UseEffect Cleanup Function for setInterval </summary>

  ### UseEffect Cleanup Function for setInterval

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  
  function App() {
    return <CleanUpFunction />;
  }
  
  const CleanUpFunction = () => {
    const [toggle, setToggle] = useState(false);
  
    return (
      <>
        <h2>Hello</h2>
        <button className="btn" onClick={() => setToggle(!toggle)}>
          Toggle Component
        </button>
        {toggle && <MyComponent />}
      </>
    );
  };
  
  const MyComponent = () => {
    useEffect(() => {
      console.log("Mounting....");
      const myInt = setInterval(() => {
        console.log("Interval....");
      }, 1000);
  
      return () => {
        console.log("Unmounting....");
        clearInterval(myInt);
      };
    }, []);
  
    return <h2>My Component</h2>;
  };
  
  export default App;
  ```
  
  ![image](https://github.com/user-attachments/assets/a1b57dd1-95e2-4189-9bf3-d667bfb65b6d)

</details>

<details>
  <summary>React Hooks - UseEffect Cleanup Function for Event Listeners </summary>

  ### UseEffect Cleanup Function for Event Listeners
  
  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  
  function App() {
    return <CleanUpFunction />;
  }
  
  const CleanUpFunction = () => {
    const [toggle, setToggle] = useState(false);
  
    return (
      <>
        <h2>Hello</h2>
        <button className="btn" onClick={() => setToggle(!toggle)}>
          Toggle Component
        </button>
        {toggle && <MyComponent />}
      </>
    );
  };
  
  const MyComponent = () => {
    useEffect(() => {
      console.log("Mounting....");
      const myFunc = () => {
        console.log("Running myFunc....");
      };
      myFunc();
      window.addEventListener("scroll", myFunc);
  
      return () => {
        console.log("Unmounting....");
        window.removeEventListener("scroll", myFunc);
      };
    }, []);
  
    return <h2>My Component</h2>;
  };
  
  export default App;
  ```

  ![image](https://github.com/user-attachments/assets/c7c96d72-b1f7-47de-a001-7102eda2b164)

</details>

<details>
  <summary>React Project Structure Setup </summary>

  ### React Project Structure Setup

  ##### react\my-app\src\main.jsx:
  
  ```jsx
  import { StrictMode } from "react";
  import { createRoot } from "react-dom/client";
  import "./index.css";
  import App from "./App.jsx";
  
  createRoot(document.getElementById("root")).render(
    // <StrictMode>
    <App />
    // </StrictMode>
  );
  ```

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import "./App.css";
  import Navbar from "./components/Navbar";
  import { Home, About } from "./pages";
  
  function App() {
    return (
      <>
        <h1>Welcome to my App</h1>
        <Navbar />
        <Home />
        <About />
      </>
    );
  }
  
  export default App;
  ```

  ##### react\my-app\src\pages\index.jsx:
  
  ```jsx
  import Home from "./Home";
  import About from "./About";
  
  export { Home, About };
  ```

  ##### react\my-app\src\pages\Home.jsx:
  
  ```jsx
  import React from "react";
  
  const Home = () => {
    return (
      <div>
        <h1>Home</h1>
      </div>
    );
  };
  
  export default Home;
  ```

  ##### react\my-app\src\pages\About.jsx:
  
  ```jsx
  import React from "react";
  
  const About = () => {
    return (
      <div>
        <h1>About</h1>
      </div>
    );
  };
  
  export default About;
  ```

  ##### react\my-app\src\components\Navbar\index.jsx:
  
  ```jsx
  import Navbar from "./Navbar";
  export default Navbar;
  
  // export { default } from "./Navbar";
  ```

  ##### react\my-app\src\components\Navbar\Navbar.jsx:
  
  ```jsx
  import React from "react";
  
  const Navbar = () => {
    return (
      <nav>
        <h2>Navbar</h2>
        <ul>
          <li>Home</li>
          <li>About</li>
          <li>Contact</li>
        </ul>
      </nav>
    );
  };
  
  export default Navbar;
  ```

  ![image](https://github.com/user-attachments/assets/ae3e5816-3fe9-4c4c-bc1a-e4d29d48fff3)
  ![image](https://github.com/user-attachments/assets/c60c2a4c-4e12-40f4-b04b-26fc3810c0b3)

</details>

<details>
  <summary>Optional Chaining with Default Values </summary>

  ### Optional Chaining with Default Values 

   ##### react\my-app\src\main.jsx:
  
  ```jsx
  import { StrictMode } from "react";
  import { createRoot } from "react-dom/client";
  import "./index.css";
  import App from "./App.jsx";
  
  createRoot(document.getElementById("root")).render(
    // <StrictMode>
    <App />
    // </StrictMode>
  );
  ```
  
  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import "./App.css";
  
  import List from "./components/List/List";
  
  function App() {
    return (
      <>
        <List />
      </>
    );
  }
  
  export default App;
  ```

  ##### react\my-app\src\db\data.js:
  
  ```jsx
  export const data = [
    { id: 1, name: "john" },
    { id: 2, name: "peter" },
    { id: 3, name: "susan" },
    { id: 4, name: "anna" },
  ];
  
  export const people = [
    { id: 1, name: "bob", nickName: "Stud Muffin" },
    { id: 2, name: "peter" },
    {
      id: 3,
      name: "oliver",
      images: [
        {
          small: {
            url: "https://res.cloudinary.com/diqqf3eq2/image/upload/ar_1:1,bo_5px_solid_rgb:ff0000,c_fill,g_auto,r_max,w_1000/v1595959121/person-1_aufeoq.jpg",
          },
        },
      ],
    },
    { id: 4, name: "david" },
  ];
  ```

  ##### react\my-app\src\components\List\List.jsx:
  
  ```jsx
  import React from "react";
  
  import Person from "../Person";
  import { people } from "../../db/data";
  
  const List = () => {
    return (
      <div>
        <h1>People List</h1>
        {people.map((person) => {
          return <Person key={person.id} {...person} />;
        })}
      </div>
    );
  };
  
  export default List;
  ```

  ##### react\my-app\src\components\List\index.jsx:
  
  ```jsx
  export { default } from "./List";
  ```

  ##### react\my-app\src\components\Person\Person.jsx:
  
  ```jsx
  import React from "react";
  import user from "../../assets/user.png";
  
  const Person = ({ name, nickName = "[None]", images }) => {
    // const img = images && images[0] && images[0].small && images[0].small.url;
    // const img = images?.[0]?.small?.url ?? user;
    const img = images?.[0]?.small?.url || user;
  
    return (
      <>
        <img src={img} alt={name} width={100} height={100} />
        <h3>{name[0].toUpperCase() + name.slice(1)}</h3>
        <h4>Nickname: {nickName} </h4>
      </>
    );
  };
  
  export default Person;
  ```

  ##### react\my-app\src\components\Person\index.jsx:
  
  ```jsx
  export { default } from "./Person";
  ```

  ##### react\my-app\src\App.css:
  
  ```css
    #root {
      max-width: 1280px;
      margin: 0 auto;
      padding: 2rem;
      text-align: center;
  }
  
  a {
      font-weight: 500;
      color: #646cff;
      text-decoration: inherit;
  }
  
  a:hover {
      color: #535bf2;
  }
  
  body {
      margin: 0;
      display: flex;
      place-items: center;
      min-width: 320px;
      min-height: 100vh;
  }
  
  h1 {
      font-size: 3.2em;
      line-height: 1.1;
  }
  
  button {
      border-radius: 8px;
      border: 1px solid transparent;
      padding: 0.6em 1.2em;
      font-size: 1em;
      font-weight: 500;
      font-family: inherit;
      /* background-color: #1a1a1a; */
      cursor: pointer;
      transition: border-color 0.25s;
  }
  
  button:hover {
      border-color: #646cff;
  }
  
  button:focus,
  button:focus-visible {
      outline: 4px auto -webkit-focus-ring-color;
  }
  ```

  ![image](https://github.com/user-attachments/assets/feab6768-0204-4926-99e3-78448ac8493a)

</details>

<details>
  <summary>React Forms - Controlled Inputs </summary>

  ### Controlled Inputs

  ##### App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return (
      <>
        <ControlledInputs />
      </>
    );
  }
  
  export default App;
  
  const ControlledInputs = () => {
    const [name, setName] = useState("");
    const [email, setEmail] = useState("");
  
    // const handleChange = (e) => {
    //   if (e.target.name === "name") {
    //     setName(e.target.value);
    //     console.log(name);
    //   } else if (e.target.name === "email") {
    //     setEmail(e.target.value);
    //     console.log(email);
    //   }
    // };
  
    const handleSubmit = (e) => {
      e.preventDefault();
      if (name && email) {
        console.log(name, email);
      } else {
        console.log("Invalid data");
      }
    };
  
    return (
      <div>
        <form className="form" onSubmit={handleSubmit}>
          <h1>Controlled Inputs</h1>
          <div className="form-row">
            <label htmlFor="name" className="form-label">
              Name
            </label>
            <input
              type="text"
              id="name"
              name="name"
              value={name}
              onChange={(e) => setName(e.target.value)}
              className="form-input"
            />
          </div>
          <div className="form-row">
            <label htmlFor="email" className="form-label">
              Email
            </label>
            <input
              type="email"
              id="email"
              name="email"
              value={email}
              onChange={(e) => setEmail(e.target.value)}
              className="form-input"
            />
          </div>
          <button type="submit" className="btn btn-block">
            submit
          </button>
        </form>
      </div>
    );
  };
  ```

  ##### App.css:
  
  ```css
  #root {
      max-width: 1280px;
      margin: 0 auto;
      padding: 2rem;
      text-align: center;
  
      /* colors */
      --primary-100: #e2e0ff;
      --primary-200: #c1beff;
      --primary-300: #a29dff;
      --primary-400: #837dff;
      --primary-500: #645cff;
      --primary-600: #504acc;
      --primary-700: #3c3799;
      --primary-800: #282566;
      --primary-900: #141233;
  
      /* grey */
      --grey-50: #f8fafc;
      --grey-100: #f1f5f9;
      --grey-200: #e2e8f0;
      --grey-300: #cbd5e1;
      --grey-400: #94a3b8;
      --grey-500: #64748b;
      --grey-600: #475569;
      --grey-700: #334155;
      --grey-800: #1e293b;
      --grey-900: #0f172a;
      /* rest of the colors */
      --black: #222;
      --white: #fff;
      --red-light: #f8d7da;
      --red-dark: #842029;
      --green-light: #d1e7dd;
      --green-dark: #0f5132;
  
      /* fonts  */
  
      --small-text: 0.875rem;
      --extra-small-text: 0.7em;
      /* rest of the vars */
      --backgroundColor: var(--grey-50);
      --textColor: var(--grey-900);
      --borderRadius: 0.25rem;
      --letterSpacing: 1px;
      --transition: 0.3s ease-in-out all;
      --max-width: 1120px;
      --fixed-width: 600px;
  
      /* box shadow*/
      --shadow-1: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
      --shadow-2: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
          0 2px 4px -1px rgba(0, 0, 0, 0.06);
      --shadow-3: 0 10px 15px -3px rgba(0, 0, 0, 0.1),
          0 4px 6px -2px rgba(0, 0, 0, 0.05);
      --shadow-4: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
          0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
  
  
  a {
      font-weight: 500;
      color: #646cff;
      text-decoration: inherit;
  }
  
  a:hover {
      color: #535bf2;
  }
  
  body {
      margin: 0;
      display: flex;
      place-items: center;
      min-width: 320px;
      min-height: 100vh;
  }
  
  h1 {
      font-size: 3.2em;
      line-height: 1.1;
  }
  
  button {
      border-radius: 8px;
      border: 1px solid transparent;
      padding: 0.6em 1.2em;
      font-size: 1em;
      font-weight: 500;
      font-family: inherit;
      /* background-color: #1a1a1a; */
      cursor: pointer;
      transition: border-color 0.25s;
  }
  
  button:hover {
      border-color: #646cff;
  }
  
  button:focus,
  button:focus-visible {
      outline: 4px auto -webkit-focus-ring-color;
  }
  
  /* form */
  
  .form {
      width: 90vw;
      max-width: var(--fixed-width);
      background: var(--white);
      border-radius: var(--borderRadius);
      box-shadow: var(--shadow-2);
      padding: 2rem 2.5rem;
      margin: 3rem auto;
  }
  
  .form-label {
      display: block;
      font-size: var(--small-text);
      margin-bottom: 0.5rem;
      text-transform: capitalize;
      letter-spacing: var(--letterSpacing);
  }
  
  .form-input,
  .form-textarea {
      width: 100%;
      padding: 0.375rem 0.75rem;
      border-radius: var(--borderRadius);
      background: var(--backgroundColor);
      border: 1px solid var(--grey-200);
  }
  
  .form-row {
      margin-bottom: 1rem;
  }
  
  .form-textarea {
      height: 7rem;
  }
  
  ::placeholder {
      font-family: inherit;
      color: var(--grey-400);
  }
  
  .form-alert {
      color: var(--red-dark);
      letter-spacing: var(--letterSpacing);
      text-transform: capitalize;
  }
  
  /* extra styles */
  .form .form-label {
      text-align: left;
  }
  
  .form .btn-block {
      margin-top: 0.5rem;
  }
  
  /* buttons */
  
  .btn {
      cursor: pointer;
      color: var(--white);
      background: var(--primary-500);
      border: transparent;
      border-radius: var(--borderRadius);
      letter-spacing: var(--letterSpacing);
      padding: 0.375rem 0.75rem;
      box-shadow: var(--shadow-1);
      transition: var(--transition);
      text-transform: capitalize;
      display: inline-block;
  }
  
  .btn:hover {
      background: var(--primary-700);
      box-shadow: var(--shadow-3);
  }
  
  .btn-hipster {
      color: var(--primary-500);
      background: var(--primary-200);
  }
  
  .btn-hipster:hover {
      color: var(--primary-200);
      background: var(--primary-700);
  }
  
  .btn-block {
      width: 100%;
  }
  ```

  ![image](https://github.com/user-attachments/assets/b3f1aa7c-a47e-48b2-9a9d-bc46be46e4b0)

</details>

<details>
  <summary>React Forms - Add and Remove Users (Filter and Find) </summary>

  ### Add and Remove Users (Filter and Find)

  ##### App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  import { data } from "./db/data";
  import user from "./assets/user.png";
  
  function App() {
    return (
      <>
        <ControlledInputs />
      </>
    );
  }
  
  export default App;
  
  const ControlledInputs = () => {
    const [people, setPeople] = useState(data);
    const [name, setName] = useState("");
  
    const handleSubmit = (e) => {
      e.preventDefault();
      // if (!name) return;
      if (!name) {
        alert("Please enter a name");
        return;
      }
  
      const newPerson = { id: Date.now(), name };
      const updatedPeople = [newPerson, ...people];
      setPeople(updatedPeople);
      setName("");
      console.log(`Added ${newPerson.name} to the list`);
    };
  
    const removePerson = (id) => {
      const removedPerson = people.find((person) => person.id === id);
      const updatedPeople = people.filter((person) => person.id !== id);
      setPeople(updatedPeople);
      console.log(`Removed ${removedPerson.name} from the list`);
    };
  
    return (
      <div>
        <form className="form" onSubmit={handleSubmit}>
          <h1>Add User</h1>
          <div className="form-row">
            <label htmlFor="name" className="form-label">
              Name
            </label>
            <input
              type="text"
              id="name"
              name="name"
              value={name}
              onChange={(e) => setName(e.target.value)}
              className="form-input"
            />
          </div>
          <button type="submit" className="btn btn-block">
            submit
          </button>
        </form>
        <section
          style={{ display: "flex", flexDirection: "column", gap: "20px" }}
        >
          {people.map((person) => {
            const cleanedName =
              person.name.slice(0, 1).toUpperCase() + person.name.slice(1);
            return (
              <div key={person.id}>
                <img
                  src={person?.img || user}
                  alt={person.name}
                  width={50}
                  height={50}
                />
                <h4>{cleanedName}</h4>
                <button onClick={() => removePerson(person.id)}>
                  remove {cleanedName}
                </button>
              </div>
            );
          })}
        </section>
      </div>
    );
  };
  ```

  ![image](https://github.com/user-attachments/assets/6d154823-79fb-4a8d-a522-47037220de04)

</details>

<details>
  <summary>React Forms - Handle Multiple Inputs </summary>

  ### Handle Multiple Inputs

  ##### react\my-app\src\App.jsx:
  
  ```jsx
  import { useState, useEffect } from "react";
  import "./App.css";
  
  function App() {
    return (
      <>
        <ControlledInputs />
      </>
    );
  }
  
  export default App;
  
  const ControlledInputs = () => {
    const [user, setUser] = useState({ name: "", email: "", password: "" });
  
    const handleChange = (e) => {
      setUser({ ...user, [e.target.name]: e.target.value });
    };
  
    // useEffect(() => {
    //   console.log(`user: ${user.name} - ${user.email} - ${user.password}`);
    // }, [user]);
  
    const handleSubmit = (e) => {
      e.preventDefault();
      console.log(user);
    };
  
    return (
      <div>
        <form className="form" onSubmit={handleSubmit}>
          <h1>Multiple Inputs</h1>
          <div className="form-row">
            <label htmlFor="name" className="form-label">
              Name
            </label>
            <input
              type="text"
              id="name"
              name="name"
              value={user.name}
              onChange={handleChange}
              className="form-input"
            />
          </div>
          <div className="form-row">
            <label htmlFor="email" className="form-label">
              Email
            </label>
            <input
              type="email"
              id="email"
              name="email"
              value={user.email}
              onChange={handleChange}
              className="form-input"
            />
          </div>
          <div className="form-row">
            <label htmlFor="password" className="form-label">
              Password
            </label>
            <input
              type="password"
              id="password"
              name="password"
              value={user.password}
              onChange={handleChange}
              className="form-input"
            />
          </div>
          <button type="submit" className="btn btn-block">
            submit
          </button>
        </form>
        <section className="info">
          <h3>Info</h3>
          <h5>name: {user.name}</h5>
          <h5>email: {user.email}</h5>
          <h5>password: {user.password}</h5>
        </section>
      </div>
    );
  };
  ```

  ##### react\my-app\src\App.css:
  
  ```css
  #root {
      max-width: 1280px;
      margin: 0 auto;
      padding: 2rem;
      text-align: center;
  
      /* colors */
      --primary-100: #e2e0ff;
      --primary-200: #c1beff;
      --primary-300: #a29dff;
      --primary-400: #837dff;
      --primary-500: #645cff;
      --primary-600: #504acc;
      --primary-700: #3c3799;
      --primary-800: #282566;
      --primary-900: #141233;
  
      /* grey */
      --grey-50: #f8fafc;
      --grey-100: #f1f5f9;
      --grey-200: #e2e8f0;
      --grey-300: #cbd5e1;
      --grey-400: #94a3b8;
      --grey-500: #64748b;
      --grey-600: #475569;
      --grey-700: #334155;
      --grey-800: #1e293b;
      --grey-900: #0f172a;
      /* rest of the colors */
      --black: #222;
      --white: #fff;
      --red-light: #f8d7da;
      --red-dark: #842029;
      --green-light: #d1e7dd;
      --green-dark: #0f5132;
  
      /* fonts  */
  
      --small-text: 0.875rem;
      --extra-small-text: 0.7em;
      /* rest of the vars */
      --backgroundColor: var(--grey-50);
      --textColor: var(--grey-900);
      --borderRadius: 0.25rem;
      --letterSpacing: 1px;
      --transition: 0.3s ease-in-out all;
      --max-width: 1120px;
      --fixed-width: 600px;
  
      /* box shadow*/
      --shadow-1: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
      --shadow-2: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
          0 2px 4px -1px rgba(0, 0, 0, 0.06);
      --shadow-3: 0 10px 15px -3px rgba(0, 0, 0, 0.1),
          0 4px 6px -2px rgba(0, 0, 0, 0.05);
      --shadow-4: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
          0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
  
  
  a {
      font-weight: 500;
      color: #646cff;
      text-decoration: inherit;
  }
  
  a:hover {
      color: #535bf2;
  }
  
  body {
      margin: 0;
      display: flex;
      place-items: center;
      min-width: 320px;
      min-height: 100vh;
  }
  
  h1 {
      font-size: 3.2em;
      line-height: 1.1;
  }
  
  button {
      border-radius: 8px;
      border: 1px solid transparent;
      padding: 0.6em 1.2em;
      font-size: 1em;
      font-weight: 500;
      font-family: inherit;
      /* background-color: #1a1a1a; */
      cursor: pointer;
      transition: border-color 0.25s;
  }
  
  button:hover {
      border-color: #646cff;
  }
  
  button:focus,
  button:focus-visible {
      outline: 4px auto -webkit-focus-ring-color;
  }
  
  /* form */
  
  .form {
      width: 90vw;
      max-width: var(--fixed-width);
      background: var(--white);
      border-radius: var(--borderRadius);
      box-shadow: var(--shadow-2);
      padding: 2rem 2.5rem;
      margin: 3rem auto;
  }
  
  .form-label {
      display: block;
      font-size: var(--small-text);
      margin-bottom: 0.5rem;
      text-transform: capitalize;
      letter-spacing: var(--letterSpacing);
  }
  
  .form-input,
  .form-textarea {
      width: 100%;
      padding: 0.375rem 0.75rem;
      border-radius: var(--borderRadius);
      background: var(--backgroundColor);
      border: 1px solid var(--grey-200);
  }
  
  .form-row {
      margin-bottom: 1rem;
  }
  
  .form-textarea {
      height: 7rem;
  }
  
  ::placeholder {
      font-family: inherit;
      color: var(--grey-400);
  }
  
  .form-alert {
      color: var(--red-dark);
      letter-spacing: var(--letterSpacing);
      text-transform: capitalize;
  }
  
  /* extra styles */
  .form .form-label {
      text-align: left;
  }
  
  .form .btn-block {
      margin-top: 0.5rem;
  }
  
  /* buttons */
  
  .btn {
      cursor: pointer;
      color: var(--white);
      background: var(--primary-500);
      border: transparent;
      border-radius: var(--borderRadius);
      letter-spacing: var(--letterSpacing);
      padding: 0.375rem 0.75rem;
      box-shadow: var(--shadow-1);
      transition: var(--transition);
      text-transform: capitalize;
      display: inline-block;
  }
  
  .btn:hover {
      background: var(--primary-700);
      box-shadow: var(--shadow-3);
  }
  
  .btn-hipster {
      color: var(--primary-500);
      background: var(--primary-200);
  }
  
  .btn-hipster:hover {
      color: var(--primary-200);
      background: var(--primary-700);
  }
  
  .btn-block {
      width: 100%;
  }
  ```

  ![image](https://github.com/user-attachments/assets/373c3761-2fb6-41d4-9322-5ac3f711071b)

</details>

<details>
  <summary>React Forms - Checkbox and Select Inputs </summary>

  ### Checkbox and Select Inputs

  ##### App.jsx:
  
  ```jsx
  import { useState } from "react";
  import "./App.css";
  
  function App() {
    return (
      <>
        <SelectInputs />
      </>
    );
  }
  
  export default App;
  
  const myFrameworks = ["react", "vue", "angular", "svelte", "next"];
  
  const SelectInputs = () => {
    const [shipping, setShipping] = useState(false);
    const [framework, setFramework] = useState("react");
  
    const handleCheckbox = (e) => {
      setShipping(e.target.checked);
    };
  
    const handleSelect = (e) => {
      setFramework(e.target.value);
    };
  
    return (
      <div>
        <form className="form">
          <h1>Checkbox and Select Inputs</h1>
          <div
            className="form-row"
            style={{ textAlign: "left", marginBottom: "10px" }}
          >
            <label htmlFor="shipping" className="form-label-x">
              Free Shipping
            </label>
            <input
              type="checkbox"
              id="shipping"
              name="shipping"
              className="form-input-x"
              checked={shipping}
              onChange={handleCheckbox}
            />
          </div>
  
          <div className="form-row">
            <label htmlFor="name" className="form-label">
              Select
            </label>
            <select
              name="select"
              id="select"
              className="form-input"
              value={framework}
              onChange={handleSelect}
            >
              {myFrameworks.map((framework) => (
                <option value={framework} key={framework}>
                  {framework}
                </option>
              ))}
            </select>
          </div>
          <button type="submit" className="btn btn-block">
            submit
          </button>
        </form>
  
        <section className="info">
          <h3>Info</h3>
          <h4 style={{ color: shipping ? "green" : "red" }}>
            Shipping Status: {shipping ? "FREE" : "PAID"}
          </h4>
          <h4>Selected Framework: {framework.toUpperCase()}</h4>
        </section>
      </div>
    );
  };
  ```

  ![image](https://github.com/user-attachments/assets/480da1c3-49d3-4468-a37d-933d2a732ce1)

</details>

<details>
  <summary>React Forms - Submitting Form Data with Uncontrolled Inputs (FormData API) </summary>

  ### Submitting Form Data with uncontrolled Inputs (FormData API)

  ##### App.jsx:
  
  ```jsx

  ```

  ##### App.css:
  
  ```css

  ```

</details>

















<details>
  <summary>React Forms - C </summary>

  ### A

  ##### App.jsx:
  
  ```jsx

  ```

  ##### App.css:
  
  ```css

  ```

</details>









<hr>




