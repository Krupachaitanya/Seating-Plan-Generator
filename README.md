# Seating Plan Generator

Seating Plan Generator is a small React + TypeScript app (Vite + Tailwind) to manage students and rooms, generate seating arrangements and printable signature lists / notices. It includes responsive UI with a mobile hamburger nav, smooth animations, Excel bulk uploads, export-to-PDF/HTML flows and simple pagination (first 15 rows shown with Next/Prev).
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7c9a083b-c1d8-4d0e-88a3-ac19a09c2882" />

Repository: https://github.com/Krupachaitanya/Seating-Plan-Generator.git

Contact
- Email: chaitu25113@gmail.com
- Phone: +91 9381900979

Logo: https://i.ibb.co/ZRrgvN1Q/logg.jpg

---

## Key features
- Manage students and rooms (add, delete, bulk upload via Excel)
- Pagination (shows first 15 records per page, Next / Prev buttons)
- Generate seating plans per room and export HTML / PDF
- Generate signature lists (paginated per room) and export PDF/HTML
- Notice / schedule printing optimized for A4
- Responsive UI with mobile hamburger navigation and footer
- Smooth animations via Tailwind CSS transitions

---

## Project structure (important files)
- index.html — app entry
- src/
  - main.tsx — React bootstrap
  - App.tsx — top-level layout, nav, footer
  - index.css — Tailwind imports
  - components/
    - StudentsManager.tsx — add, upload, list (pagination = 15 / page)
    - RoomsManager.tsx — add, upload, list (pagination = 15 / page)
    - SeatingPlanGenerator.tsx — generate and export seating plans
    - SignatureListGenerator.tsx — generate and export signature lists
    - NoticeScheduleGenerator.tsx — printable notice/schedule
  - lib/
    - supabase.ts — supabase client + types
- supabase/
  - migrations/ — DB schema SQL
- tailwind.config.js, postcss.config.js, vite.config.ts

---

## Quick start (Windows)
1. Clone
   git clone https://github.com/Krupachaitanya/Seating-Plan-Generator.git

2. Install
   npm install

3. Add environment variables (project root `.env`)
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_anon_key

   (A sample .env is already present for development — verify keys before publishing.)

4. Run dev server
   npm run dev
   Open http://localhost:5173

5. Build for production
   npm run build

6. Preview build (local)
   npm run preview

---

## Usage notes
- Students and rooms can be bulk uploaded from Excel (.xlsx/.xls). Expected column headers for students: `ROLL NO`, `Name of the Student`, `Section`. For rooms: `Room Numbers`, `No of Benches`, `Size`.
- Pagination shows the first 15 items (page size = 15). Use Next / Prev to navigate pages.
- Exports use html2pdf.js for generating downloadable PDFs from generated HTML pages.
- Signature list generation paginates rows for printing (configurable rows per page inside the component).

---

## Advantages
- Lightweight: Vite + React + TypeScript for fast dev and builds
- Tailwind CSS for responsive layouts and smooth transitions
- Excel import simplifies large dataset entry
- Print-ready HTML templates tuned for A4 (portrait & landscape)
- Simple Supabase integration for full cloud DB (no backend to host)
- Mobile-first UX with hamburger menu and footer

---

## Icons & 3D models (recommended)
Use lightweight icon libraries and free 3D model sources:
- Icons: Lucide (already used), Heroicons, Feather, Font Awesome (CDN / npm)
- 3D models / viewers (if you plan to add 3D file previews):
  - Sketchfab (embed viewer) — https://sketchfab.com
  - Google Poly alternatives / free assets: https://poly.pizza or https://free3d.com
  - Use three.js + glTF models for interactive previews (glTF recommended)
- For file-type icons (documents, pdf, xlsx) use SVG icons from Heroicons / Lucide for fast load.

---

## Security & privacy
- Keep Supabase anon key safe for deployed apps — rotate keys if exposed.
- Do not commit production keys to git. Use environment variables / secrets.

---

## Troubleshooting
- Styles missing? Ensure Tailwind build step is active and PostCSS is configured.
- Excel upload errors? Verify expected header names and file format (.xlsx/.xls).
- Supabase errors? Check .env values and network connectivity to your Supabase project.

---

If you want, I can:
- Add a downloadable README to the repo (I can create README.md in your project).
- Add sample SVG icons or a small 3D preview using three.js.
- Add a configuration section to adjust pagination size and rows-per-signature-page.
