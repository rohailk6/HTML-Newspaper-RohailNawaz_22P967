# HTML-Newspaper-RohailNawaz_22P967

# HTML Newspaper Recreation — Akhbar-e-Khawateen

## Student Information
| Field | Details |
|---|---|
| **Name** | Rohail Nawaz |
| **Roll Number** | 22P-9367 |
| **Section** | A |
| **Course** | CS-4070 Web Technologies — 8th Semester |

---

## Original Newspaper
| Field | Details |
|---|---|
| **Name** | اخبارِ خواتین (Akhbar-e-Khawateen — Women's Weekly) |
| **Date** | Thursday, 14 March 1974 |
| **Publisher** | Pakistan Women's Press Trust, Lahore |
| **Source** | Private archive scan (750 issues of Akhbar-e-Khawateen 1964–1986) |

---

## Project Description
This project is an HTML-only recreation of a 1974 page from *Akhbar-e-Khawateen*, a prominent Pakistani women's weekly newspaper published from Lahore. The original page features a dense multi-column layout with black-and-white photographs, traditional typography, and period advertisements including the Olivia Acne Cream ad. The recreation uses HTML tables for column layout and HTML5 semantic tags throughout, with all styling applied exclusively via inline `style` attributes — no external CSS files and no JavaScript are used anywhere in the project.

---

## Repository Structure
```
HTML-Newspaper-RohailNawaz_22P9367/
├── index.html                              ← Main HTML file (793 lines)
├── README.md                               ← This file
├── HTML-Newspaper-RohailNawaz_22P9367.pdf  ← 1-page code explanation
└── images/
    ├── original-newspaper.png              ← Scan of the original newspaper page
    ├── singer-portrait.png                 ← Main portrait photo (center column)
    ├── needlework-prize.png                ← Right column article photo
    ├── olivia-ad.png                       ← Olivia cream advertisement image
    └── mosque-article.png                  ← Bottom-left mosque photograph
```

---

## Features Implemented

### HTML5 Structure
- Proper `<!DOCTYPE html>` declaration with `lang="en"`
- Complete `<head>` with UTF-8 charset and viewport meta tag
- Semantic document flow: `<header>` → `<nav>` → `<main>` → `<footer>`

### Semantic Tags Used
| Tag | Where Used |
|---|---|
| `<header>` | Newspaper masthead (name, tagline, date, price) |
| `<nav>` | Section labels bar |
| `<main>` | All article content |
| `<article>` | 7 individual articles across both table layouts |
| `<section>` | "This Week Inside" list and Olivia advertisement |
| `<figure>` + `<figcaption>` | Singer portrait with caption |
| `<footer>` | Editor info, address, copyright |

### Layout
- **6 `<table>` elements** total for newspaper-style column grids:
  - 1 table inside `<header>` for Vol / Date / Price row
  - 1 top-level 3-column table (Left 28% / Center 44% / Right 28%)
  - 2 nested sub-tables inside articles for internal 2-column text layout
  - 1 bottom 2-column table for lower page content
  - 1 table in `<footer>` for editor / address / price columns
- `vertical-align: top` on all `<td>` cells to match newspaper column alignment

### Heading Hierarchy
- `<h1>` — Newspaper masthead name
- `<h2>` — Lead article headlines and section headlines
- `<h3>` — Sub-headlines, decks, and article subheadings
- `<h4>` — Box headings (This Week Inside, Advertisement)

### Images
- **4 images**, all `.png` format, all in the `images/` folder
- Every `<img>` tag has a descriptive `alt` attribute
- `filter: grayscale(100%)` inline style applied to all photos for authentic B&W newsprint look

### Lists
- `<ul>` list in the "This Week Inside" section (6 items)

### Comments
- **41 HTML comments** explaining every major section, column, article, and design decision

### Inline Styling Only
- Zero `.css` files in the repository
- Zero `<script>` tags or `.js` files
- All formatting uses the `style=""` attribute directly on HTML elements

---

## Visual Design Choices
| Decision | Reason |
|---|---|
| `background-color: #ede0c0` | Mimics aged newsprint/sepia paper colour |
| `font-family: Times New Roman` | Matches traditional newspaper typography |
| `filter: grayscale(100%)` on images | Replicates black-and-white newspaper photos |
| `border: 6px solid #111` on header | Bold masthead border typical of 1970s Pakistani newspapers |
| Purple circle `border-radius: 50%` with `#3b1f5e` | Recreates the distinctive purple printed circle from the original scan |
| `3px double` borders as section dividers | Matches the double-rule dividers used in the original newspaper columns |

---

## Challenges Faced
Replicating a dense multi-column newspaper layout using only HTML tables — without flexbox, grid, or any CSS file — required carefully setting percentage widths on `<td>` elements and ensuring `vertical-align: top` was applied consistently; without it, columns defaulted to middle alignment and broke the newspaper appearance. A second challenge was recreating the distinctive printed purple circle from the original scan, which was solved using `border-radius: 50%` combined with a fixed width percentage and inline padding, with no image required.

---

## HTML Validation
Validated at [https://validator.w3.org/](https://validator.w3.org/) — passes with **0 critical errors**.

---

## Resources Used
- [MDN Web Docs — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools HTML Tables](https://www.w3schools.com/html/html_tables.asp)
- [W3C HTML Validator](https://validator.w3.org/)
- Original newspaper: *Akhbar-e-Khawateen*, Lahore, 1974 (private archive scan)
