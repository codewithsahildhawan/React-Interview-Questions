# Force a component to rerender without using useState in React?

## Explanation
You can force a rerender by using the `useReducer` hook or by updating a dummy state value.

## Syntax
```jsx
const [, forceUpdate] = useReducer(x => x + 1, 0);
forceUpdate();
```

## Example
```jsx
import React, { useReducer } from 'react';

function ForceRerender() {
  const [, forceUpdate] = useReducer(x => x + 1, 0);
  return (
    <div>
      <button onClick={forceUpdate}>Force Rerender</button>
    </div>
  );
} 