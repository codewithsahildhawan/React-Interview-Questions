# Explain debouncing and throttling in React

## Explanation
Debouncing delays a function call until after a pause in events. Throttling limits a function to run at most once per interval. Both are used to optimize performance for frequent events.

## Syntax
```js
// Debounce
function debounce(fn, delay) {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
// Throttle
function throttle(fn, limit) {
  let inThrottle;
  return (...args) => {
    if (!inThrottle) {
      fn(...args);
      inThrottle = true;
      setTimeout(() => (inThrottle = false), limit);
    }
  };
}
```

## Example
```jsx
import React, { useState } from 'react';

function DebouncedInput({ onChange }) {
  const [value, setValue] = useState('');
  const handleChange = e => {
    setValue(e.target.value);
    onChange(e.target.value);
  };
  return <input value={value} onChange={handleChange} />;
}
``` 