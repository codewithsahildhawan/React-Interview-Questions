# Event handling

## Explanation
React handles events using camelCase syntax and passes event handlers as functions. The event object is synthetic and works similarly to native DOM events.

## Syntax
```jsx
<button onClick={handleClick}>Click me</button>
```

## Example
```jsx
import React from 'react';

function Clicker() {
  const handleClick = () => alert('Clicked!');
  return <button onClick={handleClick}>Click me</button>;
} 