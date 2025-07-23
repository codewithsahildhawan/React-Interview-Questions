# Bind array/array of objects to radio button in React?

## Explanation
To bind an array or array of objects to radio buttons, map over the array and render a radio input for each item.

## Syntax
```jsx
{array.map(item => (
  <label key={item.id}>
    <input type="radio" name="group" value={item.value} />
    {item.value}
  </label>
))}
```

## Example
```jsx
import React, { useState } from 'react';

const options = [
  { id: 1, value: 'Red' },
  { id: 2, value: 'Green' },
  { id: 3, value: 'Blue' }
];

function RadioGroup() {
  const [selected, setSelected] = useState('');
  return (
    <div>
      {options.map(opt => (
        <label key={opt.id}>
          <input
            type="radio"
            name="color"
            value={opt.value}
            checked={selected === opt.value}
            onChange={e => setSelected(e.target.value)}
          />
          {opt.value}
        </label>
      ))}
    </div>
  );
}
``` 