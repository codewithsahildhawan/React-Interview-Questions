# How to add data into useState array in functional component in React?

## Explanation
To add data to an array in state, use the spread operator to create a new array and update the state.

## Syntax
```jsx
const [arr, setArr] = useState([]);
setArr(prev => [...prev, newItem]);
```

## Example
```jsx
import React, { useState } from 'react';

function AddToArray() {
  const [items, setItems] = useState([]);
  const addItem = () => setItems(prev => [...prev, `Item ${prev.length + 1}`]);
  return (
    <div>
      <button onClick={addItem}>Add Item</button>
      <ul>
        {items.map((item, idx) => <li key={idx}>{item}</li>)}
      </ul>
    </div>
  );
}
``` 