# Forms & controlled inputs

## Explanation
Controlled inputs are form elements whose value is managed by React state. This allows validation and dynamic updates.

## Syntax
```jsx
const [value, setValue] = useState('');
<input value={value} onChange={e => setValue(e.target.value)} />
```

## Example
```jsx
import React, { useState } from 'react';

function MyForm() {
  const [name, setName] = useState('');
  const handleSubmit = e => {
    e.preventDefault();
    alert(`Hello, ${name}`);
  };
  return (
    <form onSubmit={handleSubmit}>
      <input value={name} onChange={e => setName(e.target.value)} />
      <button type="submit">Submit</button>
    </form>
  );
}
``` 