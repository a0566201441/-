# Step 5 — Single-file build (inline CSS & JS)
This variant inlines all CSS (styles.css + mobile.css) and JS (app.js) directly in index.html.
Use this when the hosting platform doesn't upload folders like `/assets` or blocks extra files.

How to deploy:
- Upload **only** this `index.html`.
- Chart.js is still loaded from CDN.
- No logic changes; same UI polish as Step 4A.
