# Render props vs HOCs

## Explanation
Render props and HOCs are patterns for code reuse. Render props pass a function as a prop to control rendering. HOCs wrap a component to add behavior.

## Syntax
```jsx
// Render props
<Component render={data => <Child data={data} />} />
// HOC
const Enhanced = withFeature(Component);
```

## Example
```jsx
import React from 'react';

// Render props
function DataProvider({ render }) {
  const data = 'Hello';
  return render(data);
}
function App() {
  return <DataProvider render={data => <div>{data}</div>} />;
}

// HOC
function withLogger(Wrapped) {
  return function Logger(props) {
    console.log('Props:', props);
    return <Wrapped {...props} />;
  };
}
const Hello = props => <h1>Hello, {props.name}</h1>;
const HelloWithLogger = withLogger(Hello);
``` 