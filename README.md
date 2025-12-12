Solaris 3D Explorer
Interactive Three.js Solar System Visualization (Single File)
A fully client-side, interactive 3D solar system explorer built using Three.js and styled with Tailwind CSS, 
designed for simplicity and maximum performance. 
This entire application—from the 3D rendering engine to the modern UI—is contained within a single index.html file, demonstrating the power of browser-based module imports.

Category,Feature,Description
3D Core,Orbital Mechanics,Planets rotate on their axis and orbit the Sun based on scaled-down speed and distance parameters.
Visuals,Pure Color Spheres,"Planets are rendered as solid, untextured spheres with distinct colors, utilizing MeshStandardMaterial for realistic lighting and shadows from the central PointLight (the Sun)."
Immersion,Atmospheric Glow,"Atmospheric effect implemented using THREE.Sprite with AdditiveBlending on Earth and Venus for a simple, non-performance-heavy glow layer."
Environment,Interactive Starfield,"The background is a pure black void populated by thousands of interactive THREE.Points (stars), replacing static image skyboxes."
Interactivity,Smooth Zoom-Focus,"Clicking any planet or the Sun triggers a smooth, interpolated camera movement that zooms into and continuously tracks the chosen celestial body."
UI/UX,Glassmorphism UI,"Modern, responsive interface built with Tailwind CSS, featuring glassmorphism panels for a sleek, space-age feel."

3D Engine: Three.js (r160) using ES Module imports.

Controls: OrbitControls.js for camera interaction.

Styling: Tailwind CSS (using the CDN) for responsive and utility-first styling.

Architecture: Single-File Module (SFM). All JavaScript uses importmap to manage dependencies directly in the browser.

🚀 How to Run (100% Client-Side)
Since the entire application is contained in one file and relies only on public CDNs for its libraries, deployment couldn't be simpler:

Clone the repository:

Bash

git clone [your-repo-link]
Open the file: Drag the index.html file into any modern web browser (Chrome, Firefox, Edge, etc.).

No local server (like npm start) is required, although using one may be necessary for texture loading in more complex versions.

💡 Key Architectural Note
The entire application state and logic are encapsulated within the single <script type="module"> block in index.html. This structure simplifies development by eliminating the need for bundlers like Webpack or Vite, making it a perfect example of a powerful, modern, dependency-free web application.
