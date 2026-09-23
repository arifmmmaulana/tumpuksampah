# AI Agent Rules

## Image Optimization (Partner Logos)
When adding a new partner logo to the project (e.g. for `TrackRecord.jsx`), you MUST automatically optimize the image to ensure consistent size and performance:
1. Resize the image to be exactly a `300x300` square. If the original image is not square, use padding/contain (`fit: 'contain', background: '#ffffff'`) to make it square without stretching.
2. Ensure the background is white (if the original is a PNG with transparency, flatten it with `#ffffff`).
3. Convert the image to `.jpg` format with high quality compression (e.g. `quality: 85`).
4. Update the `scripts/optimize-images.mjs` jobs array to include the new logo so it remains part of the automated optimization pipeline.
5. Import and use the optimized `.jpg` file in the codebase.
