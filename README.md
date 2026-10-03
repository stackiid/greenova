# Greenova

![HTML5](https://img.shields.io/badge/HTML-5-E34F26)
![CSS3](https://img.shields.io/badge/CSS-3-1572B6)
![JavaScript](https://img.shields.io/badge/JavaScript-none-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)

A responsive, single-page marketing website for a renewable energy company, built with plain HTML5 and CSS3. The page presents solar, wind, energy storage, and consulting services through a sequence of themed sections, and includes a mobile navigation menu that works without any JavaScript.

## Live Demo

[https://stackiid.github.io/greenova/](https://stackiid.github.io/greenova/)

## Table of Contents

- [Features](#features)
- [Page Sections](#page-sections)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Design System](#design-system)
- [Responsive Design](#responsive-design)
- [Accessibility](#accessibility)
- [SEO](#seo)
- [Performance Considerations](#performance-considerations)
- [Browser Support](#browser-support)
- [Known Limitations](#known-limitations)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Features

- Sticky navigation bar with a blurred translucent background
- Mobile navigation menu implemented with a hidden checkbox and the CSS `:has()` selector, with no JavaScript
- Hero section with a headline, call-to-action button, scroll indicator, and a floating information card over the hero image
- Feature strip highlighting three values: Sustainable, Reliable, and Responsible
- Four service cards for Solar Energy, Wind Energy, Energy Storage, and Consulting
- Statistics blocks in the About and Impact sections, including a visually emphasized featured metric
- Projects showcase with one tall card and two grouped cards
- Two call-to-action sections that link to the contact section
- Blog preview grid with three tagged article cards
- Multi-column footer with quick links, solution links, social icons, and contact details
- Design tokens (colors, fonts, spacing, radii, shadows, transitions) defined as CSS custom properties
- Fluid typography and spacing built with `clamp()`

## Page Sections

| Order | Section              | Anchor       | Content                                                            |
| ----- | -------------------- | ------------ | ------------------------------------------------------------------ |
| 1     | Navigation           | -            | Logo, five page links, a Search button, and a Contact Us button    |
| 2     | Hero                 | `#home`      | Headline, supporting text, Explore Solutions button, floating card |
| 3     | Features strip       | -            | Sustainable, Reliable, Responsible                                 |
| 4     | About                | `#about`     | Company summary, three highlights, three statistics                |
| 5     | Solutions            | `#solutions` | Solar, Wind, Energy Storage, Consulting                            |
| 6     | Impact               | -            | Three headline statistics and a wide image                         |
| 7     | Projects             | `#projects`  | Three project cards with locations                                 |
| 8     | Call to action       | -            | "Ready to Switch to Clean Energy?" banner                          |
| 9     | Why choose us        | -            | Four value points with icons                                       |
| 10    | Blog                 | `#blog`      | Three article preview cards                                        |
| 11    | Final call to action | `#contact`   | "Be Part of the Clean Energy Movement"                             |
| 12    | Footer               | -            | Brand summary, links, contact details, legal links                 |

The text, statistics, project names, and contact details on the page are sample content written to demonstrate the layout.

## Tech Stack

| Category      | Technology                                                                                                 |
| ------------- | ---------------------------------------------------------------------------------------------------------- |
| Markup        | HTML5 (semantic elements: `header`, `nav`, `main`, `section`, `article`, `footer`)                         |
| Styling       | CSS3 with custom properties, Grid, Flexbox, `clamp()`, `:has()`, `position: sticky`, and `backdrop-filter` |
| Fonts         | Google Fonts: Plus Jakarta Sans (headings) and Inter (body)                                                |
| Icons         | Font Awesome 6.5.1, loaded from cdnjs                                                                      |
| Images        | Photographs loaded from Unsplash URLs, plus a local favicon                                                |
| JavaScript    | None                                                                                                       |
| Build tooling | None                                                                                                       |

## Project Structure

```text
greenova/
|-- assets/
|   |-- favicon.png      # Browser tab icon
|   `-- greenova.png     # Full-page screenshot of the landing page
|-- styles/
|   `-- style.css        # All styles: tokens, layout, components, responsive rules
|-- index.html           # Complete page markup
|-- LICENSE              # MIT License
`-- README.md
```

## Prerequisites

- A modern web browser
- An internet connection, because the fonts, icons, and photographs are loaded from external hosts
- Optional: Python 3, if you want to serve the site through a local web server

## Getting Started

Clone the repository and move into it:

```bash
git clone https://github.com/stackiid/greenova.git
cd greenova
```

Open `index.html` directly in a browser, or serve the folder locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

There are no dependencies to install and no build step.

## Design System

The visual design is controlled by CSS custom properties declared on `:root` in `styles/style.css`.

| Group           | Examples                                                                                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Colors          | `--color-bg`, `--color-bg-alt`, `--color-dark`, `--color-primary`, `--color-accent`, `--color-accent-light`, `--color-text`, `--color-text-muted`, `--color-border` |
| Typography      | `--font-display`, `--font-body`, `--fs-body`, `--fs-lead`, `--fs-small`, `--fs-eyebrow`                                                                             |
| Spacing         | `--space-xs` to `--space-xl`, `--section-padding`, `--section-padding-mobile`, `--container-width`, `--container-pad`                                               |
| Shape and depth | `--radius-sm` to `--radius-full`, `--shadow-sm`, `--shadow-md`, `--shadow-lg`                                                                                       |
| Motion          | `--transition-fast`, `--transition`                                                                                                                                 |

Reusable classes such as `.container`, `.btn`, `.btn-primary`, `.eyebrow`, and `.section-heading` are shared across sections.

## Responsive Design

The stylesheet uses fluid sizing for typography, spacing, and radii, and adjusts the layout at the following breakpoints:

| Breakpoint          | Behavior                                                                                                                                   |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 1800px and wider    | Container maximum width increases to 1320px                                                                                                |
| 1024px and narrower | Hero, About, Why Choose Us, Projects, and CTA banner switch to a single column, and their images move above the text where defined         |
| 860px and narrower  | Desktop navigation links and the Search button are hidden, and the checkbox-driven mobile menu panel is used                               |
| 480px and narrower  | The About stats card and hero floating card return to normal flow instead of overlapping, and the featured impact stat is no longer offset |
| 340px and narrower  | Navigation actions and feature items use tighter gaps                                                                                      |

### Mobile Menu

The menu is built from a hidden checkbox (`#nav-toggle`) and a `<label>` that acts as the hamburger button. When the checkbox is checked, the rule `.navbar:has(.nav-toggle-input:checked)` expands the navigation panel and swaps the menu icon for a close icon.

## Accessibility

Implemented practices visible in the code:

- `lang="en"` on the root element
- Semantic landmarks and sectioning elements
- `aria-label` on the primary navigation, the Search button, the menu toggle, and the social links
- `aria-hidden` on decorative navigation icons and the menu icons
- Descriptive `alt` text on every image
- Visible `:focus-visible` styles for links, buttons, and inputs

No accessibility audit or WCAG conformance level is claimed.

## SEO

The `<head>` of `index.html` contains:

- A page title and meta description
- Open Graph tags: `og:title`, `og:description`, and `og:type`
- A viewport meta tag
- A favicon link

The page does not include an `og:image`, canonical URL, sitemap, or `robots.txt`.

## Performance Considerations

- The site ships no JavaScript and no build output
- Google Fonts are requested with `preconnect` hints and `display=swap`
- The stylesheet is a single local file
- `assets/greenova.png` is a large screenshot (about 5.8 MB) that is used only for this README and is not loaded by the page

## Browser Support

The mobile menu depends on the CSS `:has()` selector. In a browser without `:has()` support, the menu toggle will not open the navigation panel on narrow screens. No other browser targets are defined in the project.

## Known Limitations

- The Search button in the navigation bar has no behavior attached to it
- The Contact Us and Get Started buttons are in-page anchors; there is no contact form or backend
- Learn More, Read More, View All Projects, and View All Articles links point to in-page anchors rather than separate pages
- The social media icons and the Privacy Policy and Terms of Service links use placeholder `#` targets
- Photographs depend on Unsplash URLs and will not load without an internet connection

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

Copyright (c) 2026 Ubaid Ahmad

## Acknowledgements

- Photographs from [Unsplash](https://unsplash.com)
- Typefaces from [Google Fonts](https://fonts.google.com): Plus Jakarta Sans and Inter
- Icons from [Font Awesome](https://fontawesome.com)
