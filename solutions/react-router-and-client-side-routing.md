# React Router & client-side routing

## Explanation
React Router is a library for handling navigation in React apps. It enables client-side routing without full page reloads.

## Syntax
```jsx
import { BrowserRouter, Route, Routes } from 'react-router-dom';
<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
  </Routes>
</BrowserRouter>
```

## Example
```jsx
import React from 'react';
import { BrowserRouter, Route, Routes } from 'react-router-dom';

function Home() { return <h1>Home</h1>; }
function About() { return <h1>About</h1>; }

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </BrowserRouter>
  );
}
``` 