What is ReactJS?  
  -JS library used to create UI & view for front-end web apps  
  -will work with any back-end language  
  
FIRST Components  
  -Focused: should do one thing well  
  -Independent: shouldn't rely on other components  
  -Resuable: should reduce duplicating code  
  -Small: short and condensed  
  -Testable: same input should always produce same output  
  

Create-react-app  
  -creates new folder in current directory  
  -writes out build dependencies  
  -allows import of CSS, gives dev server to run, and hot reloading  
  -uses Webpack which includes Babel, Autoprefixer for CSS, Jest for testing, and ESLint  
```  
$ npm i -g create-react-app
$ create-react-app <put app name here>
$ cd <app name>
$ code .
$ npm run start
```  
Components:  
  -functional elements that take in data and produce UI  
  -every component has a render method, which generate Virtual DOM  

Component Lifecycle:  
 -provide several lifecycle methods used to control application based on state of UI
 -`componentWillUnmount` called immediately before a compent is removed from DOM
 -`componentDidMount` called immediately after a component is rendered to DOM 
 -used for making asynchronous requests, binding event listeners to components, animating components, and optimizing performance
 -two types of component lifecycle methodes
  *mounting
  *updating
  
AXIOS to query API  
  ```
  import axios from 'axios'

   axios.get('url)
    .then((res) => {
     console.log(res)
    })
    .catch((error) => {
     console.log(error)
    })
  ```  

Binding   
 -when using event methods, have to bind `this` to the methods otherwise `this` will be undefined

``` 
constructor (props) {
      super(props)
      this.handleClick = this.handleClick.bind(this)
    }

<button onClick={this.handleClick}/>
```

React Router   
  -mostly commonly used routing library  
  -serves as the root component in a React application & renders other app components wihtin itself depending on path in url
 
```
npm install --save react-router-dom
```

```index.js

import { BrowswerRouter as Router } from "react-router-dom"

ReactDom.render(
  <Router>
    <App />
  <Router>,
  document.getElementById("root")
)
```
Importing other components
  -Link: used for setting URL and provides navigation betweeen different components in app without triggering page refresh. Can also be 
   used inside any component that is connected to a Route
  -Route: connects a certain path in URL with relevant component to render at that location 

```
import { Route, Link } from "react-router-dom"

render() {
  return (
    <div>
      <nav>
        <Link to=""></Link>
      </nav>
      <main>
        <Router path="" render={}/>
      </main>
    </div>
  )
 }
```

Redirect  

```
import { Route, Link, Redirect } from "react-router-dom"

<Route path="/*" render={() => <Redirect to="/search" />} />
```

Switch  
  -used to force React Router to treate routes as unique and only render first matching route  
```
import { Route, Link, Redirect, Switch } from "react-router-dom"
```
  -wrap all Route components in Switch component `<Switch></Switch>`

Two-Server Architecture  
  -need to install CORS (Cross-Origin Resource Sharing) to allow front end to receive data from backend  
```
npm install --save cors
```

```
const cors = require('cors')

app.use(cors())
```


 
   
 
