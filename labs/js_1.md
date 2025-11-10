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
  <summary>JS</summary>

### projects-v1/app_js/sample_1/index.html

```html

```

### projects-v1/app_js/sample_1/app.js

```js

```

</details>






