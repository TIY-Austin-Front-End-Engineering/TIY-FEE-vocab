# TIY-summer-review

## HTML
* Doctype ( interview question: what does doctype declaration do )
* Meta tags
* Anatomy of an HTML tag

      ```html
      <tagname attributeName="value"></closingtag>
      <selfClosingTag />
      <!-- comment Write a bunch of stuff here-->
      ```
* Linking to external stylesheets
* Linking to external javascript files
* Forms and form accessibility - `for` attribute should match `id`. all inputs should have a `name` attribute.
* Data attribute - Use to store extra data about a particular element. Access that data with Javascript.

## CSS
* Anatomy of a CSS ruleset

      ```css
      selector {
        property: value
      }
      ```
* Specificity ( interview question: order elements from most to least specific )
* Block vs inline elements ( interview question: describe the difference, give examples )
* Box model - content, padding, border, margin
* Float vs `display: inline-block` vs Flexbox vs CSS Grid Layout (interview questions: describe block formatting, clearing methods)
* Collapsing margins
* Units of measurement - px, percent, em, rem, vh, vw
* Pseudo elements and pseudo classes (interview question: describe pseudo elements and pseudo classes. what is the difference?)
* Positioning - static, relative, absolute, fixed, sticky
* CSS resets (interview question: what is a reset, give examples)
* Media queries

      ```css
      @media media-type and (parameters) {
        selector {
          property: value;
        }
      }
      ```
* Transitions - There are four transition properties:
    * `transition-property` - the property that will transition, e.g. `background`
    * `transition-duration` - the duration of the transition in seconds, e.g. `2s`
    * `transition-timing-function` - defines a function that describes how the transition will proceed over its duration, for example starting slowly and speeding up toward the end of the transition. Values include `ease`, `linear`, `ease-in`, `ease-out`, `ease-in-out`, `step-start`, and `step-end`
    * `transition-delay` - the amount of time, in seconds, that should pass before the animation begins
* Animations - use keyframes and subproperties to animate elements

## Sass
* Partials - separate Sass files into components, import partials into main sass file using `@import 'partialName'`. Note: when naming partials, use an underscore, e.g. `_variables.scss` as the first character, but import without the underscore.
* Nesting - child elements that inherit properties from a parent can be nested inside the parent's ruleset. You can also nest pseudo selectors.

      ```sass
      .dropdown-menu {
        a {
          text-decoration: none;
            &:hover {
              text-decoration: underline;
            }
          }
        }
      ```
* Variables - Used to store repeated values. Denote with $, e.g. `$main-text-color: #8a8a8a`
* Mixins - Used to store repeated rule sets

      ```sass
      @mixin imageBox {
        height: 200px;
        width: 200px;
        border: 10px solid white;
        box-shadow: 0px 0px 5px 0px rgba(0,0,0,0.25);
      } 
      ```
* Bourbon - Sass mixin library
* Neat - Sass grid system built with Bourbon mixins

## Web Design Practices
* Pixel perfect
* Responsive vs adaptive design

## Command Line
* Beginner command line syntax - `cd`, `..`, `pwd`, `ls`, `mkdir`, `touch`, `cp`, `rm`, `clear`, `mv`, `clear`, `tree`, flags (`-rf`, `-a`, `-s`, etc)

## Git
* Beginner Git syntax - `init`, `remote`, `status`, `add`, `commit` (`-m`), `push`
* Branching - Create new branches for each feature of your project. Branch commands: 
	* Create new branch and check that branch out: `git checkout -b <branch name>`
	* Check out exising branch: `git checkout <branch name>`* List all branches: `git branch`
	* Rename the current branch: `git branch -m <new branch name>`
	* Push branch to github: `git push origin <branch name>`
* Pull requests and merging in GitHub
* After merging branches in your remote, pull changes to local repo: `git pull origin master` or `git pull origin` to pull changes while on a feature branch
* Cloning - save a copy of a repository to your computer: `git clone <remote repo path> <local folder>`

