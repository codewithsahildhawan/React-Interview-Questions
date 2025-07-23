# Which lifecycle hooks in class component are replaced with useEffect in functional components?

## Explanation
The `useEffect` hook can replicate the behavior of several class component lifecycle methods: `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`.

## Syntax
```jsx
// componentDidMount
useEffect(() => { /* ... */ }, []);
// componentDidUpdate
useEffect(() => { /* ... */ }, [deps]);
// componentWillUnmount
useEffect(() => { return () => { /* cleanup */ }; }, []);
```

## Example
```jsx
import React, { useEffect } from 'react';

function Example() {
  useEffect(() => {
    // componentDidMount
    console.log('Mounted');
    return () => {
      // componentWillUnmount
      console.log('Unmounted');
    };
  }, []);

  useEffect(() => {
    // componentDidUpdate
    console.log('Updated');
  });

  return <div>Check the console for logs.</div>;
}
``` 