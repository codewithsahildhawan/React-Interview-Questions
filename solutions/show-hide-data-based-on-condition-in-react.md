# How to show and hide data based on condition in React?

## Explanation
You can show or hide elements in React by conditionally rendering them based on state or props.

## Syntax
```jsx
{isVisible && <div>Visible Content</div>}
```

## Example
```jsx
import React, { useState } from 'react';

function ToggleVisibility() {
  const [visible, setVisible] = useState(false);
  return (
    <div>
      <button onClick={() => setVisible(v => !v)}>
        {visible ? 'Hide' : 'Show'}
      </button>
      {visible && <p>This content is visible!</p>}
    </div>
  );
}
``` 