## JavaScript
* Data types (interview question: explain the difference between `null` and `undefined`)
* Type coercion
* Accessing the DOM with vanilla javascript: `document.querySelector()`, `document.querySelectorAll()`, `document.getElementByID()`, `document.getElementByClassName()`
* Vanilla javascript event listeners: `element.addEventListener('nameOfEvent', functionToRun)`
* Hoisting
* `location.hash`
* Array looping methods - `forEach()`, `map()`, `filter()`, `reduce()`
* Constructors - functions that are used to create objects
* Prototypes - an object that other objects can look up methods on
* `this` keyword (interview question: explain how `this` works in JavaScript
* Scoping and closures 
* ES2015 (aka ES6) and ES Next - New and future versions of EcmaScript, the language specification JavaScript follows.
	* Other implementations of EcmaScript include ActionScript, SpiderMonkey, and JScript. [See full list of implementations](https://en.wikipedia.org/wiki/List_of_ECMAScript_engines).
	* ES Next - [ES2016](https://tc39.github.io/ecma262/2016/), ES2017, and beyond
	* [Babel](https://babeljs.io/) - ES2015 features aren't always compatible. Babel compiles newer syntax down to ES5
* Recursive functions - also known as self-invoking functions. Typically used when you need to call the same function repeatedly with different parameters from within a loop.
* Promises - allow chaining of asychronous code using `.then` syntax
	* jQuery's ajax requests are promises, so you can use .then syntax instead of the 'success' callback syntax
	* You can also write your own promise functions, e.g.

	```javascript
	  function wait5secs() {
  	    const promise = new Promise((resolve, reject) => {
    	      // do promisey stuff here
  	    });
  	    return promise;
	  }
	  ```

	* A promise constructor always takes a single callback function as its only argument. 
	* That callback will take 2 functions as its arguments: the first should be called when the conditions of the promise are successfully resolved; the second should be called when the conditions of the promise have failed
* Object Destructuring - a way of extracting data stored in objects or arrays
	* if an existing variable name matches the name of a property you wish to create on an object, you can use this alternative syntax:

	```javascript
	// instead of
	let myObj = {name: "jess"}
	// you can use
	let name = "jess";
	let myObj = {name}
	```

	* You can also do the reverse and get a variable name from an object

	```javascript
	var object = {name: 'jess'};
	var {name} = object;
	```

## jQuery
* getters and setters
* `.append(elementOrString)` and `.prepend(elementOrString)`
* event listening with `.on()`
* `.attr()` method - used to access or change attributes in HTML elements

## AJAX (asynchonous javascript and xml)
* used to make CRUD apps (four verbs: create, read, update, destroy)
* HTTP verbs - POST, GET, PUT, DELETE
* jQuery AJAX - `$.ajax(settings)` where `settings` is an object that configures the ajax request
* API - application interface
* JSON - JavaScript Object Notation
* CORS (Cross-Origin Resource Sharing) - Allows you to make requests to a different origin from your own. If the API you're trying to access doesn't allow CORS, use `dataType: jsonp` in your settings object.
* REST - representation state transfer
* Server errors - 200 (it worked), 300 (no change), 400 (your request is bad), 500 (something wrong on the server)
 
## Build Tools
* Popular build tools - Gulp, Grunt, Broccoli, Webpack, NPM scripts
* install dependencies with `npm install --save <dependency name>`
* Install dev dependencies with `npm install --save-dev <dependency name>`

## Single Page Applications
* All content lives on a single HTML page, which we manipulate to show different data and elements using javascript and css
* Plan ahead - wireframes, html/css mocks, data structures
* Data modeling - make a model for each discrete types of data in the application
* AJAX to get and set data
* Routers - keeps track of which route or page a user wants to see
* Data Store - single source of truth that keeps track of all application state. Should contain instances of any needed models/collections. Should also contain state information such as fetching from server or pagination data.

## Backbone and Underscore
* Underscore is a functional utility library that makes manipulation of data sooo much easier
* Backbone is a javascript framework used to build SPAs
      * Often referred to as an MVC (model-view-controller). More accurately an MV* because Backbone doesn't have controllers.
      * Models - contain application data and the logic surrounding it
      * Collections - ordered sets of models
      * Views - listen for events, react to those events, render data to the DOM
      * Router - create router object with keys as URL path and value as the function to call when you go to that route

## React
* Setting up React environment
      * start new project using spa-scaffold, webpack, or some other build tool 
      * install dependencies: `npm install --save react react-dom react-router`
      * Install dev dependencies: `npm install --save-dev babel-preset-react`
      * Add react compiler preset:

```json
	      "babel": {
	        "sourceType": "module", 
	        "presets": [
	          "es2015",
	          "react"
	        ]
	      }
```
      * setup `.jshintrc` file `json { "esversion": 6, "esnext": true }`
* Getting a project started
      * Plan project, breaking up pages and page elements into modules. Each module is a react component created with a constructor: `React.createClass()`
      * Every react component needs a render function that must return JSX
      * Add component to the DOM with the `ReactDOM.render()` function, which takes 2 arguments: the react element to render, and the DOM element into which to render it
* Using React Router
      * Import named components (as opposed to components exported as defaults) from react router, e.g. `import { Router, Route, hashHisotry } from 'react-router';` 
      * Parameterized routes - Use a `:` in your route to denote the part that changes, e.g. `<Route path=":postId" component={BlogPost} />`
      * Links - React Router has a built in `Link` component that can be imported and used anywhere in the application. Link components work just like anchor tags but use a `to` attribute instead of `href`.
      * Programmatic navigation - Use the .push() method to add path to route history, e.g. `hashHistory.push('/posts/12345')`
      * `this.props.children` Anything placed between the opening and closing tags of a component that is NOT self-closing is passed into them as `this.props.children`
* Props and state
      * `this.state` is for any data that may change over time, or that cannot be gathered/figured out from any other source
      * `this.props` is for any data that can be passed in from a parent component and can only change by the parent passing in a new value
* Component lifecycle
      1. `getInitialState()` - Set to whatever state is before component is mounted. Return value is initial value of `this.state`.
      2. `componentWillMount()` - Invoked before the first render occurs. Can force a render by setting state with `setState`.
      3. `render()` - renders the component. Render happens after will mount but before did mount. Other renders happen when props or state change
      4. `componentDidMount()` - Use this to initiate any fetching, and listening, since we know we're going ahead with rendering.
      5. `componentWillUnmount` - Happens right before a component is removed from the DOM for cleaning up any ongoing code listeners, setIntervals, etc. Use to prevent zombies.
* React Transitions - for simple hover effects, just give elements a `className` and add transitions in CSS. For animations on click events or DOM rendering, use react's animation library.
	* install animation library as a dependency `npm install --save react-addons-css-transition-group`
	* build animation by importing library, create an instance of it in our render function of a component, and
wrap the instance around any elements that we want to have a transition. 
	* Transition components require 3 props: `transitionName`, `transitionEnterTimeout`, `transitionLeaveTimeout`
	* Transition children require a key prop

## Back End as a Service
* Back end
      * persist data
      * manipulate data before or after saving/retrieving from db
      * send emails
      * protect access to data
      * run scheduled code
* Authentication
      * cookie based auth
      * token based auth
      * oauth
      * custom authorization
* Examples of BaaS - firebase, backendless, parse, Kinvey

## Unit Testing
* Unit testing is for individual building blogs of an application. Test a specific component to ensure it renders properly or a specific model to ensure correct functionality
* Testing dependencies - mocha, chai, enzyme
* Write one test file for each module. Test anything you'd check with `console.log()`.
* Write tests for custom logic on models and when a component should render differently based on props or state

## Agile Methodology
* Standups
* Scrums
* Stories - user, developer, bug

## Useful Tools
* [caniuse.com](http://caniuse.com)
* [Pixel perfect chrome extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)
* [Responsive web design checklist](http://rwdchecklist.com/)
* [List of DOM events](https://developer.mozilla.org/en-US/docs/Web/Events)
* [ES2015 compatiblity table](http://kangax.github.io/compat-table/es6/)
