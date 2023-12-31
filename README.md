# electron-bounds

Persisted window bounds for Electron.

## Quickstart

```ts
import { watchWindowBounds } from 'electron-bounds'

function createWindow(): void {
  const mainWindow = new BrowserWindow()
  watchWindowBounds(mainWindow)
}

app.whenReady().then(createWindow)
```

## Utils

### `watchWindowBounds`

Watch a window for changes in size and position and persist them in the store.

### `getWindowBounds`

Retrieve the window bounds from the store. Requires a window in case the store is empty.

### `saveWindowBounds`

Persist the bounds of a window in the store.

### `restoreWindowBounds`

Set a window's bounds to the bounds persisted in the store.

### `getWindowStorePath`

Get the path to the store file.

### `isOffScreen`

Check if the stored bounds would escape the screen.

### `centerWindow`

Center a window on the screen.
