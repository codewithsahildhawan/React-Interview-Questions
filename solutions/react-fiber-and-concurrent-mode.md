# React Fiber & Concurrent Mode

## Explanation
React Fiber is the new reconciliation engine in React 16+, enabling features like Concurrent Mode for interruptible rendering and improved responsiveness.

## Syntax
```jsx
// Concurrent Mode (experimental)
import { createRoot } from 'react-dom/client';
createRoot(container).render(<App />);
```

## Example
```jsx
import React from 'react';
import { createRoot } from 'react-dom/client';

function App() {
  return <h1>Hello, Concurrent Mode!</h1>;
}

const container = document.getElementById('root');
createRoot(container).render(<App />);
``` 