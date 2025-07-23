# How to loop array/array of objects in React?

## Explanation
Use the JavaScript `map()` function to loop through arrays or arrays of objects and render elements for each item.

## Syntax
```jsx
{array.map(item => <div key={item.id}>{item.value}</div>)}
```

## Example
```jsx
import React from 'react';

const fruits = [
  { id: 1, value: 'Apple' },
  { id: 2, value: 'Banana' },
  { id: 3, value: 'Cherry' }
];

function FruitList() {
  return (
    <ul>
      {fruits.map(fruit => (
        <li key={fruit.id}>{fruit.value}</li>
      ))}
    </ul>
  );
}
``` 