# Hadia Akbar — Portfolio

A responsive, single-page portfolio website for **Hadia Akbar**, an AI/ML Engineer, Software Developer, and Creative Technologist based in Lahore, Pakistan.

The portfolio uses a dark, crimson-accented interface inspired by an AI system dashboard. It presents professional experience, technical capabilities, selected projects, education, and contact information in an interactive scrolling experience.

## Live Portfolio

After deployment, the portfolio is available at the URL assigned by the hosting provider.

## Features

| Feature | Description |
|---|---|
| Responsive layout | Designed for desktop, tablet, and mobile screen sizes. |
| Interactive visual system | Includes animated background effects, grid overlays, particles, scan lines, HUD-style elements, and progress indicators. |
| Smooth scrolling | Uses Lenis for smooth page scrolling and GSAP ScrollTrigger for scroll-based animation. |
| Motion-aware experience | Includes reduced-motion support through the `prefers-reduced-motion` media query. |
| Embedded CV viewer | The CV can be opened inside the portfolio and downloaded from the interface. |
| External typography | Uses Space Grotesk, Inter, and Space Mono from Google Fonts. |
| Static deployment | Can be deployed directly to services such as Vercel, Netlify, GitHub Pages, or any static web host. |

## Technology

This project is intentionally lightweight and does not require a build system or package manager. It is implemented with:

- Semantic HTML5
- CSS3, including responsive layouts, custom properties, gradients, animations, and backdrop filters
- Vanilla JavaScript
- [GSAP](https://gsap.com/) and [ScrollTrigger](https://gsap.com/docs/v3/Plugins/ScrollTrigger/)
- [Lenis](https://lenis.darkroom.engineering/) for smooth scrolling
- Google Fonts

The GSAP and Lenis libraries are loaded through CDN links in `index.html`.

## Repository Structure

```text
.
├── index.html          # Main portfolio page, styles, scripts, and embedded CV data
├── HadiaAkbar_CV.pdf   # Source CV document
└── README.md           # Project documentation
```

## Run Locally

Because this is a static website, it can be opened directly in a browser. For the most reliable local preview, serve the repository with a small HTTP server.

### Using Python

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser.

### Using Node.js

If a Node.js environment is available, the repository can also be served with a static server such as `serve`:

```bash
npx serve .
```

## Deployment

The deployment root must be configured as the repository root, where `index.html` is located. No build command or output directory is required.

| Setting | Value |
|---|---|
| Framework preset | Other / Static HTML |
| Root directory | Repository root |
| Build command | None |
| Output directory | Repository root or empty, depending on the provider |
| Install command | None |
| Entry point | `index.html` |

### Vercel

Create a new project from the GitHub repository and use the default project root. Select **Other** as the framework preset if Vercel asks for one, leave the build command empty, and deploy.

### Netlify

Create a site from the repository, leave the build command empty, and set the publish directory to `.` or the repository root.

### GitHub Pages

Enable GitHub Pages from the repository settings and publish from the `main` branch root. The root `index.html` file is required for the site to load at the domain root.

## Customization

Most visual and content changes can be made directly in `index.html`.

### Update personal information

Search for the contact section and replace the placeholder LinkedIn and GitHub URLs with the correct profiles. Update the email address, phone number, location, biography, skills, project descriptions, and experience details as needed.

### Update the CV

The page currently includes CV data in the HTML so that the embedded viewer and download control work without requiring a separate PDF request. If the CV is replaced, update the embedded PDF data in `index.html` and keep `HadiaAkbar_CV.pdf` synchronized with the displayed version.

### Update colors and typography

The primary design tokens are defined near the top of the stylesheet in the `:root` block. The most important variables include:

```css
--void       /* Main background */
--crimson-mid/* Secondary background tone */
--red        /* Primary accent */
--ember      /* Warm accent */
--white      /* Main text */
--muted      /* Secondary text */
```

The font families are also defined there, making it possible to change the visual identity without editing every component.

## Accessibility and Performance Notes

The portfolio includes a reduced-motion mode for users who have enabled motion reduction in their operating system. External CDN dependencies require an internet connection, while the core page structure and styling remain contained in `index.html`.

For production use, consider self-hosting fonts and JavaScript dependencies if the site must work in offline environments or under a strict Content Security Policy.

## Known Placeholders

The contact section currently contains placeholder links for LinkedIn and GitHub. Replace these values before presenting the portfolio as a finished professional website.

## License

This repository contains personal portfolio content and is intended for personal presentation. Unless otherwise stated, the design, written content, CV, and custom code are owned by Hadia Akbar. Contact the repository owner before reusing any personal content or visual assets.

## Contact

For professional inquiries, use the email address displayed in the portfolio contact section.

---

Built as a personal portfolio interface for **Hadia Akbar**.
