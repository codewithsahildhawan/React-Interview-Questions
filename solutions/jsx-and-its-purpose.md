# JSX and its purpose

## Explanation
JSX is a syntax extension for JavaScript that looks like HTML. It allows you to write UI code in a declarative way and is compiled to `React.createElement` calls.

## Syntax
```jsx
const element = <h1>Hello, world!</h1>;
```

## Example
```jsx
import React from 'react';

function Hello() {
  return <h1>Hello, world!</h1>;
} 