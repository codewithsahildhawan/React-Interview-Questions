# Create a search textbox filter?

## Explanation
A search textbox filter allows users to filter a list based on their input. Use state to store the search term and filter the array accordingly.

## Syntax
```jsx
const [search, setSearch] = useState('');
const filtered = items.filter(item => item.includes(search));
```

## Example
```jsx
import React, { useState } from 'react';

const items = ['Apple', 'Banana', 'Cherry', 'Date'];

function SearchFilter() {
  const [search, setSearch] = useState('');
  const filtered = items.filter(item => item.toLowerCase().includes(search.toLowerCase()));
  return (
    <div>
      <input value={search} onChange={e => setSearch(e.target.value)} placeholder="Search..." />
      <ul>
        {filtered.map(item => <li key={item}>{item}</li>)}
      </ul>
    </div>
  );
}
``` 