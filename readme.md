# react-suitcss-mixin

A React component mixin to generate CSS class names that conform to [SUIT CSS naming conventions](https://github.com/suitcss/suit/blob/master/doc/naming-conventions.md).

This mixin provides several primary functions.

1. Provide a general purpose `getClassName` method that accepts a variety of options for generating SUIT CSS conformant class names.  This method accepts an optional parameter that may contain any of the following options.
  * __namespace__ - Defaults to component's `namespace` property
  * __componentName__ - Defaults to component's `displayName` property
  * __descendantName__
  * __modifiers__
  * __states__
  * __utilities__ - Defaults to values from `this.props.utilities`
2. Allow generic utility classes to be passed in from a utilities prop.
3. Allow arbitrary CSS class names to be added using the standard React className prop.

## Installation

```
npm install react-suitcss-mixin
```

## Basic Usage

```JavaScript
var React = require('react');
var SuitCss = require('react-suitcss-mixin');

var MyComponent = React.createClass({
  mixins: [SuitCss],

  render: function() {
    return <div className={ this.getClassName() }></div>
  }
});

React.render(<MyComponent/>, document.body);
```

Renders as:

```html
<div class="MyComponent"></div>
```

## Advanced Usage

Browse the [demo files](https://github.com/brentertz/react-suitcss-mixin/blob/master/demo) or just run the demo.

```
npm run demo
```

## Build

```
npm run build
```

## Tests

```
npm test
```

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code.

## Release History

* 1.0.1 - Update dependencies. Fix test mock. Update readme.
* 1.0.0 - Camelize and capitalize componentName
* 0.0.5 - Use Object.assign polyfill from react/lib. Update .npmignore and readme.
* 0.0.4 - Initial release
