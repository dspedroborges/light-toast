# @light-toast/light-toast.js

Lightweight toast notifications with zero dependencies. Simple, responsive, and animated.

## Installation

```html
<script src="light-toast.min.js"></script>
```

## Size

- **minified:** ~2.5KB

That's it. That's the whole library.

## Quick Start

```html
<button onclick="toast.success('Saved successfully!')">Success</button>
<button onclick="toast.error('Something went wrong')">Error</button>
<button onclick="toast.info('Here is some info')">Info</button>

<script src="light-toast.min.js"></script>
```

---

## API

### toast.success(message, options)

Show a success toast.

```javascript
toast.success('Operation completed!');
```

### toast.error(message, options)

Show an error toast.

```javascript
toast.error('Failed to save');
```

### toast.info(message, options)

Show an info toast.

```javascript
toast.info('New message received');
```

---

## Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `position` | string | `'top-right'` | Where to show the toast |
| `duration` | number | `3000` | How long to show (ms) |

### Positions

- `'top-right'`
- `'top-left'`
- `'bottom-right'`
- `'bottom-left'`
- `'top-center'`
- `'bottom-center'`
- `'center'`

---

## Examples

### Custom Position

```javascript
toast.success('Top center!', { position: 'top-center' });
toast.error('Bottom left!', { position: 'bottom-left' });
```

### Custom Duration

```javascript
toast.info('Stays longer', { duration: 5000 }); // 5 seconds
toast.success('Quick message', { duration: 1000 }); // 1 second
```

### All Options

```javascript
toast.error('Critical error!', { 
  position: 'center',
  duration: 6000 
});
```

---

## Complete Example

```html
<!DOCTYPE html>
<html>
<body>
  <button onclick="toast.success('Item saved!')">Success</button>
  <button onclick="toast.error('Delete failed')">Error</button>
  <button onclick="toast.info('Processing...')">Info</button>
  
  <button onclick="toast.success('Top', { position: 'top-right' })">Top Right</button>
  <button onclick="toast.success('Bottom', { position: 'bottom-left' })">Bottom Left</button>
  <button onclick="toast.success('Center', { position: 'center' })">Center</button>

  <script src="light-toast.min.js"></script>
</body>
</html>
```

---

## Behavior

- Maximum 3 toasts per position container
- Auto-dismisses after the specified duration
- Smooth fade-in and fade-out animations
- Fixed positioning, works with scrolling

---

## Browser Support

Any modern browser. Chrome, Firefox, Safari, Edge all work.

## License

MIT
