# Beginner's Guide to Small-Sided Soccer ⚽
Accessibility & Responsiveness (Assignment #4)

This two–page educational website is updated to improve **accessibility** and **responsive design**.

## What Changed for A11y
- Added a **skip link** to jump to main content.
- Ensured **one `<h1>` per page** and logical `<h2>` structure.
- Verified **descriptive `alt` text** on images.
- Added **visible `:focus-visible` outlines** for keyboard navigation.
- Chose **high-contrast colors** and underlined links.
- Used **semantic landmarks** (`header`, `main`, `footer`, `nav` with `aria-label`).

## Responsive Design
- Added a **mobile media query** at `max-width: 640px` to:
  - Stack flex rows vertically
  - Scale images
  - Adjust padding/spacing for readability

## Run an Accessibility Audit (You will submit BEFORE and AFTER screenshots)
You can use **Lighthouse** (Chrome) or **WAVE** (extension).
1. Open `index.html` in your browser (or Live Server in VS Code).
2. **BEFORE**: Run an audit and take a screenshot of the Accessibility section.
3. Fix any errors (already addressed here).  
4. **AFTER**: Run again and take a screenshot.
5. Save the images in `audits/` and name them `before.png` and `after.png`.

## Project Structure
```
.
├── index.html
├── page2.html
├── css/
│   └── style.css
├── images/
│   └── 3v3-field-zones.jpg  (add your image here)
└── audits/
    ├── before.png  (your screenshot)
    └── after.png   (your screenshot)
```

## How to View Locally
```bash
# clone
git clone https://github.com/EmekaEkwo/Educational-Webpage.git
cd Educational-Webpage

# serve (optional)
# in VS Code, right-click index.html → 'Open with Live Server'
```

## Suggested Commit Flow
```bash
git add .
git commit -m "feat(a11y): add skip link, focus styles, semantic landmarks"
git commit -m "style(responsive): add mobile media query and layout tweaks"
git commit -m "docs: update README with audit instructions"
git push
```
