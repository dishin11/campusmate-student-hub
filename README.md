# CampusMate – Student Resource Hub

A simple, responsive website that brings the resources a college student needs into one place: academic material, student clubs, career opportunities and wellbeing support.

Built with **HTML5 and CSS3 only** — no JavaScript, no frameworks, no build step.

**Live site:** https://dishin11.github.io/campusmate-student-hub/

---

## Why I built this

College students look for notes, clubs, internships and support across many different
platforms and WhatsApp groups. Information exists, but it is scattered, and first-year
students often do not know where to start.

CampusMate is a single organised starting point: one page, clear sections, and links to
resources that are actually useful.

## Features

| Section | What it does |
| --- | --- |
| **Academic Support** | Links to free learning platforms (NPTEL, SWAYAM, MIT OpenCourseWare, Khan Academy) for notes, revision and second explanations. |
| **Clubs & Communities** | Explains the kinds of campus communities available and links to open-source and hackathon platforms. |
| **Career Growth** | Internship listings, coding practice, portfolio hosting and free project-based learning. |
| **Student Wellbeing** | Counselling guidance, a national mental health helpline, and stress-management resources. |
| **FAQs** | An expandable accordion answering common questions — built with `<details>` and `<summary>`, so it works without JavaScript. |
| **Navigation** | In-page anchor links in the sticky header and footer, plus a skip link for keyboard users. |

## Pages and files

```
campusmate-student-hub/
├── index.html   → page structure and all content
├── style.css    → design, layout, responsive rules
└── README.md    → this file
```

## How it was built

- **Semantic HTML5** — `header`, `nav`, `main`, `section`, `article`, `footer`, with a
  logical heading order.
- **CSS custom properties** (design tokens) for colours, spacing and radius, so the theme
  is changed in one place.
- **CSS Grid** for card layouts, using `auto-fit` + `minmax()` so cards reflow without
  media queries.
- **Media queries** at 900px, 720px and 480px for tablet and mobile.
- **`<details>` / `<summary>`** for the FAQ accordion — the interactive part of the page
  with zero JavaScript.
- **Accessibility basics** — skip link, visible `:focus-visible` outlines, `aria-label`
  on navigation, decorative emoji hidden from screen readers, and
  `prefers-reduced-motion` support.

## Run it locally

1. Download or clone the repository.
2. Double-click `index.html` — it opens in your browser. No installation needed.

To work on it in an editor, open the folder in VS Code and use the **Live Server**
extension for auto-reload.

## Deploy with GitHub Pages

1. Push all files to the `main` branch.
2. Open the repository → **Settings** → **Pages**.
3. Under *Build and deployment*, set **Source** to `Deploy from a branch`,
   **Branch** to `main`, folder `/ (root)`.
4. Click **Save** and wait a minute.
5. The site appears at `https://<username>.github.io/<repository-name>/`.

## Limitations (honest list)

- This is a **frontend prototype**. There is no backend, database or user account system.
- The resource links are **well-known public platforms, not verified college-specific
  resources**. Your own college website remains the official source for courses, clubs
  and notices.
- There is **no search or filtering**, because both need JavaScript.
- Nothing is stored or tracked: no cookies, no analytics, no forms.
- Content is currently static and must be edited by hand.

## Roadmap

- [ ] Replace generic links with verified IIIT Raipur / Hack-A-Sol specific resources
- [ ] Add a search and filter box (needs JavaScript)
- [ ] Add a "submit a resource" form (needs a backend)
- [ ] Add a light/dark theme switch
- [ ] Track link usefulness so low-value links can be removed

## Author

**Dishin** — built as a learning project for the Hack-A-Sol hackathon at IIIT Raipur.

If you found a broken link or have a resource worth adding, feel free to open an issue.
