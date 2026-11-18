# Percent — proposed asset-based Three.js integration (not implemented in V2)

Goal: retain the approved design and replace selected flat garment visuals with genuinely pre-existing 3D assets, not procedural T-shirt meshes or fake 3D.

## Asset requirements

- Obtain commercially licensed or brand-owned GLB/glTF models for both Oversized Fit and Regular Fit. Review the actual silhouette, sleeves, seams, wrinkles, collar, fabric, UVs and logo positioning before use. Check license, attribution, redistribution and modification permissions before bundling any asset.
- Obtain separately approved human models with clothing and compatible poses/rigging for Try the Look. A garment GLB on its own does not automatically provide realistic cloth fitting or human animation.
- Prefer compressed, optimized models with physically based materials and efficient textures. Test actual mobile devices before using several animated 3D characters simultaneously.

## Implementation order after asset approval

1. Prototype a single garment in the product detail overlay using Three.js GLTFLoader; support drag rotation with a static photo fallback for unsupported WebGL or reduced-motion preferences.
2. Replace the central garment in Latest Drop with the approved asset, preserving current carousel drag, color and selection logic. Only after performance validation, expand to nearby models. Use a shared rendering context where practical and avoid one persistent WebGL renderer per item.
3. Evaluate the human lookbook separately once realistic compatible human and garment assets are available. Preserve the swipe/tap distinction and navigation.
4. Load assets lazily, pause rendering outside the viewport, cap device pixel ratio, dispose geometries/materials/textures and clean up on modal close. Verify device memory, frame pacing, fallback behavior, contrast, and touch accessibility.

Three.js official GLTFLoader documentation: https://threejs.org/docs/pages/GLTFLoader.html
Three.js official model loading guide: https://threejs.org/manual/pages/loading-3d-models.html

V2 remains dependency-free and offline. No external stock model has been substituted, and this document is a plan, not a claim of implemented 3D functionality.
