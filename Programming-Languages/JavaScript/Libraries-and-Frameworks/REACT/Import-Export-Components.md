# Import and Export components

An `export` makes a component available to other files. An `import` allows a file to use a component that was exported elsewhere.

## Using Default Exports

If we want to use our component in another file, we need to first export it like this:

`export defaul Component`

We use the `default` keyword because this will be the default export from the module. We can also expport the component on the same line as the component definition like this:

`export default function Component(){...}`

> [!NOTE]
> A file can only have one default export, which makes it ideal for a file that primarily contains a single component.

## Import a Default Export

You can choose to import child components in other parent component files, or import them in the root component file.

Every React project has a top-level component, typically called `App` defined in a file named `App.jsx`. And this file is usually located in the `src` directory of the project.

To use the component inside the root **App** component, we need import it like this:

`import Example from "./Example";`

And now we have the following code:

```javascript
import Example from "./Example";

export default function App() {
  return (
    <Example />
  );
}
```

## Using Named Exports

Named exports allow a file to share multiple components or functions.

Unlike default exports, these must be imported using the exact name they were exported with (unless you rename them using the `as` keyword).

Example:

```javascript
// Animals.jsx
export function Cat() {
  return <h2>Mr. Whiskers</h2>;
}

export function Dog() {
  return <h2>Fido</h2>;
}
```
We use the `export` keyword individually on each component. To use these in another file, we import them using curly braces:

```javascript
import { Cat, Dog } from "./Animals";

export default function App() {
  return (
    <div>
      <Cat />
      <Dog />
    </div>
  );
}
```

We can rename a component during import using the `as` keyword.

```javascript
import { Cat as Kitty } from "./Animals";

export default function App() {
  return <Kitty />;
}
```

## Combining Default and Named Exports

A file can have one default export and multiple named exports.

```javascript
// Animals.jsx
export default function Cat() {
  return <h2>Mr. Whiskers</h2>;
}

export function Dog() {
  return <h2>Fido</h2>;
}
```
When importing mixed exports, the `default export` comes first (**without braces**), followed by the `named exports` (**inside braces**):

```javascript
// App.jsx
import Cat, { Dog } from "./Animals";

export default function App() {
  return (
    <div>
      <Cat />
      <Dog />
    </div>
  );
}
```