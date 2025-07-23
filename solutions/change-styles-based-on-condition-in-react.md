# How to change styles based on condition in React?

## Explanation
You can change styles conditionally by using inline style objects or dynamic class names based on state or props.

## Syntax
```jsx
<div style={{ color: isActive ? 'green' : 'red' }}>Text</div>
<div className={isActive ? 'active' : 'inactive'}>Text</div>
```

## Example
```jsx
import React, { useState } from 'react';

function ConditionalStyle() {
  const [active, setActive] = useState(false);
  return (
    <div>
      <button onClick={() => setActive(a => !a)}>
        Toggle Style
      </button>
      <p style={{ color: active ? 'green' : 'red' }}>
        This text changes color!
      </p>
    </div>
  );
}
``` 