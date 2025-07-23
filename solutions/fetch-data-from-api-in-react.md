# Create a component to fetch data from API?

## Explanation
Use the `useEffect` hook to fetch data from an API when the component mounts. Store the data in state.

## Syntax
```jsx
useEffect(() => {
  fetch(url)
    .then(res => res.json())
    .then(data => setData(data));
}, []);
```

## Example
```jsx
import React, { useState, useEffect } from 'react';

function FetchData() {
  const [data, setData] = useState(null);
  useEffect(() => {
    fetch('https://jsonplaceholder.typicode.com/posts/1')
      .then(res => res.json())
      .then(data => setData(data));
  }, []);
  return (
    <div>
      {data ? <pre>{JSON.stringify(data, null, 2)}</pre> : 'Loading...'}
    </div>
  );
}
``` 