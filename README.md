# 🧰 PPT Toolbox

> **A powerful, browser-based PowerPoint utility toolbox for creating, editing, and managing PPTX presentations.**

PPT Toolbox is a lightweight, modern web application that provides useful PowerPoint operations directly inside your browser.

Create presentations, convert images into slides, merge PPTX files, remove slides, reorder slides, and inspect presentation information — **without Python, a server, or external libraries.**

The entire application runs locally in the browser.

---

## ✨ Features

- 📊 **Create PPT**
- 🖼️ **Images → PPT**
- 🧩 **Merge PPTs**
- 🗑️ **Remove Slides**
- 🔀 **Reorder Slides**
- 📄 **PPT Info**
- 🖱️ **Visual file selection**
- ⚡ **100% browser-based processing**
- 🔒 **No server required**
- 🌐 **Works offline**
- 📦 **Direct PPTX generation**
- 🎨 **Modern dark purple glass-style UI**
- 📱 **Responsive interface**
- 🚀 **Simple HTML launcher**

---

# 🖥️ User Interface

PPT Toolbox uses a clean task-based interface where each PowerPoint operation is available as a separate card.

```text
┌─────────────────────────────────────────────────────┐
│                                                     │
│                  🧰 PPT TOOLBOX                     │
│                                                     │
│       100% Browser • Works Offline • No Server      │
│                                                     │
│  ┌──────────────┐    ┌──────────────┐              │
│  │ 📊           │    │ 🖼️           │              │
│  │ Create PPT   │    │ Images → PPT │              │
│  └──────────────┘    └──────────────┘              │
│                                                     │
│  ┌──────────────┐    ┌──────────────┐              │
│  │ 🧩           │    │ 🗑️           │              │
│  │ Merge PPTs   │    │ Remove Slides│              │
│  └──────────────┘    └──────────────┘              │
│                                                     │
│  ┌──────────────┐    ┌──────────────┐              │
│  │ 🔀           │    │ 📄           │              │
│  │ Reorder      │    │ PPT Info     │              │
│  └──────────────┘    └──────────────┘              │
│                                                     │
└─────────────────────────────────────────────────────┘
```

The available tools are implemented directly in the HTML application.

---

# 🚀 Quick Start

## 1. Clone the Repository

```bash
git clone https://github.com/rsamwilson2323-cloud/PPT_TOOLBOX.git
```

Enter the project:

```bash
cd PPT_TOOLBOX
```

---

## 2. Open PPT Toolbox

The application is a standalone HTML file.

Open:

```text
PPT_TOOLBOX_BROWSER.html
```

using:

- Google Chrome
- Microsoft Edge
- Firefox
- Any modern browser with the required browser APIs

No Python installation is required.

No Node.js installation is required.

No server setup is required.

---

# 📊 Available Tools

## 1. 📊 Create PPT

Create a PowerPoint presentation directly in your browser.

You can add multiple slides containing:

- Slide title
- Slide text
- Multiple paragraphs

### Workflow

```text
Create PPT
    ↓
Enter Slide Title
    ↓
Enter Slide Text
    ↓
Add Slide
    ↓
Repeat
    ↓
Download PPTX
    ↓
PPT_Toolbox_Presentation.pptx
```

Each generated presentation is a real `.pptx` PowerPoint file.

---

# 🖼️ 2. Images → PPT

Convert selected images into a PowerPoint presentation.

Multiple images can be selected at once.

Supported image processing includes common browser image formats such as:

```text
JPG
JPEG
PNG
```

Each image becomes one PowerPoint slide.

The images are automatically fitted into a **16:9 presentation layout**.

### Example

```text
photo1.jpg
photo2.jpg
photo3.png
      ↓
Images → PPT
      ↓
Images_Presentation.pptx
```

---

# 🧩 3. Merge PPTs

Combine two or more `.pptx` presentations into one presentation.

The files are merged in the order selected.

### Example

```text
presentation-1.pptx
presentation-2.pptx
presentation-3.pptx
        ↓
    Merge PPTs
        ↓
Merged_Presentation.pptx
```

The application works directly with the internal PPTX package structure to combine presentations.

