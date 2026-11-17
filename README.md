# Vangardis — criminal defense law firm landing page

A portfolio study case: a one-page website for a fictional law firm specialising in criminal defense. English version.

**Live version:** https://vangardis-english.vercel.app

---

## ⚠️ Disclaimer

**This is a fictional project, created solely for educational purposes.**

The law firm "Vangardis" does not exist. All names, phone numbers, bar certificate numbers, company registration codes, addresses, attorney names, case descriptions and any other data on this website are **fictional**. Any resemblance to real people, organisations, cases or contact details is **coincidental**.

The "Privacy Policy" page (`privacy.html`) is a **sample document structure**, not an operative policy of a real company. It is included as part of the study mockup and creates no obligations whatsoever.

This website provides no legal services and is not legal advice.

---

## The brief

Someone lands on a site like this under stress — during a search, after a relative has been arrested, before being questioned. So the central idea of the layout is this: do not make them work out which service they need.

The first screen opens with a question — **"What has happened?"** The visitor picks their situation and immediately sees their rights and what to do right now. A call button stays within reach from anywhere on the page.

## Site structure

1. Hero — situation picker and rights
2. What we handle — 12 services
3. From the first call to the decision — four steps
4. Attorneys
5. Cases we have handled
6. Frequently asked questions
7. Contacts and call-back form

## What was built

**Markup and layout**
- Semantic markup, `lang="en"`
- Responsive from 320px to 1440px, no horizontal scrolling
- Horizontal carousels with `scroll-snap` and arrow controls
- Hero video with a poster frame and a WebM fallback format

**Performance**
- Photography in WebP wherever it pays off (one file stays JPEG — WebP came out larger for it)
- Lazy loading: the first screen pulls 7 images instead of 22
- Video in two formats, with a poster for the first frame

**Accessibility**
- Visible keyboard focus on every interactive element
- Logical Tab order
- `aria-label`, `aria-selected` and `alt` on all images
- Text contrast meets WCAG AA
- Full `prefers-reduced-motion` support — every animation switches off

**Motion**
- Sections and cards reveal on scroll
- Headline emerges from a blur, with the colour igniting a beat later
- Cards lift on hover
- Carousel edges fade where content continues
- A one-time nudge hinting that the carousels scroll
- Smooth expansion of the FAQ items
- A ring that follows the cursor (without hiding the system cursor)

## Data and privacy

The site uses no cookies, no counters and no analytics. The only external request is for fonts from Google Fonts.

The call-back form collects nothing but a name and a phone number. The consent checkbox is not pre-ticked and links to the [privacy policy](privacy.html); without it the submit button stays disabled.

## Tech

Plain HTML, CSS and JavaScript — no frameworks, no build step.
Typefaces — Cormorant SC and Manrope (Google Fonts).

## File structure

```
.
├── index.html        home page: markup, styles and scripts
├── privacy.html      privacy policy
├── preview.jpg       preview card for messengers (og:image)
├── images/           photography (22 files, mostly WebP)
├── media/            hero video and poster
├── .gitignore
└── README.md
```

## Running it locally

Open the page through a local server rather than by double-clicking it — otherwise the browser may block the video:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

## Photography and licensing

**All photography** comes from [Unsplash](https://unsplash.com), under the [Unsplash licence](https://unsplash.com/license).
Images are cropped to the proportions of their blocks; no other changes were made.

---

Design: Figma. Author: Irina Kaliadina.
