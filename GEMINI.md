# Alternative Everything - Project Context

## Project Overview
**Alternative Everything** is a website project built with Astro, dedicated to promoting intentional living, community building, and sustainable alternatives to conventional societal systems (food, education, economy). The project is likely a migration or redesign of an older HTML/CSS-based site (found in `oldsite/`).

### Main Technologies
- **Astro (v6.x):** Modern web framework for content-driven websites.
- **Tailwind CSS (v4.x):** Utility-first CSS framework integrated via Vite.
- **Vite:** Build tool and development server.
- **TypeScript:** Used for type-safe Astro components and scripts.
- **Font Awesome (v4.7.0):** Used for icons, integrated via CDN in the layout.
- **Google Tag Manager:** Integrated for analytics.

### Architecture
- `src/pages/`: Contains the route-based pages (`index.astro`, `about.astro`, `contact.astro`, `our-values.astro`).
- `src/layouts/Layout.astro`: The primary layout component wrapping all pages, including navigation and footer.
- `src/components/`: Reusable UI components like `Nav.astro`, `Footer.astro`, `Header.astro`, `Button.astro`, and `ContactForm.astro`.
- `src/styles/global.css`: Global stylesheet containing Tailwind imports, CSS variables for the color palette, and custom styles (including legacy styles and responsive overrides).
- `public/`: Static assets such as images (`.png`, `.jpg`, `.svg`) and favicons.
- `oldsite/`: Legacy version of the site (HTML/CSS), used for reference during migration.

## Building and Running
All commands are run from the root of the project using `npm`.

| Command | Action |
| :--- | :--- |
| `npm install` | Installs project dependencies. |
| `npm run dev` | Starts the local development server at `http://localhost:4321`. |
| `npm run build` | Builds the production-ready site into the `./dist/` directory. |
| `npm run preview` | Previews the production build locally. |
| `npm run astro ...` | Runs Astro CLI commands (e.g., `astro add`, `astro check`). |

## Development Conventions

### Styling
- **Tailwind CSS 4:** Use Tailwind utility classes where possible. Note that the project uses `@import "tailwindcss";` in `src/styles/global.css`.
- **CSS Variables:** Global colors are defined in `:root` within `src/styles/global.css`. Use these variables (`var(--primary)`, `var(--secondary)`, etc.) for consistency.
- **Custom Shapes:** The project uses SVG-based shape dividers (classes like `.custom-shape-divider-bottom-1709772170`).

### Components and Layouts
- **Layouts:** All pages should be wrapped in `Layout.astro` to ensure consistent navigation, footer, and metadata (GTM, Font Awesome).
- **Navigation:** Managed via `src/components/Nav.astro`.
- **Footer:** Managed via `src/components/Footer.astro`.

### Images
- Place new images in the `public/` directory and reference them with absolute paths (e.g., `/my-image.png`).

### Legacy Reference
- When implementing new features or sections, refer to the corresponding files in `oldsite/` if you are replicating existing functionality or content.
