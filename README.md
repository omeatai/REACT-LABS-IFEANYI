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
  <summary>Project - Booklist - Create Structure</summary>

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
  <summary>Project - Booklist - Add Image, Title and Author from Amazon</summary>

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
  <summary>Project - Booklist - Add CSS Styling with Grid</summary>

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
  <summary>Project - Booklist - Local images in Public Folder (Less Performant)</summary>

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
  <summary>Project - Booklist - CSS in JSX</summary>

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
  <summary>Project - Booklist - Javascript in JSX</summary>

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
  <summary>Project - Booklist - JSX Props</summary>

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
  <summary>Project - Booklist - Children Props</summary>

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
  <summary>Project - Booklist - Displaying Lists</summary>

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
  <summary>Project - Booklist - Spread Objects as Props</summary>

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
  <summary>Project - Booklist - Form Events Basics</summary>

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
  <summary>Project - Booklist - Component Specificity</summary>

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



































