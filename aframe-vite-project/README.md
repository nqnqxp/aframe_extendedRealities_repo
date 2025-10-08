# A-Frame Vite Project

This project combines [Vite](https://vitejs.dev/) with [A-Frame](https://aframe.io/) version 1.7.0 for creating immersive WebVR experiences with fast development and hot module replacement.

## Features

- ⚡️ Vite for lightning-fast development
- 🥽 A-Frame 1.7.0 for WebVR/WebXR experiences
- 🎨 Pre-configured CSS for A-Frame scenes
- 🚀 Hot Module Replacement (HMR)
- 📦 Optimized production builds

## Getting Started

### Installation

Dependencies are already installed. If you need to reinstall them:

```bash
npm install
```

### Development

Start the development server with hot reload:

```bash
npm run dev
```

Then open your browser to the URL shown in the terminal (typically `http://localhost:5173`).

### Building for Production

Create an optimized production build:

```bash
npm run build
```

### Preview Production Build

Preview the production build locally:

```bash
npm run preview
```

## Project Structure

```
aframe-vite-project/
├── src/
│   ├── main.js        # Main entry point, imports A-Frame
│   └── style.css      # CSS styling for A-Frame scenes
├── public/            # Static assets
├── index.html         # HTML with A-Frame scene
├── package.json       # Project dependencies
└── vite.config.js     # Vite configuration
```

## A-Frame Scene

The project includes a basic A-Frame scene with:
- A colored sky
- A ground plane
- Geometric primitives (box, sphere, cylinder)
- Camera with look and WASD controls

### Controls

- **Mouse**: Look around by clicking and dragging
- **WASD**: Move around the scene
  - W: Forward
  - A: Left
  - S: Backward
  - D: Right

## Customization

### Adding New Objects

Edit `index.html` and add A-Frame primitives inside the `<a-scene>` tag:

```html
<a-box position="0 1 -3" color="#FF0000"></a-box>
```

### Styling

Modify `src/style.css` to customize the appearance of your scene or add UI overlays.

### A-Frame Components

You can register custom A-Frame components in `src/main.js`:

```javascript
AFRAME.registerComponent('my-component', {
  init: function () {
    // Component logic here
  }
});
```

## Resources

- [A-Frame Documentation](https://aframe.io/docs/)
- [A-Frame School](https://aframe.io/aframe-school/)
- [Vite Documentation](https://vitejs.dev/)
- [A-Frame Inspector](https://aframe.io/docs/master/introduction/visual-inspector-and-dev-tools.html) - Press `Ctrl+Alt+I` in the browser

## Troubleshooting

### A-Frame not loading
Make sure A-Frame is properly imported in `src/main.js`:
```javascript
import 'aframe'
```

### Scene not visible
Check that your CSS doesn't have conflicting styles. The body and html should have no margins and full height.

## License

MIT

