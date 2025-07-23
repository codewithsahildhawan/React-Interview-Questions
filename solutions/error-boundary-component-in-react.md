# Create an error boundary component in React.

## Explanation
Error boundaries are React class components that catch JavaScript errors in their child component tree and display a fallback UI.

## Syntax
```jsx
class ErrorBoundary extends React.Component {
  componentDidCatch(error, info) { /* ... */ }
  render() { /* ... */ }
}
```

## Example
```jsx
import React from 'react';

class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }
  static getDerivedStateFromError() {
    return { hasError: true };
  }
  componentDidCatch(error, info) {
    // log error
  }
  render() {
    if (this.state.hasError) return <h1>Something went wrong.</h1>;
    return this.props.children;
  }
}

function BuggyComponent() {
  throw new Error('Crash!');
}

function App() {
  return (
    <ErrorBoundary>
      <BuggyComponent />
    </ErrorBoundary>
  );
} 