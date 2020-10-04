# React 1


## ES6 Syntax and Feature Overview


* ECMAScript 2015, also known as ES6, introduced many changes to JavaScript.    
* Here is a key of most identifier names used throughout this reference.

    - Variable: **x**
    - Object: **obj**
    - Array: **arr**
    - Function: **func**
    - Parameter, method: **a**, **b**, **c**
    - String: **str**

* Arrow functions

    The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own **this**, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

    ES5

    ```
    function func(a, b, c) {} // function declaration
    var func = function (a, b, c) {} // function expression

    ```

    ES6

    ```
    let func = (a) => {} // parentheses optional with one parameter
    let func = (a, b, c) => {} // parentheses required with multiple parameters

    ```

[For more information on ES6](https://www.taniarascia.com/es6-syntax-and-feature-overview/)


## React - Hello World

The smallest React example looks like this:

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);

```
[For more information](https://reactjs.org/docs/hello-world.html)


## Introducing JSX

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.

### Why JSX?

    React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

    Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

    React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.


## Rendering Elements

Let’s say there is a <div> somewhere in your HTML file:

`<div id="root"></div>`

We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element into a root DOM node, pass both to ReactDOM.render():

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

## Updating the Rendered Element

React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().

Consider this ticking clock example:

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```

## Components and Props

The simplest way to define a component is to write a JavaScript function:

```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

## Handling Events

Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

* HTML: 

```
<button onclick="activateLasers()">
  Activate Lasers
</button>
```
* is slightly different in React:

```

<button onClick={activateLasers}>
  Activate Lasers
</button>
```



[For more information](https://reactjs.org/docs/handling-events.html)
