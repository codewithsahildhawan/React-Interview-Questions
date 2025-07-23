# Given two dropdowns, select 2nd dropdown options based on value selected in one dropdown? (Load states based on country selected)

## Explanation
You can use state to store the selected value of the first dropdown and filter the options for the second dropdown based on that value.

## Syntax
```jsx
<select onChange={...}>{/* countries */}</select>
<select>{/* states filtered by selected country */}</select>
```

## Example
```jsx
import React, { useState } from 'react';

const data = {
  USA: ['California', 'Texas', 'Florida'],
  India: ['Delhi', 'Mumbai', 'Bangalore']
};

function DependentDropdowns() {
  const [country, setCountry] = useState('USA');
  return (
    <div>
      <select value={country} onChange={e => setCountry(e.target.value)}>
        {Object.keys(data).map(c => <option key={c}>{c}</option>)}
      </select>
      <select>
        {data[country].map(state => <option key={state}>{state}</option>)}
      </select>
    </div>
  );
}
``` 