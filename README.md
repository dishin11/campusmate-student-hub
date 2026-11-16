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
| **Hero** | Headline, call-to-action buttons, a photo panel with three floating info cards, and a keyboard-friendly skip link. |
| **Four pillars** | Academic Support, Student Clubs, Career Growth and Wellbeing — each with an icon and an "Explore" link. |
| **Resource library** | 12 real resources (NPTEL, SWAYAM, MIT OpenCourseWare, Khan Academy, GitHub, Stack Overflow, Internshala, HackerRank, LinkedIn, Tele-MANAS, WHO, campus counselling). |
| **Live filter** | Filter the library by All / Academics / Clubs / Career / Wellbeing. Instant, no reload, no JavaScript. |
| **Student stories** | Two student quotes, with a "More Stories" button that reveals two more. |
| **FAQs** | An expandable accordion built with `<details>` and `<summary>`. |
| **Quick tour** | A pop-up overview of the four areas, opened from the hero. |
| **CTA band + footer** | Contact/action band, social links and footer navigation. |

## Interactive features (all without JavaScript)

| Feature | How it works |
| --- | --- |
| Library filter | Five hidden `<input type="radio">` buttons. CSS checks which one is selected and hides every card whose `data-cat` does not match, using `:checked` + the general sibling combinator. |
| "More Stories" toggle | A hidden `<input type="checkbox">`. When checked, CSS reveals the extra quote cards and swaps the button text — the classic "CSS-only toggle" pattern. |
| Quick tour pop-up | The tour lives in the page but is `display: none` until the URL ends in `#tour`. `.modal:target { display: grid }` then shows it. Links inside close it by pointing back to `#home`. |
| FAQ accordion | Native `<details>` / `<summary>` elements. The browser handles opening and closing; CSS only styles the arrow and the blue marker. |
| Responsive layout | CSS Grid with `auto-fit`/`minmax` plus media queries at 1024px, 820px, 720px and 560px. |

## Placeholder content

The university names in the "Trusted by students at" strip and the student quotes in
the stories section are **sample placeholders**, not real endorsements. Replace them
with real names and permission-based quotes before using this as an official site.

## Pages and files

```
campusmate-student-hub/
├── index.html   → page structure and all content
├── style.css    → design, layout, responsive rules
└── README.md    → this file
```

## How it was built

- **Semantic HTML5** — `header`, `nav`, `main`, `section`, `article`, `figure`, `footer`,
  with a logical heading order.
- **One SVG icon sprite** — every icon is drawn once in a hidden `<svg>` block and reused
  with `<use href="#i-name">`, so icons stay consistent and the markup stays short.
- **CSS custom properties** (design tokens) for colours, spacing and radius, so the theme
  is changed in one place.
- **CSS Grid** for card layouts, using `auto-fit` + `minmax()` so cards reflow before a
  media query is even needed.
- **`<details>` / `<summary>`** for the FAQ accordion.
- **Accessibility basics** — skip link, visible `:focus-visible` outlines, `aria-label`
  on navigation and icon links, keyboard-reachable filter controls, and
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
- The "Get Started" button scrolls to the resource library — there is no sign-up flow yet.
- The resource links are **well-known public platforms, not verified college-specific
  resources**. Your own college website remains the official source for courses, clubs
  and notices.
- The hero photo is loaded from Unsplash over the internet, so it needs a connection.
- There is **no text search**, because that needs JavaScript.
- Nothing is stored or tracked: no cookies, no analytics, no forms.

## Roadmap

- [ ] Replace generic links with verified college-specific resources
- [ ] Replace the placeholder universities and quotes with real ones
- [ ] Add a text search box (needs JavaScript)
- [ ] Add a "submit a resource" form (needs a backend)
- [ ] Self-host the hero photo instead of hotlinking it
- [ ] Add a light/dark theme switch

## Author

**Dishin** — built as a learning project to practise HTML and CSS.

If you found a broken link or have a resource worth adding, feel free to open an issue.
