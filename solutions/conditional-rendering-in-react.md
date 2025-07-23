# How to conditionally render an element or text in React?

## Explanation
Conditional rendering in React can be done using JavaScript logical operators (&&, ?:, if-else) inside JSX.

## Syntax
```jsx
{condition && <div>Show this if true</div>}
{condition ? <span>Yes</span> : <span>No</span>}
```

## Example
```jsx
import React, { useState } from 'react';

function ShowHide() {
  const [show, setShow] = useState(true);
  return (
    <div>
      <button onClick={() => setShow(s => !s)}>{show ? 'Hide' : 'Show'}</button>
      {show && <p>This is conditionally rendered!</p>}
    </div>
  );
}
``` 