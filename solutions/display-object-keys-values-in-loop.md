# Display keys and values of objects in a loop in React?

## Explanation
You can use `Object.entries()` to get an array of key-value pairs from an object and then map over them to display each pair.

## Syntax
```jsx
{Object.entries(obj).map(([key, value]) => (
  <div key={key}>{key}: {value}</div>
))}
```

## Example
```jsx
import React from 'react';

const user = {
  name: 'Alice',
  age: 25,
  city: 'New York'
};

function UserDetails() {
  return (
    <div>
      {Object.entries(user).map(([key, value]) => (
        <p key={key}>{key}: {value}</p>
      ))}
    </div>
  );
}
``` 