# ◈ SketchView 3D

> A professional, browser-based 3D viewer — packaged as a single, self-contained HTML file.

[![Three.js](https://img.shields.io/badge/Three.js-r160-black?logo=three.js)](https://threejs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Single File](https://img.shields.io/badge/Single%20File-HTML-success)]()

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
