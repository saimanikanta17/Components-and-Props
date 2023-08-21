# Components & Props

- Components
  - Creating a Component
  - Reusable Components
  - Composable Components
- Props
  - Passing Props
  - Accessing Props
- Create React App
  - React Project Setup
  - Starting the Application

# React Components

- component is a reusable part of code

- types

  - Functional Components
  - Class Components

- naming convention -- PascalCase

  - if we provide component name starts with lower case, react consider as HTML elements rather than component as a result an error is raised(unrecognized element)

- props

  - pass information to component
  - similar to declaring attributes for html elements
  - props are taken as arguments it will be object form
  - through object destructuring we access the properties

- composable
  - we can use component inside another component
  - liked nested elements

# Functional Components

- These are JavaScript functions that take props as a parameter if necessary and return JSX element.

```js
const ComponentName = (props) => {
  const { propName1, propName2 } = props;
  return (
    <h1 className="message">
      {propName1} {propName2}
    </h1>
  );
};
<ComponentName propName1="propValue1" propName2="propValue2" />; // void syntax
```

# create-react-app

- it is a third party package
- created by facebook
- to generate react application setup

  > npm install -g create-react-app

  - run above command in terminal
  - its installs create-react-app globally in our environment

    - to create a react application run below command in terminal

      > create-react-app myapp --use-npm

      - navigate to created myapp directory

        > cd myapp

      - to start server

        > npm start

- src folder - all created react components are maintained here and majority of code are written here

  - index.js
    - starting point of application
    - when we run npm start in terminal the index.js file will run and other modules like app.js,app.css,index.css etc are imported
  - app.js
    - code logic are written

- public folder - contains assets like images,icons,videos etc

  - index.html
    - final output
    - everything gets attached to the div element with id "root"

- react uses ES6 modules but extension is .js not .mjs

- pre-configured tools --- stepup made by react
  - live editing -> live reloaded
  - ESLint -> show errors,bugs and syntax errors
  - prettier -> enforces a consistent styles like indentation,spacing,semicolons etc
  - babel -> compiles jsx to js code
  - webpack -> bundling group of modules into single file its shown when we inspect
