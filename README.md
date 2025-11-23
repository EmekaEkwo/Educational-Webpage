# Beginner's Guide to Small-Sided Soccer ⚽  

This two-page site is my small-sided soccer guide for beginners. It started as a basic HTML project and has been improved over time for accessibility, responsiveness, and now Bootstrap integration.

---

## Accessibility & Responsiveness (Assignment #4)

For Assignment 4, I focused on making the site easier to use and more inclusive.

### What Changed for A11y
- Added a **“Skip to main content”** link so keyboard users can jump straight into the page.
- Cleaned up the heading structure (one `<h1>` per page, clear `<h2>` sections).
- Wrote **descriptive `alt` text** for images instead of generic labels.
- Turned on **visible `:focus-visible` outlines** to show where keyboard focus is.
- Chose **high-contrast colors** and made sure links are easy to see and understand.
- Used **semantic landmarks** like `header`, `main`, `footer`, and `nav` with `aria-label` where it made sense.

### Responsive Design
- Added a **mobile media query** at `max-width: 640px` to:
  - Stack sections vertically on smaller screens
  - Let images scale down instead of overflowing
  - Adjust spacing so text stays readable on a phone

### Accessibility Audit (BEFORE & AFTER)
To document the improvements, I used a browser accessibility audit:

1. Opened `index.html` using Live Server in VS Code.
2. Ran an audit on the page and saved a **before** screenshot.
3. Fixed the issues mentioned above (headings, focus styles, alt text, etc.).
4. Ran the audit again and saved an **after** screenshot.
5. Stored the screenshots in the `audits/` folder as `before.png` and `after.png`.

---

## Bootstrap Integration (Assignment #5)

For Assignment 5, the goal was to integrate **Bootstrap** and clean up my existing CSS so they work together instead of clashing.

### How I Added Bootstrap
- Linked the **Bootstrap 5 CSS CDN** in the `<head>` of both `index.html` and `page2.html`, **above** `css/style.css`.
- Included the **Bootstrap JS bundle** at the bottom of each page so interactive components are available if I want to add them later.

### Where I Used Bootstrap on the Pages
- Wrapped major sections in `.container` and used `.row` + `.col-*` classes to organize content instead of relying on my own flexbox layout.
- Upgraded important links into **Bootstrap buttons**, for example the navigation link to Page 2 and the “Back to Home” button.
- Applied common **utility classes**:
  - Spacing: `py-4`, `my-4`, `mb-3`, `mb-4`
  - Layout: `d-flex`, `justify-content-between`, `align-items-center`
  - Typography: `lead`, `fw-bold`, `text-muted`
  - Images: `img-fluid`, `rounded`, `shadow-sm`
- Used a **card component** on the second page to highlight the main skills section in a more structured way.

### Refactoring My Custom CSS
Once Bootstrap was in place, some of my older CSS became redundant:

- I **commented out** my custom `.container` and layout helper classes (`.flex-row`, `.gap-lg`, `.stack-md`), since Bootstrap now handles those roles.
- I kept the parts of `style.css` that still matter for my design:
  - Color variables (brand colors, focus rings)
  - Typography tweaks
  - The skip link
  - Focus outlines
  - Minor card and footer polish
- The new comment at the top of `style.css` explains that this file is now focused on **layering custom styles on top of Bootstrap**, instead of trying to replace it.

Overall, the final result is a blend of:
- Bootstrap’s layout and utility classes  
- My own soccer-specific content and styling choices  
- The accessibility and responsiveness work from previous assignments  

It still feels like my site, but it’s structured more like something you’d see in a professional front-end codebase.
