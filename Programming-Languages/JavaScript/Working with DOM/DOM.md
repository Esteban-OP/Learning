# What is the DOM?

DOM stands for Document Object Model and let's you interact with HTML documents. With the DOM we can add, modify or delete elements on a web page.

In the DOM, an HTML document is represented as a tree of nodes. Each element node represents an HTML element from the HTML document.

So let's take a look at this example:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Example</title>
  </head>
  <body>
    <h1>Title</h1>
    <h2>Sub-title</h2>
  </body>
</html>
```

This will be the basic DOM structure:

```text
Document  // this is the root node in the DOM hierarchy.
========

HTML // and this is the only child node.
-----

- Head
  - Title
- Body
  - H1
  - H2   
```

We can access these elements with JS methods like `getElementById()`, `querySelector()`, `getElementsByClassName()` and `querySelectorAll()`. This methods are web APIs because they provide standardized ways to interact with the DOM using JS.

## getElementById()

With this method we can get an object that represents the HTML element with the specified `id`.

**Example**

JS
```javascript
const container = document.getElementById("container");
```
HTML
```html
<div id="container">
  <h1>Hello, World!</h1>
  <p>Welcome to learning about the DOM.</p>
</div>
<script src="index.js"></script>
```

## querySelector()

**querySelector()** is broader than getElementById(). With querySelector() we can get the first element in the HTML document that matches the CSS selector passed as argument.

**Example**

JS
```javascript
const sectionEl = document.querySelector("section");
```
HTML
```html
<section>
  <h2>Section Title</h2>
  <p>This is a section of the webpage.</p>
</section>
<script src="index.js"></script>  
```