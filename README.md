# Aman Chapadiya — Personal Portfolio

A professional, responsive, single-page developer portfolio website presenting the skills, projects, and career background of Aman Chapadiya, a Software Developer specializing in frontend engineering and full-stack systems.

---

## Badges

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Last Commit](https://img.shields.io/github/last-commit/obscure-01/Portfolio.svg?style=flat&color=success)](https://github.com/obscure-01/Portfolio/commits/main)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Glossary/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Responsive](https://img.shields.io/badge/Responsive-Yes-blueviolet.svg?style=flat)](#responsive-design)

---

## Table of Contents

- [Overview](#overview)
- [Live Demo](#live-demo)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Architecture](#project-architecture)
- [Folder Structure](#folder-structure)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Scripts](#scripts)
- [Performance](#performance)
- [Accessibility](#accessibility)
- [Responsive Design](#responsive-design)
- [Deployment](#deployment)
- [Code Quality](#code-quality)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)
- [Acknowledgements](#acknowledgements)

---

## Overview

This project is a clean, single-page web portfolio designed to present a professional resume and portfolio overview in a structured layout.

### Purpose
The portfolio serves as a central hub to display skills, experience, and projects. It is built to load instantly and behave predictably across device sizes, allowing recruiters and technical collaborators to evaluate Aman Chapadiya's credentials.

### Target Audience
- **Technical Recruiters & Hiring Managers** requiring rapid access to credentials, skill maps, and project repositories.
- **Developers & Open Source Contributors** looking to verify code layout or collaborate on referenced applications.

### Key Objectives
- Achieve high-speed page loads using semantic, framework-free web standards.
- Provide fluid visual cues and micro-animations through optimized CSS properties.
- Ensure cross-browser styling consistency and responsive viewports.

---

## Live Demo

| Resource | Link |
| :--- | :--- |
| **🌐 Live Portfolio** | [https://portfoliobyaman.vercel.app/](https://portfoliobyaman.vercel.app/) |
| **💻 GitHub Repository** | [https://github.com/obscure-01/Portfolio](https://github.com/obscure-01/Portfolio) |
| **👨‍💼 LinkedIn** | [https://www.linkedin.com/in/amanchapadiya/](https://www.linkedin.com/in/amanchapadiya/) |
| **📧 Email** | [chapadiya.aman@gmail.com](mailto:chapadiya.aman@gmail.com) |

---

## Features

### User Experience
- **Fluid Layout Transitions:** Uses transition curves (`0.4s cubic-bezier`) for visual elements, links, and cards.
- **Glassmorphic Navigation:** Sticky navigation bar utilizing browser-native `backdrop-filter: blur(24px)` to maintain visibility during scroll.
- **Smooth Navigation Scrolling:** Navigates via native browser anchors with scroll offset buffers to prevent section headers from being obscured.

### Design & Theme
- **Sunrise Palette:** A cohesive, custom color scheme using warm ivory background tones, soft sands, and contrasting ocean blue typography.
- **Ambient Accents:** Employs absolute-positioned, heavy-blurred background glowing elements to create depth without layout shifting.
- **Project Styling Accents:**
  - **ORIGO Card:** Renders a dashed compass ring decoration that rotates on card hover.
  - **AIris Security Card:** Renders a technical blueprint SVG grid layout that brightens on hover.

### Developer Experience
- **Icon Normalization:** Corrects optical scale differences between Devicon logos and FontAwesome glyphs using an explicit class boundary container (`36px` x `36px`) and customized relative sizing overrides.
- **Strict Formatting:** Structured markup and modular CSS variables map out typography, colors, padding, and transitions globally.

---

## Tech Stack

| Component | Standard / Library | Purpose |
| :--- | :--- | :--- |
| **Core** | HTML5 | Semantics and site structure |
| **Style Sheet** | CSS3 | Variable definitions, grid/flexbox system, animations, media queries |
| **Typography** | Inter & Poppins | Google Fonts imported for readable paragraphs and clean headings |
| **Icons** | FontAwesome 6.4.0 & Devicon | Lightweight scalable SVG vector icons |
| **Asset Host** | Cloudinary | Delivers optimized profile portrait image from cloud CDN |
| **Deployment** | Vercel | Hosting infrastructure for static assets |

---

## Project Architecture

The repository is built as a single-page static document:

```
[Browser Request]
       │
       ├──► index.html (Builds DOM Tree, Loads CDNs, Integrates Layout)
       │
       └──► style.css (Injects CSS variables, Animations, Media Breakpoints)
```

- **Folder Organization:** Flat files structure containing static templates and styled variables, preventing redundant compile steps.
- **Components:** Created inside clean semantic blocks (`<header>`, `<main>`, `<section>`, `<article>`).
- **Data Flow:** Entirely static. Anchor navigation maps targets between navigation links and specific section IDs.
- **Styling Strategy:** Relies on CSS Custom Properties (`:root`) for color palettes, shadows, spacing values, and transitions.

---

## Folder Structure

```
Portfolio/
├── assets/                     # Shared static visual assets
│   └── favicon/                # Cross-platform favicon collection
│       ├── apple-touch-icon.png
│       ├── favicon-16x16.png
│       ├── favicon-32x32.png
│       └── favicon.ico
├── index.html                  # Core HTML document structure
├── style.css                   # Custom styles and responsive layouts
├── LICENSE                     # MIT License specification
└── README.md                   # Project documentation
```

---

## Installation

This is a static project using raw HTML/CSS. No installation or build environment setup is required.

### Local Preview Setup

#### Option A: Python HTTP Server (Terminal)
Run a local server from the root directory:
```bash
python -m http.server 8000
```
Navigate to `http://localhost:8000` in your web browser.

#### Option B: VS Code Live Server (IDE)
1. Open the project workspace in Visual Studio Code.
2. Install the **Live Server** extension.
3. Click **Go Live** in the status bar at the bottom right.

---

## Environment Variables

This project does not use any environment variables. All references are linked statically within the codebase.

---

## Scripts

This project does not include a `package.json` file. Consequently, no package manager scripts are available or required. Local previews are handled using the methods specified in the [Installation](#installation) section.

---

## Performance

- **Zero JavaScript Overhead:** Contains no script tags or JavaScript files, minimizing parse and execution times.
- **Connection Pre-warming:** Employs HTML resource hints (`preconnect` and `dns-prefetch`) to establish early connections with Google Fonts, Devicon, and FontAwesome domains.
- **Render-Optimized Animations:** Animates layout transformations using CSS transitions rather than active scroll handlers or layout-disrupting scripts.

---

## Accessibility

- **Standard Focus Ring Indicators:** Focusable links and buttons specify a custom visible outline style (`outline: 2px solid var(--ocean-blue)`) to ensure navigation visibility.
- **Semantic DOM Outline:** Content is structured hierarchically (`<h1>` down to `<h4>`), allowing screen readers to parse the layout sequentially.
- **Descriptive Labels:** Screen reader target definitions are annotated on non-text elements (e.g. `aria-label="Scroll down"` on navigation chevron).

---

## Responsive Design

Responsiveness is handled in `style.css` via custom media breakpoints:

- **Desktop (default):** Supports fluid flexbox and multi-column project grids.
- **Tablet / Large Screens (`<= 1024px`):** Centers the hero section and stacks the profile layout column.
- **Mobile Devices (`<= 768px`):** Collapses navigation lists to a wrapped column, hides the scroll indicator, reduces section paddings, and formats button elements as block-width tap targets.

---

## Deployment

The application is deployed on **Vercel** at the following URL:
[https://portfoliobyaman.vercel.app/](https://portfoliobyaman.vercel.app/)

### Deployment Instructions on Vercel
To deploy this project to Vercel:
1. Push your code to your GitHub repository.
2. Go to the [Vercel Dashboard](https://vercel.com/dashboard) and click **Add New Project**.
3. Import the `Portfolio` repository.
4. Select the default project configuration (Vercel automatically detects static HTML/CSS configurations with no build step required).
5. Click **Deploy**.

---

## Code Quality

- **Modular CSS Variables:** All styling coordinates are defined inside the CSS `:root` selector.
- **Clean Structure:** Consistent tag indentation, readable comment dividers, and BEM-like naming conventions.
- **Maintainable Layouts:** Eliminates frame dependencies to preserve standard, long-term compatibility.

---

## Future Improvements

- [ ] **Dark Mode Toggle:** Ingest preferences via `@media (prefers-color-scheme: dark)` or a manual toggle.
- [ ] **Contact Form Endpoint:** Link the contact elements to a form validation service (e.g. Formspree).
- [ ] **Dynamic Project Filters:** Apply client-side JavaScript filtering to isolate projects by tag.

---

## Contributing

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Author

**Aman Chapadiya**
- **GitHub:** [@obscure-01](https://github.com/obscure-01)
- **LinkedIn:** [Aman Chapadiya](https://www.linkedin.com/in/amanchapadiya/)
- **Email:** [chapadiya.aman@gmail.com](mailto:chapadiya.aman@gmail.com)

---

## Acknowledgements

- [Google Fonts](https://fonts.google.com/) (Inter & Poppins)
- [FontAwesome Icons](https://fontawesome.com/)
- [Devicon Library](https://devicon.dev/)
- [Shields.io Badges](https://shields.io/)
- [Cloudinary](https://cloudinary.com/) (Image distribution)