# Perform type checking using prop-types?

## Explanation
The `prop-types` package allows you to specify the types of props a component should receive. This helps catch bugs and document your components.

## Syntax
```jsx
import PropTypes from 'prop-types';
Component.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number
};
```

## Example
```jsx
import React from 'react';
import PropTypes from 'prop-types';

function User({ name, age }) {
  return <div>{name} ({age})</div>;
}

User.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number
};
``` 