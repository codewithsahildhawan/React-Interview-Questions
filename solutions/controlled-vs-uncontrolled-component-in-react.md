# Create a controlled and uncontrolled component in React.

## Explanation
A controlled component's value is managed by React state. An uncontrolled component's value is managed by the DOM, accessed via refs.

## Syntax
```jsx
// Controlled
<input value={value} onChange={e => setValue(e.target.value)} />
// Uncontrolled
<input ref={inputRef} />
```

## Example
```jsx
import React, { useRef, useState } from 'react';

function Controlled() {
  const [value, setValue] = useState('');
  return <input value={value} onChange={e => setValue(e.target.value)} />;
}

function Uncontrolled() {
  const inputRef = useRef(null);
  const showValue = () => alert(inputRef.current.value);
  return (
    <div>
      <input ref={inputRef} />
      <button onClick={showValue}>Show Value</button>
    </div>
  );
}
```

# Explain the difference between controlled and uncontrolled components

## Explanation
A controlled component's value is managed by React state, while an uncontrolled component's value is managed by the DOM and accessed via refs. Controlled components are preferred for validation and dynamic updates.

## Syntax
```jsx
// Controlled
<input value={value} onChange={e => setValue(e.target.value)} />
// Uncontrolled
<input ref={inputRef} />
```

## Example
```jsx
import React, { useRef, useState } from 'react';

function Controlled() {
  const [value, setValue] = useState('');
  return <input value={value} onChange={e => setValue(e.target.value)} />;
}

function Uncontrolled() {
  const inputRef = useRef(null);
  const showValue = () => alert(inputRef.current.value);
  return (
    <div>
      <input ref={inputRef} />
      <button onClick={showValue}>Show Value</button>
    </div>
  );
}
``` 