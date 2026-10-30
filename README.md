<p align="center">
  <img src="icons/icon-192.png" width="96" alt="SoEasy DICOM Web logo">
</p>

<h1 align="center">SoEasy DICOM Web</h1>

<p align="center">
  The browser, iPad and iPhone version of <a href="https://github.com/TrithoneSE/SoEasy-DICOM-Viewer"><b>SoEasy DICOM Viewer</b></a> —
  2D, cine, DSA, MPR, layouts with reference lines and colour 3D volume rendering, with nothing to install.
</p>

<p align="center">
  <a href="https://trithonese.github.io/SoEasy-DICOM-Web/"><img alt="Open SoEasy DICOM Web" src="https://img.shields.io/badge/%E2%96%B6%20Open%20the%20web%20app-trithonese.github.io-2ea44f?style=for-the-badge"></a>
  &nbsp;
  <a href="https://github.com/TrithoneSE/SoEasy-DICOM-Viewer/releases/latest"><img alt="Windows desktop version" src="https://img.shields.io/badge/Windows%20desktop%20version-download-0a5bd3?style=for-the-badge"></a>
</p>

<p align="center">
  <img alt="Platform: any modern browser" src="https://img.shields.io/badge/platform-Safari%20%7C%20Chrome%20%7C%20Edge%20%7C%20Firefox-555">
  <img alt="iPad and iPhone" src="https://img.shields.io/badge/iPad%20%7C%20iPhone-installable%20(offline)-555">
  <img alt="No upload" src="https://img.shields.io/badge/images-never%20uploaded-2ea44f">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/TrithoneSE/SoEasy-DICOM-Viewer/main/docs/media/3d-cinematic.gif" width="640" alt="3D snapshot movie: the skull opens to show a segmented tumour and the arteries around it">
</p>

> **Not a medical device.** SoEasy DICOM Web is a visualisation tool for education, research and personal use.
> It is not certified for diagnosis or treatment decisions. Always rely on the original images and the radiologist's
> report.

---

## Open the app

