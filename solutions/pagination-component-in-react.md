# Create a pagination component.

## Explanation
Pagination divides data into pages. Use state to track the current page and slice the data array to display only the relevant items.

## Syntax
```jsx
const [page, setPage] = useState(1);
const itemsPerPage = 5;
const paginated = data.slice((page-1)*itemsPerPage, page*itemsPerPage);
```

## Example
```jsx
import React, { useState } from 'react';

const data = Array.from({ length: 20 }, (_, i) => `Item ${i+1}`);

function Pagination() {
  const [page, setPage] = useState(1);
  const itemsPerPage = 5;
  const paginated = data.slice((page-1)*itemsPerPage, page*itemsPerPage);
  return (
    <div>
      <ul>
        {paginated.map(item => <li key={item}>{item}</li>)}
      </ul>
      <button onClick={() => setPage(p => Math.max(1, p-1))} disabled={page === 1}>Prev</button>
      <button onClick={() => setPage(p => Math.min(Math.ceil(data.length/itemsPerPage), p+1))} disabled={page === Math.ceil(data.length/itemsPerPage)}>Next</button>
      <p>Page {page}</p>
    </div>
  );
}
``` 