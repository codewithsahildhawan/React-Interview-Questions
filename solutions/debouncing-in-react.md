# How to perform debouncing?

## Explanation
Debouncing is a technique to limit how often a function is called. In React, you can debounce input handlers to reduce API calls or expensive operations.

## Syntax
```jsx
useEffect(() => {
  const handler = setTimeout(() => {
    // do something
  }, delay);
  return () => clearTimeout(handler);
}, [value]);
```

## Example
```jsx
import React, { useState, useEffect } from 'react';

function DebouncedInput() {
  const [value, setValue] = useState('');
  const [debounced, setDebounced] = useState('');

  useEffect(() => {
    const handler = setTimeout(() => setDebounced(value), 500);
    return () => clearTimeout(handler);
  }, [value]);

  return (
    <div>
      <input value={value} onChange={e => setValue(e.target.value)} />
      <p>Debounced value: {debounced}</p>
    </div>
  );
}
``` 