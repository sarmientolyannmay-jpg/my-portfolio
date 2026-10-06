# Lyann May B. Sarmiento — Personal Portfolio Website

A static personal portfolio website built with plain HTML, CSS, and JavaScript
for the BSCS Midterm Project at CATSU | CICT.

---

## 1. Project Overview

**Purpose**

This portfolio presents who I am beyond a single job title. It is designed to
introduce me as a mom, wife, student, entrepreneur, and virtual assistant, and
to serve as an online point of contact for anyone interested in working with
me or learning about my services.

**Intended Audience**

- Prospective clients looking for virtual assistant services
- Employers or recruiters reviewing my background
- Fellow students and instructors viewing the project
- Anyone who wants to reach out through my listed contact channels

**Content Included**

- A hero introduction with my name and the roles I hold
- An "About Me" section describing my background and approach
- A "Hobbies and Interests" section with four interest cards
- A dedicated Skills page listing my technical and professional skills
- Contact details (email, LinkedIn, Facebook, WhatsApp)

**How the Website Is Organized**

The site has two pages:

1. `index.html` — the main page, containing four sections: Home (hero),
   About, Skills (a summary linking to the Skills page), and Contact.
2. `skills.html` — the detailed Skills page, listing Technical Skills and
   Professional Skills.

Navigation is a sticky header that stays visible while scrolling. On the main
page, the header links jump to sections within the page. On the Skills page,
the header links return to the matching sections of the main page.

---

## 2. Technologies Used

- **HTML5** — semantic structure, no frameworks
- **CSS3** — custom properties (variables), Flexbox, CSS Grid, media queries
- **JavaScript (vanilla)** — scroll reveal animation, dynamic footer year
- **Google Fonts** — Playfair Display (headings) and Poppins (body text)

No build tools, package managers, or external libraries are used.

---

## 3. File Structure


Assets are separated by type: all styling lives in `css/`, all scripting in
`js/`, and all images in `images/`. Both HTML files sit at the project root.

---

## 4. How to View the Project

No installation or server is required. Download or clone the project folder,
then open `index.html` in any modern web browser.

For the best experience, keep the folder structure intact so the relative
paths to `css/`, `js/`, and `images/` resolve correctly.

---

## 5. Web Development Practices Applied

**HTML**

- Proper document structure with `<!DOCTYPE html>`, `<html lang="en">`,
  `<head>`, and `<body>`
- Semantic elements: `<header>`, `<nav>`, `<main>`, `<section>`,
  `<footer>`, `<figure>`
- Logical heading hierarchy (`<h1>` once per page, then `<h2>`, `<h3>`, `<h4>`)
- Meaningful link text (no bare "click here" links)
- `alt` text on the portrait image

**CSS**

- Consistent colour palette and typography defined as CSS custom properties
  in `:root`
- Layout using CSS Grid (`.about-grid`, `.card-grid`) and Flexbox
  (`.nav-links`, `.role-list`, `.chip-list`)
- Consistent spacing and visual hierarchy across sections
- Hover and focus states on all interactive elements

**Accessibility**

- "Skip to main content" link for keyboard users
- Visible focus outlines on links and buttons
- Sufficient colour contrast between text and backgrounds
- Decorative emoji icons marked `aria-hidden="true"`
- Reduced-motion support via `prefers-reduced-motion`

**Responsive Design**

- Two breakpoints: `768px` (tablet) and `480px` (mobile)
- `.about-grid` collapses to a single column on smaller screens
- Heading sizes scale with viewport width using `clamp()`
- Content remains readable at desktop, tablet, and mobile widths without
  horizontal scrolling

---

## 6. Testing and Improvement

**Problem Encountered: Portfolio Heading Wrapping Mid-Name**

- **What the problem was:** On the main page, my full name in the hero
  heading ("Lyann May B. Sarmiento") broke across two lines, splitting the
  name awkwardly and breaking the visual balance of the introduction.

- **What caused it:** The heading font size was set too large for the width
  of its container. When the rendered text grew wider than the available
  space, the browser wrapped it at the nearest word boundary. The heading
  also lacked any rule controlling where a line break was allowed.

- **How it was solved:** I split the heading into two spans — the greeting
  and the name — and set both to `display: block` in CSS so the greeting
  sits on the first line and the name below it. I then applied
  `white-space: nowrap` to the name so it could never break mid-name, and
  changed the font size to a `clamp()` value that scales with viewport
  width instead of a fixed size. A media query at `480px` reduces the size
  further so the name still fits on narrow phone screens.

- **What was learned:** Text layout depends on the relationship between font
  size and container width, not on the text alone. A size that looks correct
  on a large screen can overflow on a smaller one. Viewport-relative units
  like `clamp()` and explicit control over line breaks (`white-space`) are
  more reliable than fixed sizes when content must stay on one line.

Another issue encountered during development was that the Skills page was
initially rendering with no styling at all — it displayed as plain,
unformatted HTML. The cause was that the page's stylesheet link was pointing
to a path that did not resolve, so the browser loaded the HTML but never
received the CSS. Confirming the folder structure and correcting the link so
it pointed to `css/style.css` resolved it. This showed the importance of
maintaining a consistent folder structure and using relative paths
carefully.

---

## 7. Remaining Work

The project is roughly 60–70% complete. The following still needs to be
done before the Final Term:

- [ ] **Contact form** — currently only contact links; a proper form with
      labelled fields would demonstrate form elements and labels
- [ ] **Mobile navigation menu** — the header links wrap on very small
      screens; a collapsible hamburger menu would improve usability
- [ ] **Accessibility audit** — verify colour contrast values with a
      contrast checker and confirm keyboard navigation order on both pages
- [ ] **Content completion** — add a Projects or Experience section, and
      replace any placeholder content with final text
- [ ] **Testing** — test across multiple browsers (Chrome, Firefox, Safari,
      Edge) and on real mobile devices
- [ ] **Code cleanup** — review the stylesheet for unused or duplicate
      rules and consolidate where possible
- [ ] **SEO and metadata** — add Open Graph tags so links preview properly
      when shared on Facebook or LinkedIn
- [ ] **Deployment** — publish the site online (see below)

---

## 8. Deployment Plan

The site is fully static, so it needs no server-side runtime or database.
For the Final Term, I plan to deploy it using **GitHub Pages**, which hosts
static sites directly from a GitHub repository at no cost.

The steps will be:

1. Push the project folder to a GitHub repository
2. Enable GitHub Pages in the repository settings
3. Verify that all relative paths (`css/`, `js/`, `images/`) resolve
   correctly on the live URL
4. Test the deployed site on both desktop and mobile to confirm it matches
   the local version

An alternative would be Netlify, which supports drag-and-drop deployment of
a static folder and provides a free subdomain.

---

## 9. Author

**Lyann May B. Sarmiento**
BSCS — CATSU | CICT

- Email: sarmientolyannmay@gmail.com
- LinkedIn: [linkedin.com](https://www.linkedin.com/in/lyann-may-sarmiento-977082170/)
- Facebook: [facebook.com](https://www.facebook.com/akosileeyann/)
- WhatsApp: leeyanmay

---

*Midterm Project Update — 2026*
