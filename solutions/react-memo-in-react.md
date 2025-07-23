# What is React.memo() and when should you use it?

## Explanation
`React.memo` is a higher-order component that memoizes a functional component, preventing unnecessary re-renders if props haven't changed.

## Syntax
```jsx
const Memoized = React.memo(Component);
```

## Example
```jsx
import React from 'react';

const MyComponent = React.memo(function MyComponent({ value }) {
  return <div>{value}</div>;
});

function App() {
  return <MyComponent value="Hello" />;
}
``` 