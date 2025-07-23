# How to call a method when component is rendered for the first time in React?

## Explanation
Use the `useEffect` hook with an empty dependency array to call a method only once when the component mounts.

## Syntax
```jsx
useEffect(() => {
  // code to run on mount
}, []);
```

## Example
```jsx
import React, { useEffect } from 'react';

function OnMount() {
  useEffect(() => {
    alert('Component mounted!');
  }, []);
  return <div>Check the alert on mount.</div>;
} 