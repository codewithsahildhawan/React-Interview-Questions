# SSR vs CSR

## Explanation
SSR (Server-Side Rendering) renders React components on the server and sends HTML to the client. CSR (Client-Side Rendering) renders components in the browser.

## Syntax
```js
// SSR: Next.js example
export async function getServerSideProps() { /* ... */ }
// CSR: Standard React
useEffect(() => { /* ... */ }, []);
```

## Example
```jsx
// SSR (Next.js)
export async function getServerSideProps() {
  return { props: { data: 'Hello from server' } };
}
function Page({ data }) {
  return <div>{data}</div>;
}

// CSR (React)
import React, { useEffect, useState } from 'react';
function Page() {
  const [data, setData] = useState('');
  useEffect(() => { setData('Hello from client'); }, []);
  return <div>{data}</div>;
}
``` 