# reat router dom

## 1- install 

`npm install react-router-dom`

## 2- import BrowserRouter

  `import { BrowserRouter as Router } from 'react-router-dom';`


If we want to provide routes within our entire application it needs to be wrapped around our entire component tree ( the main component )

```
export default function App() {
  return (
    <Router>
      {/* routes go here, as children */}
    </Router>
  );
}
```

## 3- declare individual routes within our application.


`import { BrowserRouter as Router, Route } from 'react-router-dom';
`


 we need to provide at least two props to each route, `path` and `component`

 ```
  <Router>
      <Route path="/about" component={About} />
    </Router>
 ``` 

 **The path prop specifies on what path of our app a given route is located.**

 **component props are used to display a specific component for our path. or you can use it as a child **

 ```
 <Route path="/about">
        <About />
      </Route>
 ```

 ## 4- if want a component (such as a navbar) to be visible on every page, put it still within the browser router, but above (or below) the declared routes

 ```
 <Router>
      <Navbar />
      <Route path="/" component={Home} />
      <Route path="/about" component={About} />
    </Router>
 ```


 ## 5- make sure that our router matches exactly the path ( using switch)

 `import { BrowserRouter as Router, Switch, Route } from "react-router-dom";`

The switch component should be included within the router


The switch component looks through all of its child routes and it displays the first one whose path matches the current URL.


 ```
 export default function App() {
  return (
    <Router>
      <Navbar />
      <Switch>
        <Route exact path="/" component={Home} />
        <Route path="/about" component={About} />
      </Switch>
    </Router>
  );
}
 ```



 ## 6- Link Component (use it in nav bar) 

 `import { BrowserRouter as Router, Switch, Route, Link } from "react-router-dom";`


 ```
 function Navbar() {
  return (
    <nav>
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
    </nav>
  )
}
 ```



## 7- Redirect Component


 . It accepts the to prop, which specifies where we want the link to navigate our user to


 Whenever we're using something like a private route and we have a condition in which the user is not authenticated, we want to redirect them back to the login page.


`import {
  BrowserRouter as Router,
  Switch,
  Route,
  Redirect
} from "react-router-dom";`


```
 
export default function App() {
  return (
    <Router>
      <Switch>
        <Route exact path="/" component={Home} />
        <PrivateRoute path="/hidden" component={Hidden} />
      </Switch>
    </Router>
  );
}

function PrivateRoute({ component: Component, ...rest }) {
  // useAuth is some custom hook to get the current user's auth state
  const isAuth = useAuth();

  return (
    <Route
      {...rest}
      render={(props) =>
        isAuth ? <Component {...props} /> : <Redirect to="/" />
      }
    />
  );
}



```
