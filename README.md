# robofriends

Tutorial for React - Junior to Senior Web Developer Roadmap
To run the project:

1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. Update CRA: go to Json package, scripts and change the react script version to new version, run npm install

- npm audit //Will show vulnerabilities
- npm update will update dependencies to newer versions
- npm audit fix--force //This will force any new updates

### Font

- Search for desired font. In this SEGA LOGO FONT was used. Get it from [CufOnFonts](http://www.cufonfonts.com)
- Import it in App.css
- Drop the SEGA.wooff file in project file

### API

- [jsonplaceholder ](https://jsonplaceholder.typicode.com/) is a free fake API for testing and prototyping powered by JSON Server + LowDB

### CSS

[Tachyons CSS Toolkit](https://tachyons.io/) - Tachyons is a CSS framework, but unlike other well-known frameworks like Foundation and Bootstrap, it doesn't come with pre-built UI components. Instead it aims to break down CSS rules into as small and reusable parts as possible.

- Install Tachyons with npm and import it in index.js

### Class components lifecyle

#### Mounting methods are called when an instance of component is being created and inserted into the DOM

- constructor()
- componentWillMount()
- render()
  componentDidMount()

#### Updating methods. an update canb e caused by changes to props or state. These methos are called when a component is being re-rendered:

- componentWillReceiveProps()
- shouldComponentUpdate()
- componentWillUpdate()
- render()
- componentDidUpdate()

#### Error handling

- ErrorBoundry component will wrap the card list component. If something goes wrong it will show an error message. This will work only on production.

```
class ErrorBoundry extends Component {
  constructor(props) {
    super(props);
    this.state = {
      hasError: false,
    };
  }
  componentDidCatch(error, info) {
    this.setState({ hasError: true });
  }
  render() {
    if (this.state.hasError) {
      return <h1>Oops... There was an error</h1>;
    }
    return this.props.children;
  }
}
export default ErrorBoundry;
```

#### Deployment

- [CRA deployemnt](https://create-react-app.dev/docs/deployment/#github-pages-https-pagesgithubcom) instruction for github pages CL deployment
- [Page deployed](https://sandracoburn.github.io/robofriends/) with GitHub pages

#### State Management

- React hooks
  - Redux 3 principles
  - Single source of truth
  - State is read only - immutable
  - Changes using pure functions
- Redux Flux Pattern:
  - Action -> Dispatcher -> Store -> View
- MVC Pattern
  - Action -> Controller -> Model -> View
    To install:

```
npm install redux
npm install react-redux
```

#### Popular Tools for React + Redux

Utility Libraries:

- [Ramda](https://ramdajs.com/) library designed specifically for a functional programming style. It's easy to create functional pipelines that doesn't mutate user data.
- [Lodash](https://github.com/lodash/lodash) - makes JavaScript easier by taking the hassle out of working with arrays, numbers, objects, strings, etc Lodash's modular methods are great for:
  - Iterating arrays, objects, & strings
  - Manipulating & testing values
  - Creating composite funcitons
- [Glamorous](https://glamorous.rocks/) - Maintainable CSS with React
- [Styled Components](https://styled-components.com/docs/basics) utilises tagged template literals to style your components
- [CSS Modules](https://github.com/css-modules/css-modules) are CSS files in which all class names and animation names are scoped locally by default. CSS Modules compile to a low-level interchange format called ICSS or Interoperable CSS, but are written like normal CSS files.
- [Gatsby](https://www.gatsbyjs.com/) allows developers to quickly ftch and render content from nearly any content or data source. Gatsby brings React's component model to websites. Declarative UI makes your code easier to debug and helps your team move faster. Plus, you can wite in modern Javascript or SCSS/LESS without the hassle of setting up an asset pipeline.
- [Next.js](https://nextjs.org/) - The React Framework for production. Next.js gives you the best developer experience with all the features you need for production: hybrid static & server rendering, TypeScript support, small boundling, route pre-fetching, and more. No config needed.
- [Material UI](https://material-ui.com/) - React components for faster and easier web development.
- [Reselect](https://github.com/reduxjs/reselect) - Simple "selector" library for Redux(and others) inspired by getters in NuclearJS, subscriptions in re-frame and this proposal from speedsaker.
  - Selectors can compute derived data, allowing Redux to store the minimal possible state.
  - Selectors are efficient. A selector is not recomputed unless of ot its arguments changes.
  - Selectors are composable. They can be used as input to other selectors.
- [Redux-Sage](https://redux-saga.js.org/) - Handles asynchronous actions in Redux for bigger apps.
- [Immutable.JS](https://immutable-js.github.io/immutable-js/) is a library to make sure your state remains immutable. Immutable collections for JavaScript.

#### Module Bundlers

- [Webpack](https://webpack.js.org/) is a static module bundler. It's main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packagging. When webpack processes your application, it internally builds a dependency graph which maps every module your project needs and genertes one or more bundles.
- [Parcel](https://parceljs.org/) is a fast, zero configuratin web application bundler. It has out of the box support for JS, CSS, HTML, file assets, and more - no plugins needed.
- [Rollup.js](https://rollupjs.org/guide/en/) is a module bundler for JavaScript which compiles small pieces of code into something larger and more complex, such as a library or application.

### PWA - Progressive Web App

- A progressive web application is a type of application software delivered through the web, built using common web technologies including HTML, CSS and JavaScript. It is intended to work on any platform that uses a standards-compliant browser, including both desktop and mobile devices
- PWAs can: Work offline or in poor network conditions, be installed on the user's device and accessed via a home screen icon like a native app.
