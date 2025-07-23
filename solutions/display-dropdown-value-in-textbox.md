# How to display dropdown value selected by user in another textbox?

## Explanation
Store the selected dropdown value in state and bind it to the value of another textbox.

## Syntax
```jsx
<select onChange={e => setValue(e.target.value)}>
  {/* options */}
</select>
<input value={value} readOnly />
```

## Example
```jsx
import React, { useState } from 'react';

function DropdownToTextbox() {
  const [selected, setSelected] = useState('');
  return (
    <div>
      <select onChange={e => setSelected(e.target.value)}>
        <option value="">Select</option>
        <option value="One">One</option>
        <option value="Two">Two</option>
      </select>
      <input value={selected} readOnly placeholder="Selected value" />
    </div>
  );
}
``` 