**👉 [https://trithonese.github.io/SoEasy-DICOM-Web/](https://trithonese.github.io/SoEasy-DICOM-Web/)**

That link *is* the release: the web app is updated in place, so it is always the latest version and there is
nothing to download. Share this link (not the repository's *Releases* page — the web version has no download files).

- **iPad / iPhone**: open the link in Safari → *Share* → *Add to Home Screen*. It then starts full-screen from its own
  icon and works **offline**.
- **Android / Chrome / Edge**: open the link → menu → *Install app* (or *Add to Home screen*).
- **Desktop browser**: just open the link; drag DICOM files, a folder or a .zip onto the page.

Looking for the full Windows application (segmentation, DTI, fusion, more measurements)? Download
**[SoEasy DICOM Viewer](https://github.com/TrithoneSE/SoEasy-DICOM-Viewer/releases/latest)**.

## Contents

- [Open the app](#open-the-app)
- [Highlights](#highlights)
- [Web or desktop?](#web-or-desktop)
- [Getting started](#getting-started)
- [Features in detail](#features-in-detail)
- [Requirements](#requirements)
- [Privacy](#privacy)
- [About this repository](#about-this-repository)

## Highlights

- **Runs in the browser** — Safari on iPad and iPhone, Chrome, Edge and Firefox on any computer. Installable as an
  app and usable offline.
- **Opens DICOM from files, folders or a .zip archive**, including JPEG baseline / lossless, JPEG-LS, JPEG 2000 and
  RLE compressed images (decoded with WebAssembly in a background worker).
- **2D viewing** with drag window / level, CT presets (abdomen / mediastinum, subdural, temporal bone, …), auto window,
  invert, pan, zoom and pinch-zoom, length measurements, MIP / MinIP / average slabs (5–40 mm).
- **Cine** for multi-frame runs at the file's own frame rate.
- **DSA** for X-ray angiography runs: subtraction on / off, the displayed frame as mask, reset, automatic pixel shift.
- **Layouts** 1 × 1, 1 × 2 and 2 × 2 with **reference lines** and a 3D cursor between series.
- **MPR** — sagittal, coronal and axial planes, tiltable axes, slab MIP.
- **Colour 3D volume rendering** (WebGL 2) with the same colour-curve editor and presets as the desktop app, bone
  colour lock, crop box, scalpel with undo, and snapshots of views.
- **Shares presets with the desktop app** — import and export colour presets as the same .json files.

## Web or desktop?

Both versions share the same viewing engine ideas, colour presets and look. Use the web version to look at a study
quickly on any device; use the desktop version for the full toolset.

| Feature | [SoEasy DICOM Viewer](https://github.com/TrithoneSE/SoEasy-DICOM-Viewer) (Windows) | SoEasy DICOM Web (browser) |
|---|:---:|:---:|
| Install | installer or portable zip | none — open a link |
| Runs on | Windows 10 / 11 64-bit | iPad, iPhone, Android, Mac, Windows, Linux |
| Works offline | ✅ | ✅ (after *Add to Home Screen* / install) |
| Images stay on the device | ✅ | ✅ |
| Open folders and files | ✅ | ✅ |
| Archives | .zip, .rar, .7z, .tar | .zip |
| CD / DVD / DICOMDIR | ✅ | folder scan |
| Compressed DICOM (JPEG, JPEG-LS, JPEG 2000, RLE) | ✅ | ✅ |
| Window / level, presets, invert | ✅ | ✅ |
| Touch: pinch zoom, drag | — | ✅ |
| Layouts | up to 5 × 5 | 1 × 1, 1 × 2, 2 × 2 |
| Reference lines, 3D cursor | ✅ | ✅ |
| Measurements | length, angle, Cobb, ellipse, rectangle, polygon, arrow, text, ABC/2… | length |
| MIP / MinIP / average slabs | ✅ | ✅ |
| Cine | ✅ | ✅ |
| DSA (mask, auto pixel shift) | ✅ manual + automatic shift | ✅ automatic shift |
| MPR (oblique) | ✅ | ✅ |
| 3D volume rendering, colour curves, presets | ✅ | ✅ |
| Bone colour lock | ✅ | ✅ |
| Rim filter (tumour vs. vessel walls) | ✅ | ✅ |
| Crop box, scalpel | ✅ | ✅ |
| 3D snapshots | ✅ | ✅ |
| Collage (one 5 × 5 / 4 × 4 / 4 × 3 image, one slice every N mm) | ✅ | ✅ |
| 3D fly-through movie (GIF / PNG) | ✅ | — |
| 3D measurements | ✅ | — |
| Tumour segmentation, volume in ml, STL export | ✅ | — |
| DTI (FA / MD maps, tractography) | ✅ | — |
| Fusion (overlay series) | ✅ | — |
| Anonymous display (hide patient identity) | ✅ | — |
| Several patients in separate windows | ✅ | — |
| Runs without a graphics card | ✅ (software OpenGL) | needs WebGL 2 for 3D |

## Getting started

1. **Open a study**: tap *Open* and choose files, a folder or a .zip archive — or drag them onto the page on a
   computer. On iPad / iPhone pick the files from *Files* (iCloud Drive, a USB stick, or a folder you copied there).
2. **Browse**: the series list on the left shows each series as a thumbnail; tap one to show it. Drag up / down to
   scroll through the images, or use the *Window*, *Zoom* and *Pan* tools; pinch with two fingers to zoom.
3. **Layout and reference lines**: choose 1 × 2 or 2 × 2 and put a series in each viewport; *Reference lines* shows
   where each viewport's slice cuts the others.
4. **MPR / 3D**: open the active series in MPR or 3D from the toolbar. Back to the series returns to 2D.
5. The *About* menu has the quick guide, privacy notes, memory use and keyboard shortcuts.

## Features in detail

### Loading
- DICOM files, whole folders and .zip archives; non-image and DICOMDIR files are skipped automatically.
- Series assembled from DICOM position and orientation; multi-frame runs are one series each.
- Compressed transfer syntaxes decoded in a Web Worker with WebAssembly codecs (libjpeg-turbo, CharLS, OpenJPEG).

### 2D viewing
- Window / level by dragging, presets, *Auto (1–99 %)*, invert; fit to window by double tap.
- MIP 5 / 10 / 20 / 40 mm, MinIP 10 mm and average 5 / 10 mm slabs.
- Length measurement (L) with movable end points; delete one or all on the image.
- Cine play / pause (Space) at the run's own frame rate.

### DSA
- Subtraction on / off, *Use displayed image as mask*, *Reset mask*, and *Auto pixel-shift* to correct patient motion.
- The mask is taken from the scanner's Mask Subtraction Sequence when present.

### Layouts and reference lines
- 1 × 1, 1 × 2 and 2 × 2; reference lines between series in the same frame of reference; 3D cursor (*Locate*).

### MPR
- Sagittal, coronal and axial planes (all three or one at a time), tiltable axes, slab MIP, reset axes.

### 3D volume rendering
- WebGL 2 ray casting; VR with colour curves, MIP and MinIP.
- Built-in presets: CT bone, CT angio (vessels only, vessels + bone, arteries / veins + bone), enhancing lesion /
  tumour, skin + bone, muscle + vessels + bone, lung, and a generic MR preset; your own presets are kept in the
  browser and can be exported to or imported from the desktop app.
- Bone colour lock, rim filter (*Rim threshold*), crop box, scalpel (keep inside or outside the lasso, undo),
  snapshots you can tap to return to a view.

## Requirements

| | |
|---|---|
| iPad / iPhone | a recent iPadOS / iOS with Safari (WebGL 2 is available from iOS 15) |
| Computer | a current Chrome, Edge, Safari or Firefox |
| 3D and MPR | WebGL 2 (all current browsers) |
| Memory | large CT studies in 3D need a device with plenty of RAM; an iPad with 4 GB or more is recommended |

## Privacy

- All DICOM processing runs inside the browser. Images are **never uploaded**; the app makes no network requests
  except loading itself, and sends no analytics.
- A strict Content-Security-Policy only allows the app's own files.
- Colour presets you save are kept in the browser's local storage on that device.

## About this repository

This repository holds only the **built** web app, published with GitHub Pages at
<https://trithonese.github.io/SoEasy-DICOM-Web/>. The desktop application, its source code, documentation,
screenshots and issue tracker live in **[SoEasy DICOM Viewer](https://github.com/TrithoneSE/SoEasy-DICOM-Viewer)**.

Please report problems there and do **not** attach patient images or DICOM files to issues.
