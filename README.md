# Myntra HackerRamp — Fashion Store & Try‑On Prototype

A simple, beginner‑friendly prototype for a fashion e‑commerce experience. The repository contains static web pages (HTML/CSS) for browsing products and brand sections, plus a small webcam script that can be used as a basis for a try‑on/camera demo.

> This README is based on the files present in the repository (HTML/CSS assets and a `webcam.py` script). The web portion runs as a static site; the webcam script is optional.

---

## Features

* **Multi‑page frontend** built with plain HTML/CSS:

  * `index.html` – Home/landing page
  * `shop.html` – Shop/catalog page
  * `iconic.html` – Iconic/brand section
  * `page.html` – Auxiliary/product page
  * `tryon.html` – Try‑on demo page
  * `avatar.html` – Avatar/intro demo (includes `avatar.mp4`)
* **Clean styling** via `styles.css` and `layout.css`.
* **Image/product assets** organized under `images/`, `clothes/`, and `iconic/`.
* **Optional camera demo** via `webcam.py` (local webcam preview/try‑on prototype).
* No frameworks or build tools required — easy to run locally.

---

## Installation

> You only need a web browser to view the static site. For the optional camera demo, install Python 3.

### 1) Clone the repository

```bash
git clone https://github.com/Riyabachheti/myntra_hackerramp.git
cd myntra_hackerramp
```

### 2) (Recommended) Serve the site locally

Running a tiny local server avoids CORS/camera permission issues some browsers enforce for `file://` pages.

**Option A — Python 3 built‑in server**

```bash
# from the repo root
python -m http.server 8000
# then open http://localhost:8000/ in your browser
```

**Option B — VS Code Live Server**

* Install the **Live Server** extension
* Right‑click `index.html` → **Open with Live Server**

### 3) (Optional) Set up the webcam demo

If you plan to run `webcam.py`, create a virtual environment and install dependencies:

```bash
python -m venv .venv
# Windows PowerShell
. .venv\Scripts\Activate.ps1
# macOS/Linux
source .venv/bin/activate

# likely dependencies for webcam access
pip install opencv-python
```

> If `webcam.py` imports additional libraries on your machine, install them with `pip install <package>` and re‑run.

---

## Usage

### Web UI (static site)

* Start your local server (see Installation) and open:

  * `http://localhost:8000/index.html` — landing page
  * `http://localhost:8000/shop.html` — product grid
  * `http://localhost:8000/iconic.html` — brand/collection
  * `http://localhost:8000/page.html` — supporting page
  * `http://localhost:8000/tryon.html` — try‑on demo page
* Browse pages and images. Styling is handled by `styles.css`/`layout.css`.

### Webcam demo (optional)

Run the Python script from the repository root:

```bash
python webcam.py
```

Common tips:

* Allow camera permissions if prompted by your OS/browser.
* Press `q` in the terminal/window to quit (typical OpenCV behavior). If your script uses a different key, update here as needed.

---

## Configuration

This prototype has **no required environment variables** or external configuration files.

You may customize:

* **Images & products**: Replace assets inside `images/`, `clothes/`, and `iconic/`.
* **Styles**: Edit `styles.css` and `layout.css` for colors, spacing, and layout.
* **Try‑on behavior**: Modify `tryon.html` (browser‑based) or `webcam.py` (Python script) to change camera handling.

> Browser camera APIs generally require HTTPS or `http://localhost`. Serving the site locally (rather than opening files via `file://`) is recommended.

---

## Folder Structure

```
myntra_hackerramp/
├── .vscode/             # editor settings (optional)
├── clothes/             # product images/assets
├── iconic/              # iconic/brand assets
├── images/              # shared images
├── avatar.html          # avatar/intro page
├── avatar.mp4           # video asset used by avatar.html
├── iconic.html          # brand/collection page
├── index.html           # landing page (entry point)
├── layout.css           # layout stylesheet
├── page.html            # auxiliary/product page
├── shop.html            # shop/catalog page
├── styles.css           # base stylesheet
├── tryon.html           # try‑on demo page
└── webcam.py            # optional webcam/camera demo script
```

---
