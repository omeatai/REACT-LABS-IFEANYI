# REACT-LABS-IFEANYI
by Ifeanyi Omeata

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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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

  ##### App.jsx:
  
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
  <summary>React Hooks - Setup </summary>

  ### A

  ##### App.jsx:
  
  ```jsx

  ```

</details>














