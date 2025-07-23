# Create a pure component.

## Explanation
A pure component in React only re-renders if its props or state change. In class components, use `React.PureComponent`. In functional components, use `React.memo`.

## Syntax
```jsx
// Class
class MyComponent extends React.PureComponent { ... }
// Functional
const MyComponent = React.memo(function MyComponent(props) { ... });
```

## Example
```jsx
import React from 'react';

const Pure = React.memo(function Pure({ value }) {
  return <div>{value}</div>;
});

function App() {
  return <Pure value="Hello" />;
}
``` 