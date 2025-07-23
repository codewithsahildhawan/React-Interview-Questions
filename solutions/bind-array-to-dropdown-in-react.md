# How to bind array/array of objects to dropdown in React?

## Explanation
To bind an array or array of objects to a dropdown, map over the array and render `<option>` elements for each item.

## Syntax
```jsx
<select>
  {array.map(item => <option key={item.id}>{item.value}</option>)}
</select>
```

## Example
```jsx
import React from 'react';

const options = [
  { id: 1, value: 'Apple' },
  { id: 2, value: 'Banana' },
  { id: 3, value: 'Cherry' }
];

function Dropdown() {
  return (
    <select>
      {options.map(opt => (
        <option key={opt.id} value={opt.value}>{opt.value}</option>
      ))}
    </select>
  );
}
``` 