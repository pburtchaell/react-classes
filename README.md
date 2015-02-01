# react-classes [![Dependency Status](https://david-dm.org/pburtchaell/react-classes.svg)](https://david-dm.org/pburtchaell/react-classes)
[![devDependency Status](https://david-dm.org/alanshaw/pburtchaell/react-classes.svg)](https://david-dm.org/pburtchaell/react-classes)

> A small wrapper for `React.addons.classSet`

## Overview

This module adds additional functionality to [class name manipulation](http://facebook.github.io/react/docs/class-name-manipulation.html) in React by allowing a base class to be specified.

## Example

This component will always be rendered with base class of `.foo` and will have the classes of `.bar` & `.baz` when the expressions are true.

```
render: function() {

  var classes = this.getClass('foo', {
    'bar': this.props.bar === true,
    'baz': this.props.baz === true
  });

  return (
    <div className={classes}></div>
  );

}
```

## Quick Start

Install with npm:

```
npm install react-classes --save
```

Require the module in your project and add it to the React component as a mixin.

```
/** @jsx React.DOM */

var React = require('react');
var classes = require('react-classes');

module.exports = React.CreateClass({

  mixins: [classes],

```

---
Built with care in New Orleans by Patrick Burtchaell.

[Copyright 2014](LICENSE) Patrick Burtchaell. All rights reserved.
