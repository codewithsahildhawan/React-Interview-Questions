# Display radio button data selected by user in another textbox?

## Explanation
You can display the selected radio button value in another textbox by storing the value in state and binding it to the textbox.

## Syntax
```jsx
<input type="radio" value={value} onChange={...} />
<input value={selectedValue} readOnly />
```

## Example
```jsx
import React, { useState } from 'react';

function RadioToTextbox() {
  const [selected, setSelected] = useState('');
  return (
    <div>
      <label>
        <input type="radio" name="fruit" value="Apple" onChange={e => setSelected(e.target.value)} /> Apple
      </label>
      <label>
        <input type="radio" name="fruit" value="Banana" onChange={e => setSelected(e.target.value)} /> Banana
      </label>
      <input value={selected} readOnly placeholder="Selected value" />
    </div>
  );
}
``` 