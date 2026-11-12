# Foundora homepage — exact source export

React + TypeScript + Vite source of the published homepage.
Source revision: 4d432bac7114094d68e6b7d55178e2efae66b638.
No redesign or runtime code changes have been made for this export.

## Requirements and installation

Use Node.js 22 LTS and npm. All dependencies are public npm packages.
No private build plugins, API keys or hosting account are required.

```sh
npm ci
npm run dev
```

Open the URL printed by Vite. To build and preview production:

```sh
npm run build
npx vite preview
```

Upload the contents of `dist/` to any static web host. A prebuilt copy is included.

## Editing

- `src/main.tsx`: reusable components, all homepage sections, responsive navigation,
  item illustrations, interactive journey and coming-soon messages.
- `src/style.css`: complete responsive styles, animations, focus states and
  reduced-motion support.
- `src/config.ts`: logo path and configurable future application links.
- `public/`: bundled, optimised workplace and hotel photography.
- `index.html`: SEO metadata and application entry point.
- `package.json` and `package-lock.json`: scripts, dependencies and locked versions.

## Original logo integration

The published version uses plain-text brand placements because the original logo
file was not available at publication. This export preserves that exact appearance.
The logo image displayed in the export request was not exposed as an accessible
attachment file, so its original bytes are not included or recreated.

The existing Brand component already supports the original logo in the navigation
and footer. To activate it, save the unmodified original file to
`public/foundora-logo.png` and set `logoUrl: '/foundora-logo.png'` in `src/config.ts`.
Use the actual extension if different. Then rebuild. Existing CSS preserves its
proportions with `object-fit: contain` and applies no colour filters.

## Functionality and external resources

The project is frontend-only. Empty application URLs display accessible
coming-soon messages. The Holiday Inn link points to https://hotel.foundora.co.uk/.
No authentication, actual QR scanning, notifications, database or API is implemented.

Inter loads from public Google Fonts with a sans-serif fallback. No private
external dependencies are required. Photography is bundled locally, sourced from
Unsplash. Product visuals and hotel imagery are illustrative.

## Validation

TypeScript and the production Vite build pass. Internal section links were checked.
Browser rendering and console behavior remain unverified because this environment
has no callable browser-control tool.