---

# 🗑️ 4. Remove Slides

Remove selected slides from an existing PPTX file.

You can enter individual slide numbers or ranges.

### Examples

```text
2
```

Remove slide 2.

```text
2,5,7
```

Remove slides 2, 5, and 7.

```text
7-9
```

Remove slides 7 through 9.

```text
2,5,7-9
```

Remove multiple individual slides and ranges.

### Workflow

```text
Choose PPTX
     ↓
Enter slide numbers
     ↓
Remove & Download
     ↓
presentation_edited.pptx
```

The application prevents removing every slide from a presentation.

---

# 🔀 5. Reorder Slides

Change the order of slides in an existing presentation.

Enter the complete new slide order.

### Example

Original:

```text
1
2
3
4
```

Enter:

```text
3,1,4,2
```

Result:

```text
3
1
4
2
```

### Workflow

```text
Choose PPTX
     ↓
Enter New Slide Order
     ↓
Reorder & Download
     ↓
presentation_edited.pptx
```

The application validates that every slide is included exactly once.

---

# 📄 6. PPT Info

Inspect information about a PowerPoint presentation.

The information tool can display:

- File name
- File size
- Number of slides
- Slide dimensions
- Slide masters
- Slide layouts
- Media files
- Notes
- Charts
- Slide titles
- Word counts

### Example Output

```text
File: presentation.pptx
Size: 245.8 KB
Slides: 12

Slide size:
13.33 × 7.50 in

Masters: 1
Layouts: 1
Media files: 8
Notes: 0
Charts: 2

1. Introduction (45 words)
2. Problem Statement (82 words)
3. Proposed Solution (104 words)
...
```

The application reads the PPTX package and extracts presentation metadata directly in the browser.

---

# 📦 PPTX Processing

PPTX files are essentially ZIP-based Office Open XML packages.

PPT Toolbox contains its own browser-side ZIP reader and writer for processing these packages.

```text
PPTX File
   ↓
ZIP Package
   ↓
PowerPoint XML Parts
   ↓
Modify / Analyze
   ↓
Rebuild ZIP
   ↓
New PPTX
```

The project directly handles PowerPoint presentation XML, relationships, slide masters, layouts, media, and content types.

---

# ⚡ Browser-Only Architecture

PPT Toolbox is designed to run completely inside the browser.

```text
┌───────────────────────────────┐
│        Your Computer          │
│                               │
│       Web Browser             │
│            │                  │
│            ▼                  │
│      PPT TOOLBOX              │
│            │                  │
│     ┌──────┴──────┐           │
│     │             │           │
│     ▼             ▼           │
│  Read PPTX     Create PPTX    │
│     │             │           │
│     └──────┬──────┘           │
│            ▼                  │
│       Download File           │
│                               │
└───────────────────────────────┘
```

There is:

```text
❌ No Python
❌ No Node.js
❌ No backend server
❌ No database
❌ No API
❌ No cloud upload
❌ No external library dependency
```

The interface itself identifies the application as **100% Browser • Works Offline • No Server • No Libraries**.

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| 🌐 HTML5 | Application structure |
| 🎨 CSS3 | UI and responsive design |
| ⚡ JavaScript | Application logic |
| 📦 ZIP Processing | PPTX package reading/writing |
| 📄 XML DOM APIs | PowerPoint XML manipulation |
| 🖼️ Canvas / Image APIs | Image processing |
| 🌐 Browser APIs | File access and downloads |
| 💾 Blob API | Local file generation |

---

# 📂 Project Structure

```text
PPT_TOOLBOX/
│
├── 📄 PPT_TOOLBOX_BROWSER.html
│
└── 📄 README.md
```

### `PPT_TOOLBOX_BROWSER.html`

The main application containing:

- User interface
- PPTX creation
- Image-to-PPT conversion
- PPTX merging
- Slide removal
- Slide reordering
- PPT information inspection
- ZIP processing
- XML processing
- File downloads

---

# 🔐 Privacy

PPT Toolbox is designed as a local browser utility.

Your selected PowerPoint files are processed inside the browser for the supported operations.

