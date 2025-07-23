# Props vs State

## Explanation
Props are read-only data passed from parent to child. State is managed within the component and can change over time.

## Syntax
```jsx
// Props
<Child name="Alice" />
// State
const [count, setCount] = useState(0);
```

## Example
```jsx
import React, { useState } from 'react';

function Child({ name }) {
  return <p>Name: {name}</p>;
}

function Parent() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <Child name="Alice" />
      <button onClick={() => setCount(c => c + 1)}>Count: {count}</button>
    </div>
  );
}
``` 