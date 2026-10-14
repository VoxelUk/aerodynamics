# AEROLAB — Browser Aerodynamics Prototype

A single-page Three.js prototype for GitHub Pages. It includes:
- Interactive 3D viewport with orbit, zoom, and pan
- Drag-and-drop or file-picker model import: GLB, glTF, OBJ, STL, PLY
- Animated illustrative particle/streamline effects
- Wind speed, angle of attack, density, reference area, Cd and Cl controls
- Estimated dynamic pressure, drag, lift, and Reynolds number readouts

## Publish on GitHub Pages
1. Create a new GitHub repository.
2. Upload `index.html` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose your default branch (usually `main`) and folder `/ (root)`, then Save.
6. Wait for the Pages URL to appear in the Pages settings.

## Important scientific limitation
This is a visual prototype, not a computational fluid dynamics solver. The moving particles and streamlines are illustrative effects. Lift and drag are calculated from user-supplied coefficients and reference area; they are not derived from the imported model's geometry. Reynolds number uses an approximate 4.1 m reference length after normalization, so treat it as a rough display value only. Do not use these outputs for engineering validation or safety-critical design.

## Notes
- Three.js and its loaders are imported from jsDelivr, so the page needs an internet connection.
- A single-file `.glb` is the most convenient import format. `.gltf` models may rely on external textures or binary files and may not load if those companion files are not available.
- No uploaded model is sent to a server by this page; file processing occurs in the browser.