```text
Your Computer
      │
      ▼
┌─────────────────────┐
│    Web Browser      │
│                     │
│  Select PPTX        │
│       ↓             │
│  Process Locally    │
│       ↓             │
│  Generate PPTX      │
│       ↓             │
│  Download Result    │
└─────────────────────┘
```

No project-specific backend server is required.

---

# 🌐 Offline Support

Unlike web applications that depend on online APIs or CDN libraries, PPT Toolbox is designed to operate without external libraries.

This makes it suitable for:

- Offline environments
- College labs
- Personal computers
- Restricted networks
- Local document processing

> **Internet access is not required for the core application after the HTML file has been obtained.**

---

# 💻 Requirements

### Windows

- Windows 10 / 11
- Modern web browser

Recommended:

- Google Chrome
- Microsoft Edge

### Other Platforms

The HTML application can also be opened on other desktop operating systems with a modern browser.

No:

```text
Python
Node.js
npm
PowerPoint installation
Server
Database
```

is required for the browser application.

---

# 🧪 Example Workflow

Suppose you have:

```text
Project_Introduction.pptx
Project_Methodology.pptx
Project_Results.pptx
```

Choose:

```text
🧩 Merge PPTs
```

Then:

```text
Select Files
      ↓
Project_Introduction.pptx
Project_Methodology.pptx
Project_Results.pptx
      ↓
Merge & Download
      ↓
Merged_Presentation.pptx
```

---

# 🎨 Design

PPT Toolbox uses a modern dark interface with a purple glass-style design.

### Design Goals

- Clean
- Modern
- Minimal
- Beginner-friendly
- Fast
- Responsive
- Easy navigation
- Simple controls

The UI uses glass-style cards, purple accents, rounded controls, and a dark background.

---

# 🔮 Future Improvements

Possible future features:

```text
□ PowerPoint → PDF
□ PowerPoint → Images
□ Slide preview thumbnails
□ Duplicate slides
□ Rotate slides
□ Delete individual slide objects
□ Edit existing slide text
□ Add images to existing slides
□ Add shapes
□ Add tables
□ Add charts
□ Add speaker notes
□ Presentation metadata editor
□ Theme editor
□ Custom slide sizes
□ Template support
□ Drag-and-drop slide ordering
□ Batch processing
□ Desktop EXE version
□ Mobile-optimized version
```

---

# 🚀 Roadmap

## Version 1.0

```text
✓ Modern PPT Toolbox UI
✓ Create PPT
✓ Images → PPT
✓ Merge PPTs
✓ Remove Slides
✓ Reorder Slides
✓ PPT Information
✓ Browser-based processing
✓ Offline operation
✓ No external libraries
```

## Version 2.0

```text
□ Slide preview
□ Advanced slide management
□ PowerPoint → PDF
□ PowerPoint → Images
□ Duplicate slides
□ Presentation templates
□ Metadata tools
```

## Version 3.0

```text
□ Advanced PowerPoint editor
□ Drag-and-drop slide builder
□ Presentation themes
□ Batch processing
□ Standalone Windows EXE
□ Cross-platform desktop application
□ Advanced presentation automation
```

---

# 👨‍💻 Author

## Sam Wilson

**B.E. CSE — Artificial Intelligence & Machine Learning**

GitHub:

https://github.com/rsamwilson2323-cloud

---

# ⭐ Repository

## PPT_TOOLBOX

https://github.com/rsamwilson2323-cloud/PPT_TOOLBOX

If you find this project useful, consider giving the repository a ⭐.

---

# 📜 License

This project is released under the **MIT License**.

See the `LICENSE` file for details.

---

# ⚡ Quick Start

```bash
git clone https://github.com/rsamwilson2323-cloud/PPT_TOOLBOX.git

cd PPT_TOOLBOX
```

Then open:

```text
PPT_TOOLBOX_BROWSER.html
```

Choose a PowerPoint task, select your files, process them locally, and download the result.

---

# 📊 PPT → ⚡ Process → 💾 Download

**Simple. Fast. Private. Browser-based.**

---

## 🔗 Repository

**GitHub:**  
https://github.com/rsamwilson2323-cloud/PPT_TOOLBOX
