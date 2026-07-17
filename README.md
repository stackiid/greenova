# 🌿 Greenova - Powering a Greener Future with Renewable Energy

A responsive marketing landing page for a renewable energy company, built with plain HTML5 and CSS3 - no JavaScript, no frameworks.

<div align="center">

### 🔗 [**View Live Demo**](https://stackiid.github.io/greenova/) 🔗

</div>

---

## 📖 Overview

Greenova is a single-page marketing site for a fictional renewable energy company offering solar, wind, storage, and consulting services. It was built as a front-end practice project focused on layout composition, section-based storytelling, and CSS-only interactivity - proving that a fully responsive, animated-feeling navigation experience doesn't require a single line of JavaScript.

## ✨ Features

- Sticky navbar with a fully CSS-only mobile menu (no JS toggle logic)
- Hero section with floating info card overlay
- Feature strip highlighting core value props (Sustainable, Reliable, Responsible)
- About section with an inline stats card (experience, projects, satisfaction)
- Solutions grid covering Solar, Wind, Energy Storage, and Consulting
- Impact/stats section with a featured metric callout
- Projects showcase with a tall + grouped card layout
- Two distinct CTA banners driving toward the contact section
- "Why Choose Us" grid with icon-led value points
- Blog/resources preview grid with tagged articles
- Multi-column footer with quick links, solutions, and contact details
- SEO-ready `<meta>` tags and Open Graph tags for link previews

## 🧠 Concepts Demonstrated

| Concept                          | Where it shows up                                                        |
| -------------------------------- | ------------------------------------------------------------------------ |
| Semantic HTML5                   | `<header>`, `<main>`, `<section>`, `<article>`, `<footer>` structure     |
| CSS-only interactivity           | Checkbox + `:has()` selector driving the mobile nav (zero JS)            |
| CSS Grid & Flexbox               | Hero, about, solutions, projects, and footer layouts                     |
| Responsive design                | Mobile-first breakpoints across every section                            |
| Accessibility                    | `aria-label`, `aria-hidden`, descriptive `alt` text on all images        |
| SEO / Open Graph                 | Meta description, `og:title`, `og:type`, `og:description`                |
| Third-party integration          | Google Fonts (Plus Jakarta Sans, Inter) + Font Awesome 6 via CDN         |
| Component-style CSS organization | Reusable classes (`.btn`, `.eyebrow`, `.section-heading`, card patterns) |

## 📁 Project Structure

```
Greenova/
├── index.html            # All page markup - nav, hero, about, solutions, impact,
│                         # projects, CTAs, why-choose, blog, footer
├── style.css             # All styling - layout, responsive rules, CSS-only nav logic
└── assets/
    ├── favicon.png       # Browser tab icon
    └── greenova.png      # Brand asset
```

## 🚀 Getting Started

**Prerequisites:** a web browser. That's it - no Node, no package manager, no build step.

```bash
# Clone the repo
git clone <your-repo-url>
cd Greenova

# Open directly
# Option A - just double-click index.html

# Option B - serve locally (recommended for correct relative paths)
python -m http.server 8000
# then visit http://localhost:8000
```

## 📝 Notes

- All hero, about, projects, and blog imagery is pulled from Unsplash via direct URLs - swap these for your own assets before production use.
- Nav links (`#solutions`, `#about`, `#projects`, `#blog`, `#contact`) point to in-page anchors; content beyond the hero is illustrative/placeholder copy.
- No backend, no form submission handling - the "Contact Us" and "Get Started" CTAs are static anchors, not wired to a mail service.
- Future improvement: connect the contact CTA to a real form handler (e.g., Formspree, EmailJS) and swap placeholder social links for real profiles.

## 📄 License

MIT - see the [LICENSE](./LICENSE) file in the root of the repository.
