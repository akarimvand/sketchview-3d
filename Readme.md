# ◈ SketchView 3D

> A professional, browser-based 3D viewer — packaged as a single, self-contained HTML file.

[![Three.js](https://img.shields.io/badge/Three.js-r160-black?logo=three.js)](https://threejs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Single File](https://img.shields.io/badge/Single%20File-HTML-success)]()

**Author:** Amin Naseri Karimvand  
**Email:** akarimvand@gmail.com

---

## 📖 About

**SketchView 3D** is a lightweight, install-free 3D viewer built on **Three.js**, delivered as a single HTML file. It's designed to view, edit, and export 3D models directly in the browser — no backend, no build step, no dependencies to install.

Just open the file and start viewing.

---

## ✨ Features

### 📦 Multi-Format Support
- **STL** — 3D printing standard
- **OBJ** (+ MTL and companion textures)
- **GLTF / GLB** — modern web standard
- **PLY** — point clouds and meshes
- **FBX** — animation and modeling format

### 🎨 Materials & Rendering
- 7 material types: **Standard (PBR)**, **Physical**, **Phong**, **Lambert**, **Toon**, **Normal**, **Basic**
- Full PBR parameters: metalness, roughness, opacity, environment intensity
- Display modes: **Solid**, **Wireframe**, **Points**, **X-Ray**
- Preset color palette + custom color picker

### 🖼️ Texture Management
- **Automatic bulk texture extraction** as a ZIP package
- **Markdown text report** of all model textures
- Advanced texture editor: repeat, offset, rotation, color factor
- Replace, remove, and toggle each slot
- Supports 19 texture slots (Base Color, Normal, Roughness, Metalness, AO, Emissive, etc.)
- **Automatic UV generation** for models without UVs

### 🌅 Environment & Lighting
- 6 **procedural HDRI** environments: Studio, Sunset, Forest, Night, Warehouse, City
- Three-point lighting: key, fill, rim
- Adjustable ambient light
- Soft shadows (PCF Soft Shadow)
- **Bloom** post-processing effect

### 📍 Annotations
- Add 3D pins to any point on the model
- Interactive tooltips
- Sidebar list with jump-to-annotation
- Delete individually or in bulk

### 📤 Export & Sharing
- **OBJ**, **STL (Binary)**, **GLB (with textures)**, **JSON**
- **PNG** screenshot and **4K** screenshot
- **Embed** code and copy-link

### 🎬 Scene Controls
- Toggle: grid, axes, shadows
- Auto-rotate with adjustable speed
- Camera FOV and damping controls
- Live FPS counter and model stats

### 🎁 Extras
- **Model gallery** — switch between loaded models
- **Drag & Drop** file upload
- **Multi-file loading** (OBJ + MTL + textures)
- **Full Persian (RTL) UI** with Vazirmatn font
- **Modern dark theme**
- **Keyboard shortcuts**: `F` (Fit), `R` (Reset), `A` (Annotate), `Esc`

---

## 🚀 Installation

### Option 1 — Direct Run
Download `index.html` and open it in your browser.

```bash
git clone https://github.com/YOUR_USERNAME/sketchview-3d.git
cd sketchview-3d
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

### Option 2 — Local Server (Recommended)
Avoids CORS issues when loading textures.

```bash
python -m http.server 8000     # Python 3
npx serve                      # Node.js
php -S localhost:8000          # PHP
```

Then open `http://localhost:8000`.

### Option 3 — GitHub Pages
1. Go to **Settings → Pages**
2. Source: branch `main`, folder `/ (root)`
3. Your site: `https://YOUR_USERNAME.github.io/sketchview-3d/`

### Requirements
- Modern browser with **WebGL 2.0** (Chrome, Firefox, Edge, Safari)
- Internet only for the initial Three.js CDN load

---

## 📚 Usage

### Load a Model
Click **📤 Upload Model** in the header, or **drop** a file onto the central area.
For OBJ models, select `.obj`, `.mtl`, and texture images together.

### Edit Materials
Open the **🎨 Material** tab:
- Choose a material type (recommended: "Keep Original" for textured models)
- Adjust color, metalness, roughness, and more

### Work with Textures
Open the **🖼️ Textures** tab — all textures in the model are listed.
- Click a card to open its editor
- **📥 Extract All Textures** creates a ZIP with all textures + manifest

### Annotations
1. Click **📍 Annotate** in the toolbar
2. Click on the model
3. Enter the annotation text
4. Right-click to delete, or use the **📍 Notes** tab

### Export
Open the **📤 Export** tab:
- **OBJ** / **STL** for 3D printing
- **GLB** for the web (with embedded textures)
- **JSON** for programmatic processing
- **Screenshots** at standard or 4K quality

---

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|---|---|---|
| [Three.js](https://threejs.org/) | r160 | 3D rendering engine |
| OrbitControls | — | Camera control |
| EffectComposer | — | Post-processing |
| UnrealBloomPass | — | Bloom effect |
| [JSZip](https://stuk.github.io/jszip/) | 3.10.1 | ZIP creation |
| [Vazirmatn](https://github.com/rastikerdar/vazirmatn) | v33 | Persian font |
| Vanilla JS | ES2020+ | Logic |
| CSS3 | — | Styling |

---

## 📁 Project Structure

```
sketchview-3d/
├── index.html          # Entire app (HTML + CSS + JS)
├── README.md           # This file
├── LICENSE             # MIT License
└── screenshots/        # Optional images
    ├── main.png
    ├── textures.png
    └── annotations.png
```

---

## 🤝 Contributing

1. **Fork** the project
2. Create a branch: `git checkout -b feature/AmazingFeature`
3. Commit: `git commit -m 'Add some AmazingFeature'`
4. Push: `git push origin feature/AmazingFeature`
5. Open a **Pull Request**

### Roadmap
- [ ] GLTF/FBX animation support
- [ ] Distance measurement tool
- [ ] Cross-section slicing
- [ ] Save/load scene presets
- [ ] Light mode theme
- [ ] PWA and offline mode
- [ ] Large point cloud support (LOD)

---

## 🐛 Bug Reports

Open a new [Issue](https://github.com/YOUR_USERNAME/sketchview-3d/issues) and include:
- Problem description
- Steps to reproduce
- Browser and OS
- Screenshot or video (if possible)

---

## 📄 License

Released under the **MIT License**. See [LICENSE](LICENSE) for details.

```
MIT License

Copyright (c) 2026 Amin Naseri Karimvand

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📬 Contact

**Amin Naseri Karimvand**  
📧 Email: [akarimvand@gmail.com](mailto:akarimvand@gmail.com)  
🐙 GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)

For questions, suggestions, or collaboration — feel free to reach out.

---

## 🙏 Acknowledgements

- [Three.js](https://threejs.org/) — powerful 3D engine
- [Vazirmatn](https://github.com/rastikerdar/vazirmatn) — Persian font
- [JSZip](https://stuk.github.io/jszip/) — easy ZIP creation
- All contributors and users of this project ❤️

---

<div align="center">

**⭐ If you find this project useful, please give it a star! ⭐**

Made with ❤️ by **Amin Naseri Karimvand**

</div>
