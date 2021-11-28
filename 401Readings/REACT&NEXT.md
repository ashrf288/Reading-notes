## ES 6

+ Variable declaration

`let x = 0`

+ Constant declaration

`const CONST_IDENTIFIER = 0`

+ Arrow functions

`let func = (a) => {}`

+ Template literals

`let str = Release Date: ${date}`

+ Multi-line strings

```
let str = `This text
            is on
            multiple lines`
```

+ Implicit returns


`let func = (a, b, c) => a + b + c /`


+ Key/property shorthand

```
let obj = {
  a,
  b,
}
```


+ Method definition shorthand

```
let obj = {
  a(c, d) {},
  b(e, f) {},
}
```

+ Destructuring (object matching)

`let {a, b, c} = obj`



+ Array iteration (looping)

```
for (let i of arr) {
  console.log(i)
}
```

+ Promises/Callbacks

Promises represent the completion of an asynchronous function. They can be used as an alternative to chaining functions.

```
let doSecond = () => {
  console.log('Do second.')
}

let doFirst = new Promise((resolve, reject) => {
  setTimeout(() => {
    console.log('Do first.')

    resolve()
  }, 500)
})

doFirst.then(doSecond)
```


## Specifying Children with JSX


```
const element = (
  <div>
    <h1>Hello!</h1>
    <h2>Good to see you here.</h2>
  </div>
);
```


## Updating the Rendered Element
React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().



## Function and Class Components

This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

## Rendering a Component

+ We call ReactDOM.render() with the <Welcome name="Sara" /> element.
React calls the Welcome component with {name: 'Sara'} as the props.
Our Welcome component returns a <h1>Hello, Sara</h1> element as the result.
React DOM efficiently updates the DOM to match <h1>Hello, Sara</h1>.


## Props are Read-Only
Whether you declare a component as a function or a class, it must never modify its own props. Consider this sum function:
```
function sum(a, b) {
  return a + b;
}
```


Such functions are called “pure” because they do not attempt to change their inputs, and always return the same result for the same inputs.

All React components must act like pure functions with respect to their props.

Of course, application UIs are dynamic and change over time. In the next section, we will introduce a new concept of “state”. State allows React components to change their output over time in response to user actions, network responses, and anything else, without violating this rule.



## Converting a Function to a Class

+ Create an ES6 class, with the same name, that extends   React.Component.
+ Add a single empty method to it called render().
+ Move the body of the function into the render() method.
+ Replace props with this.props in the render() body.
+ Delete the remaining empty function declaration.


```
constructor(props) {
    super(props);
    this.state = {date: new Date()};
  }
```


## Adding Lifecycle Methods to a Class
In applications with many components, it’s very important to free up resources taken by the components when they are destroyed.

We want to set up a timer whenever the Clock is rendered to the DOM for the first time. This is called “mounting” in React.

We also want to clear that timer whenever the DOM produced by the Clock is removed. This is called “unmounting” in React.


## Using State Correctly
There are three things you should know about setState().

1- Do Not Modify State Directly
For example, this will not re-render a component:
```
// Wrong
this.state.comment = 'Hello';
Instead, use setState():

// Correct
this.setState({comment: 'Hello'});
The only place where you can assign this.state is the constructor.
```

2- State Updates May Be Asynchronous
React may batch multiple setState() calls into a single update for performance.

Because this.props and this.state may be updated asynchronously, you should not rely on their values for calculating the next state.

For example, this code may fail to update the counter:
```
// Wrong
this.setState({
  counter: this.state.counter + this.props.increment,
});
To fix it, use a second form of setState() that accepts a function rather than an object. That function will receive the previous state as the first argument, and the props at the time the update is applied as the second argument:

// Correct
this.setState((state, props) => ({
  counter: state.counter + props.increment
}));
```

We used an arrow function above, but it also works with regular functions:

3- State Updates are Merged
When you call setState(), React merges the object you provide into the current state.

For example, your state may contain several independent variables:
```
  constructor(props) {
    super(props);
    this.state = {
      posts: [],
      comments: []
    };
  }
Then you can update them independently with separate setState() calls:

  componentDidMount() {
    fetchPosts().then(response => {
      this.setState({
        posts: response.posts
      });
    });

    fetchComments().then(response => {
      this.setState({
        comments: response.comments
      });
    });
  }
```

## Tailwind CSS

important benefits:

+ You aren’t wasting energy inventing class names. No more adding silly class names like sidebar-inner-wrapper just to be able to style something, and no more agonizing over the perfect abstract name for something that’s really just a flex container.

+ Your CSS stops growing. Using a traditional approach, your CSS files get bigger every time you add a new feature. With utilities, everything is reusable so you rarely need to write new CSS.

+ Making changes feels safer. CSS is global and you never know what you’re breaking when you make a change. Classes in your HTML are local, so you can change them without worrying about something else breaking.



## But using utility classes has a few important advantages over inline styles:

+ Designing with constraints. Using inline styles, every value is a magic number. With utilities, you’re choosing styles from a predefined design system, which makes it much easier to build visually consistent UIs.
+ Responsive design. You can’t use media queries in inline styles, but you can use Tailwind’s responsive utilities to build fully responsive interfaces easily.
+ Hover, focus, and other states. Inline styles can’t target states like hover or focus, but Tailwind’s state variants make it easy to style those states with utility classes.



## Next.js: The React Framework


+ Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
+ You need to do production optimizations such as code splitting.
You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
+ You might have to write some server-side code to connect your React app to your data store.

+ An intuitive page-based routing system (with support for dynamic routes)
+ Pre-rendering, both static generation (SSG) and server-side
+  rendering (SSR) are supported on a per-page basis

+ Automatic code splitting for faster page loads
+ Client-side routing with optimized prefetching
+ Built-in CSS and Sass support, and support for any CSS-in-JS library
+ Development environment with Fast Refresh support
+ API routes to build API endpoints with Serverless Functions
Fully extendable
