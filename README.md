# Interactive 3D Skeleton Sphere

![Demo](demo.gif)

The Interactive 3D Skeleton Sphere is a visually striking WebGL component that creates an engaging 3D visualization with interactive elements. Built with Three.js, this animated sphere features a wireframe design with protruding "bones" that respond to user interaction. Perfect for portfolios, tech showcases, or as an eye-catching background element.

## Features

- **Interactive 3D Visualization**: Sphere with wireframe design and protruding bones
- **Mouse/Touch Interaction**: Bones extend and rotate in response to cursor movement
- **Auto-Rotation**: Smooth automatic rotation when not interacting
- **Responsive Design**: Works on all device sizes
- **Loading Animation**: Elegant loading sequence with progress bar
- **Subtle Animations**: Wave motion on bones and pulsing effect on sphere
- **Orbit Controls**: User can rotate, zoom, and pan the camera

## Installation

To use this component in your project, follow these steps:

1. Add the HTML container where you want the 3D sphere to appear:
```html
<div id="skeletonContainer">
  <!-- The 3D visualization will render here -->
</div>
```

2. Include the required Three.js libraries in your `<head>`:
```html
<script src="https://cdn.jsdelivr.net/npm/three@0.132.2/build/three.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/three@0.132.2/examples/js/controls/OrbitControls.min.js"></script>
```

3. Add the CSS styles to your stylesheet:
```css
#skeletonContainer {
  position: relative;
  width: 100%;
  height: 600px; /* Adjust height as needed */
  overflow: hidden;
}

.info-panel {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  z-index: 100;
  background: rgba(15, 23, 42, 0.85);
  backdrop-filter: blur(12px);
  border-radius: 14px;
  padding: 1.5rem 2rem;
  border: 1px solid rgba(255, 255, 255, 0.12);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.25);
  max-width: 90%;
  text-align: center;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

/* ... (see full CSS in index.html) ... */
```

4. Add the JavaScript implementation to your project:
```javascript
// Full implementation code (see index.html)
```

## Customization

You can customize various aspects of the visualization:

1. **Colors**:
```javascript
// Change wireframe color
const wireMaterial = new THREE.MeshPhongMaterial({
  color: 0x60a5fa, // Change this hex value
  // ...
});

// Change bone colors
const boneMaterial = new THREE.MeshPhongMaterial({
  color: new THREE.Color().setHSL(hue, 0.7, 0.7), // Adjust HSL values
  // ...
});
```

2. **Size and Density**:
```javascript
// Adjust sphere detail
const geometry = new THREE.SphereGeometry(1, 36, 36); // Increase segments for more detail

// Change number of bones
const boneCount = 32; // Increase or decrease this value
```

3. **Animation Parameters**:
```javascript
// Adjust hover sensitivity
hoverProgress += (isHovering ? 0.1 : -0.05); // Change these values

// Modify bone extension length
targetPosition: new THREE.Vector3(x * 1.7, y * 1.7, z * 1.7) // Increase multiplier
```

4. **Lighting**:
```javascript
// Modify light intensity and positions
const light1 = new THREE.DirectionalLight(0xffffff, 0.8); // Change intensity
light1.position.set(2, 1, 3); // Change position
```

## Dependencies

- [Three.js](https://threejs.org/) (v0.132.2)
- [OrbitControls](https://threejs.org/docs/#examples/en/controls/OrbitControls)

## Usage Examples

1. **Portfolio Background**:
```html
<div id="skeletonContainer" style="height: 100vh; position: fixed; top: 0; left: 0;">
  <!-- Your content overlayed on top -->
  <div style="position: relative; z-index: 200; padding: 2rem;">
    <h1>Your Portfolio</h1>
    <!-- ... -->
  </div>
</div>
```

2. **Product Showcase Section**:
```html
<section style="position: relative;">
  <div id="skeletonContainer" style="height: 80vh;"></div>
  <div class="product-info" style="position: absolute; top: 50%; transform: translateY(-50%);">
    <!-- Product details -->
  </div>
</section>
```

3. **Loading Screen**:
```html
<div id="skeletonContainer" style="height: 100vh;">
  <div class="loading-content" style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);">
    <!-- Loading progress/content -->
  </div>
</div>
```

## Browser Support

The Interactive 3D Skeleton Sphere works on all modern browsers that support WebGL:

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

Note: Internet Explorer is not supported.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a pull request

## Support

If you encounter any issues or have questions, please [open an issue](https://github.com/yourusername/interactive-3d-sphere/issues).

---

**Enjoy the mesmerizing 3D experience!** ✨
