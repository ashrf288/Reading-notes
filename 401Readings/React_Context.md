

# Create a Next.js App

1- Create a Next.js app

`npx create-next-app nextjs-blog --use-npm --example `



2- Run the development server
You now have a new directory called nextjs-blog. Let’s cd into it:

`cd nextjs-blog`
Then, run the following command:

`npm run dev`


3- editing the starter page.

+ Make sure the Next.js development server is still running.
+ Open pages/index.js with your text editor.
+ Find the text that says “Welcome to” under the <h1> tag and change it to “Learn”.
+ Save the file.




## React Context

React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

In other words, React context allows us to share data (state) across our components more easily.


## When should you use React context

These types of data include:

Theme data (like dark or light mode)
User data (the currently authenticated user)
Location-specific data (like user language or locale)



## What problems does React context solve

Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.

Here is an example of props drilling. In this application, we have access to theme data that we want to pass as a prop to all of our app's components.

As you can see, however, the direct children of App, such as Header, also have to pass the theme data down using props.


## How do I use React context?

There are four steps to using React context:

+ Create context using the createContext method.
+ Take your created context and wrap the context provider around your component tree.
+ Put any value you like on your context provider using the value prop.
+ Read that value within any component by using the context consumer.


## What is the useContext hook?

Another way of consuming context became available in React 16.8 with the arrival of React hooks. We can now consume context with the useContext hook.

Instead of using render props, we can pass the entire context object to React.useContext() to consume context at the top of our component.


## Does React context replace Redux?

Yes and no.

For many React beginners, Redux is a way of more easily passing around data. This is because Redux comes with React context itself.

However, if you are not also updating state, but merely passing it down your component tree, you do not need a global state management library like Redux.


## React context caveats

Why it is not possible to update the value that React context passes down?

While it is possible to combine React context with a hook like useReducer and create a makeshift state management library without any third-party library, it is generally not recommended for performance reasons.

The issue with this approach lies in the way that React context triggers a re-render.

If you are passing down an object on your React context provider and any property on it updates, what happens? Any component which consumes that context will re-render.

