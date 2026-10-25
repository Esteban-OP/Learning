# What is REACT?

React is one of the most popular libraries for building user interfaces and web applications. 

A fundamental concept in React is the cration of reusable  UI components like buttons, cards, and avatars. and you can nest these components inside each other to build more complex, dynamic interfaces.

Unlike traditional JS, wich requires direct manipulation of the DOM, React uses a virtual DOM.

## What are Components in React?

Components are the building blocks of React applications that allow developers to break down complex user interfaces into smaller, manageable pieces, making it easier to develop and maintain large-scale applications.

The two types of components in React are functional and class-based components. In modern React, developers use functional components.

We can think of components like JS functions that returns elements describing the UI. The UI is describing using JSX, a syntax extension for JS that looks similar to HTML.

### Example

```javascript
function Greeting() {
  const name = "John";
  return (
    <h1 className="title">
      {/* The result will be Hello John */}
      {/*A comment inside JSX has to be wrapped in curly braces.*/}
      Hello {name}
    </h1>
  );
}
```

We defined a component called `Greeting`.  The curly braces `{}` inside the `h1` tags enable us to embed JavaScript expressions, allowing us to access the name variable within the `h1` element.

> [!NOTE]
> React treats components with a capital letter as custom components, while elements with lowercase letters are consider built-in HTML elements.

We are also applying a class called `title` to the h1 element using the `className` attribute.

But why are we using className instead of class like with regular HTML elements?

This is because in JavaScript, class is a reserved keyword. So, we need to use className instead.

## Using a Component

To use this Greeting component in our application, we would write something like this:
```javascript
<Greeting />
```
When working with JSX, all tags and uses of components need to be explicitly closed.

> [!NOTE]
> If the component or tag doesn't have any children you need to explicitly close it.

## Rendering multiple components

Let's analyze the following code:

```javascript
function Greeting() {
  const name = "John";
  // This will throw an error
  return (
    <h1>Hello {name}</h1>
    <p>Nice to meet you.</p>
  );
}
```
This code will throw an error like this: `Adjacent JSX elements must be wrapped in an enclosing tag.`

The reason why we getting this error is because multiple sibling elements need to be wrapped in a parent element.

### React fragments

React fragments are used group elements together. The correct code is:

```javascript
import { Fragment } from "react";

function Greeting() {
  const name = "John";
  return (
    <Fragment>
      <h1>Hello {name}</h1>
      <p>Nice to meet you.</p>
    </Fragment>
  );
}
```
Or we can just use the `<> ... </>` empty JSX tags which can serve as shorthand for fragments
