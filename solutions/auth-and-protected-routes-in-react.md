# Auth & protected routes

## Explanation
Protected routes restrict access to certain pages based on authentication. Use React Router and conditional rendering to implement them.

## Syntax
```jsx
<Route path="/private" element={isAuth ? <Private /> : <Navigate to="/login" />} />
```

## Example
```jsx
import React from 'react';
import { BrowserRouter, Routes, Route, Navigate } from 'react-router-dom';

function Private() { return <h1>Private</h1>; }
function Login() { return <h1>Login</h1>; }

function App() {
  const isAuth = false; // Replace with real auth logic
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/login" element={<Login />} />
        <Route path="/private" element={isAuth ? <Private /> : <Navigate to="/login" />} />
      </Routes>
    </BrowserRouter>
  );
}
``` 