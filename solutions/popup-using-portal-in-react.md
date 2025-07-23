# Create a popup using portal.

## Explanation
React portals let you render children into a DOM node outside the parent component hierarchy using `ReactDOM.createPortal`.

## Syntax
```jsx
ReactDOM.createPortal(child, container)
```

## Example
```jsx
import React from 'react';
import ReactDOM from 'react-dom';

function Modal({ open, children }) {
  if (!open) return null;
  return ReactDOM.createPortal(
    <div className="modal">{children}</div>,
    document.body
  );
}

function App() {
  const [open, setOpen] = React.useState(false);
  return (
    <div>
      <button onClick={() => setOpen(true)}>Open Modal</button>
      <Modal open={open}>
        <h2>Modal Content</h2>
        <button onClick={() => setOpen(false)}>Close</button>
      </Modal>
    </div>
  );
} 