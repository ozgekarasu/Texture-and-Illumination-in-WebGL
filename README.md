# CS405 Project 2 – Texture & Illumination

This repository contains the implementation for **CS405: Computer Graphics Project 2** at Sabancı University.  
The project focuses on **texture mapping of arbitrary-sized images** and **basic illumination (ambient + diffuse lighting)** in a WebGL environment.

---

## Project Structure

| File | Description |
|------|--------------|
| `index.html` | Main WebGL interface with canvas and UI controls |
| `mesh_renderer.js` | Core rendering logic implementing texture and lighting |
| `mesh_loader.js` | Handles `.obj` model loading and buffer creation |
| `CS405_Report_Texture_Illumination.docx` | Report explaining methodology and implementation details |

---

## Tasks Overview

### **Task 1 – Texture Mapping**
- Modified the `setTexture()` method to support images with **non-power-of-two dimensions**.
- Applied:
  ```js
  gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_S, gl.CLAMP_TO_EDGE);
  gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_T, gl.CLAMP_TO_EDGE);
  gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_MIN_FILTER, gl.LINEAR);
