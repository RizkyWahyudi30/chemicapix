# ChemicaPix - Apps Helping You Convert Any Files

Convert hundreds or thousands of images into a single PDF directly in your browser.

This tool allows users to upload a ZIP file containing images (such as WEBP, JPG, or PNG) and convert them into a single ordered PDF without uploading files to any server.

All processing happens locally in your browser.

---

## Background, Problem, and Solution

| Background | Problem | Solution |
|------------|---------|----------|
| Many websites display content such as manga or documents as **one image per page** | Users often download **hundreds of separate image files** which are difficult to read offline | This tool converts a collection of images into **one organized PDF file** |
| Downloaded content is frequently packaged as a **ZIP file containing images** | Extracting and manually combining these images into a PDF is **time-consuming** | The application automatically **extracts images from ZIP and generates a PDF** |
| Many images are stored in **WEBP format** to reduce size | Some PDF tools **do not support WEBP images directly** | The application **converts WEBP images into compatible formats before generating the PDF** |
| Online tools usually process files on **remote servers** | Users may worry about **privacy and data security** when uploading files | This application processes files **entirely in the browser without uploads** |
| Many file conversion services have **file size limits or require subscriptions** | Large image collections may **fail to upload or require payment** | The tool works **locally in the browser with no file upload limits from a server** |

---

## Key Features

- Convert ZIP (images) → PDF
- Supports `.webp`, `.png`, `.jpg`
- Automatic image sorting
- Drag and drop upload
- Image preview
- Progress indicator
- 100% client-side processing
- No file upload
- Privacy friendly

---

## Tech Stack

- React
- Bootstrap
- JSZip
- pdf-lib
- FileSaver
- Canvas API

---

## How It Works

Processing pipeline:

1. User uploads a ZIP file
2. The application extracts images from the ZIP
3. Images are sorted by filename
4. Images are converted into compatible format
5. Images are embedded into a PDF document
6. The generated PDF is downloaded by the user

All steps run directly in the browser.

---

## Project Structure
```bash
/chemicapix
├── /src
│   ├── /components
│   │   ├── UploadArea.jsx      # Area drag-and-drop file ZIP
│   │   ├── ImagePreview.jsx    # Thumbnail hasil ekstrak gambar
│   │   ├── ProgressBar.jsx     # Indikator proses ekstraksi & konversi
│   │   ├── PageSorter.jsx      # UI untuk mengatur ulang urutan halaman
│   │   └── DownloadButton.jsx  # Tombol trigger generate PDF
│   ├── /services
│   │   ├── zipService.js       # Logika ekstraksi (e.g. JSZip)
│   │   ├── imageService.js     # Logika manipulasi/optimasi gambar
│   │   └── pdfService.js       # Logika pembuatan PDF (e.g. jsPDF)
│   ├── /hooks
│   │   └── useImageProcessor.js # Hook untuk menyatukan logika ZIP & PDF
│   ├── /utils
│   │   ├── sortImages.js       # Fungsi sorting cerdas (alfabetik/numerik)
│   │   └── fileHelpers.js      # Utility pengecekan tipe file/ukuran
│   ├── /pages
│   │   └── Home.jsx            # Layout utama aplikasi
│   ├── App.jsx                 # Provider & Router (jika ada)
│   └── main.jsx                # Entry point aplikasi
├── README.md                   # Dokumentasi proyek
├── package.json                # Daftar dependency (Vite, React, dll)
└── vite.config.js              # Konfigurasi Vite
```

---

## Installation

1. Cloning the repository :
   ```bash
   git clone https://github.com/RizkyWahyudi30/chemicapix.git
   ```
2. Enter the project directory
   ```bash
   cd chemicapix 
   ```
3. Install depedencies
   ```bash
   npm install
   ```
4. Run development server
   ```bash
   npm run dev
   ```

--- 
