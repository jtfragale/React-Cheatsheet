What is ReactJS?  
  *JS library used to create UI & view for front-end web apps  
  *will work with any back-end language  
  
FIRST Components  
  *Focused: should do one thing well  
  *Independent: shouldn't rely on other components  
  *Resuable: should reduce duplicating code  
  *Small: short and condensed  
  *Testable: same input should always produce same output  
  

Create-react-app  
  *creates new folder in current directory  
  *writes out build dependencies  
  *allows import of CSS, gives dev server to run, and hot reloading  
  *uses Webpack which includes Babel, Autoprefixer for CSS, Jest for testing, and ESLint  
```  
$ npm i -g create-react-app
$ create-react-app <put app name here>
$ cd <app name>
$ code .
$ npm run start
```  
Components:  
  *functional elements that take in data and produce UI  
  *every component has a render method, which generate Virtual DOM  
