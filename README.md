# Awesome-Mobile-Asset-Capture

# Top Mobile Asset Capture Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on On-Device Digitization, Barcode-Driven Inventory & Privacy-First Material Capture*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Mobile Asset Capture**. These tools turn a phone camera into a capture device for the physical world — scanning documents, inventory tags, textures, and even 3D objects — with a spectrum running from polished commercial apps like Adobe Capture and CamScanner to open-source Android tools that keep every byte on-device.

**Examples** include OpenNoteScanner, InvScan, TM 26, and xnotes (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, offline processing, and privacy-respecting mobile capture — especially relevant as **Adobe Capture's cloud-first model** pushes privacy-conscious users toward on-device alternatives like **TM 26** for texture capture and **InvScan** for inventory OCR [citation:23][citation:1].

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Adobe Capture** — **The reference commercial asset capture app.** Turns photos into vector shapes, color themes, materials, and 3D textures, with Creative Cloud sync. **Free with Adobe account; premium features require subscription**. **Trade-offs**: cloud-first architecture, account required, and output locked to Adobe formats [citation:2][citation:8]. **Best for Adobe subscribers** wanting seamless integration with Illustrator and Photoshop, accepting cloud dependency.

- **CamScanner** — **The widely-installed document scanner.** Edge detection, OCR, and PDF export with cloud backup. **Free tier with watermark and ads; paid Pro**. **Trade-offs**: historical data-harvesting controversies have driven privacy-conscious users to open-source alternatives. **Best for users** already invested in its ecosystem, though open-source options now match its core features without the privacy trade-off.

- **Microsoft Lens** — **The Office-integrated scanner.** Captures documents, whiteboards, and business cards with on-device OCR for some functions and OneDrive/Office integration. **Free with Microsoft account**. **Best for Microsoft 365 users** wanting scans that flow directly into Word, PowerPoint, or OneDrive.

- **Genius Scan** — **The all-round commercial scanner.** On-device edge detection, perspective correction, and OCR once upgraded. **Free tier capped at 30 pages/month; ~$5/month or ~$50 one-time unlocks offline OCR**. **Best for users** wanting polished scanning with on-device processing, accepting the free tier's monthly cap.

## Open-Source GitHub Projects

- **OpenNoteScanner** — **The minimalist Android document scanner.** **Open-source, available on F-Droid, Google Play, and Amazon App Store** [citation:5][citation:10]. **Automatic edge detection on contrasting surfaces**, **perspective correction to a 90-degree top-down view**, **QR code page template support**, and **PDF export or image sharing** [citation:5]. **Organizes scans in a local gallery**. **Requires OpenCV Manager** — the app will prompt to download it if missing [citation:5][citation:10]. **The honest caveat**: **no OCR** — it captures and corrects images but does not extract text, and the UI is functional rather than polished [citation:10]. **Best for Android users** wanting the simplest possible privacy-respecting scanner with automatic edge detection and zero cloud dependency.

- **InvScan** — **The Android inventory asset scanner with on-device OCR.** **Open-source diploma project (2022), Kotlin + Google ML Kit** [citation:1][citation:16]. **Photograph or scan an item's inventory tag** — ML Kit recognizes the number on-device, searches a remote MariaDB database via REST API, and generates an inventory report [citation:1]. **Features**: room selection, live search by inventory number, object marking during inventory sessions, and report generation saved to device storage [citation:16]. **On-device text recognition** means basic scanning does not depend on cloud services [citation:1]. **The honest caveat**: **requires a remote server** (MariaDB + PHP API) for database sync — it is not a standalone offline app, and it is a diploma project rather than a maintained product [citation:1][citation:16]. **Best for organizations** wanting a reference implementation for barcode/inventory-number capture with ML Kit OCR, accepting the server dependency.

- **TM 26** — **The portable texture instrument for PBR material capture.** **Open-source hackathon project (vanilla HTML5/CSS3/JS, Three.js)** [citation:23]. **Point your phone at any surface** — the app processes the image locally and generates **full PBR maps (Albedo, Depth, Gloss) viewable on an interactive 3D sphere**, **seamless vector patterns (SVG)**, and **digital brush kits for Procreate/Photoshop** [citation:23]. **Tactile dial controls** for fine-tuning, local archive saving, and channel diagnostics [citation:23]. **100% client-side processing** — no backend, no uploads [citation:23]. **The honest caveat**: **hackathon prototype** — not a production-hardened app, and depth generation uses luminance filtering rather than true photogrammetry [citation:23]. **Best for 3D artists and texture designers** wanting to capture real-world surfaces as PBR materials without cloud tools, accepting prototype-stage maturity.

- **xnotes** — **The handwriting-first notebook with vector PDF capture.** **Open-source (MIT), available on F-Droid** [citation:14]. **Pressure-sensitive ink** with variable-width strokes, **vector PDF import/export** (annotate a PDF and export true vector), **razor-sharp deep zoom**, **real highlighter blending**, and **every stroke stored as editable vector data** in the open `.xnote` format . **Stylus-aware**: pen and finger handled separately, with finger drawing auto-enabled on devices without a stylus . **No accounts, no telemetry, no network access** — files go through Android's Storage Access Framework . **The honest caveat**: **it is a note-taking and sketching app**, not a document scanner or texture capture tool — it captures handwritten input and PDF annotations, not camera-based assets . **Best for tablet users** wanting to capture handwritten notes and sketches as editable vector data, not for scanning physical documents.

### Additional Strong Open-Source Options

- **OSS Document Scanner** — **The Material You Android scanner with OCR and WebDAV sync.** **Open-source (Apache-2.0), Play Store and F-Droid** [citation:4][citation:15]. **Automatic edge detection**, bulk scanning, **offline Tesseract OCR** (models downloaded first), password-protected PDFs, and **sync to WebDAV, Google Drive, or OneDrive** [citation:15]. **The honest caveat**: **building from source requires NativeScript, OpenCV, and Tesseract setup** — the repo does not include the large native libraries [citation:4]. **Best for Android users** wanting a polished open-source scanner with OCR and WebDAV backup, installing via Play Store/F-Droid rather than building from source.

- **Mapilio Mobile** — **The open-source street-level imagery capture app.** **Open-source (Expo/React Native), iOS and Android** [citation:21]. **Captures street-level imagery** and contributes to the OpenStreetMap ecosystem, with offline SQLite storage and self-hosted tile service support [citation:21]. **The honest caveat**: **specialized for geospatial imagery**, not general asset capture — it is for mapping, not documents or inventory [citation:21]. **Best for mappers and researchers** needing to capture geotagged street imagery for OpenStreetMap.

- **Open Foris Arena Mobile** — **The offline field data capture app.** **Open-source, Android and iOS**, designed for **inventory surveys and field data collection** with support for numbers, coordinates, images, video, and text [citation:30]. **Configurable validation rules** for high-quality data, QR code login, and location averaging [citation:30]. **The honest caveat**: **requires an Open Foris Arena server** — it is a companion app, not a standalone capture tool [citation:30]. **Best for forestry and field survey teams** wanting structured offline data capture with server-side analytics.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Mobile asset capture tools differ significantly in capture target (documents vs inventory tags vs textures vs handwriting), processing model (on-device vs cloud), and platform support. **Adobe Capture and CamScanner are cloud-first** — they require accounts and sync data to servers [citation:2][citation:8]. **OpenNoteScanner and InvScan process on-device**, but **OpenNoteScanner lacks OCR** and **InvScan requires a remote MariaDB server** [citation:5][citation:1]. **TM 26 is a hackathon prototype** — its PBR map generation is local and impressive for a prototype, but it is not production-hardened [citation:23]. **xnotes captures handwriting and PDF annotations**, not camera-based physical assets . **The choice often comes down to target**: documents (OpenNoteScanner, OSS Document Scanner), inventory tags (InvScan), textures (TM 26), or handwritten notes (xnotes).
- Self-hosted open-source solutions require proper app installation from F-Droid or GitHub Releases, and awareness that some apps require companion servers (InvScan, Open Foris Arena) or native library setup (OSS Document Scanner) for full functionality.

---

**Made for mobile users, field workers, inventory managers, and 3D artists choosing asset capture tools that respect their data and workflow.**
Let's make mobile asset capture more open, on-device, and privacy-respecting.
