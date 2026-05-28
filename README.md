# Client Website Template

A generic, reusable blueprint for building modern client websites with integrated design system support. Use this as the starting point for any new client website project.

## Overview

This template provides a clean foundation that combines:

- A **Next.js + TypeScript** application shell
- A **two-layer design system** (agency base + client custom)
- A pragmatic source layout for pages, components, styles, and utilities

Clone this repository, rename it for your client (e.g., `client-website-{clientname}`), and start customizing.

## Structure

```
src/
├── design-system/       # Client-specific design tokens & components
│   ├── colors.ts
│   ├── typography.ts
│   └── index.ts
├── pages/               # Website pages
├── components/          # Reusable components
├── styles/              # Global styles
├── lib/                 # Utilities
└── types/               # TypeScript types
```

## Design System

This template is built around a two-layer design system so brand customization stays decoupled from shared infrastructure:

1. **Agency Base** (`@olmeda/design-system`)
   - Shared colors, spacing, typography
   - Base component structure
   - Updated centrally and consumed by all client projects

2. **Client Custom** (`src/design-system/`)
   - `{ClientName}` brand colors, typography, and tokens
   - Custom components specific to the client
   - Overrides and extensions to the agency base

## Getting Started

### 1. Create a new client project from this template

```bash
# Clone this template
git clone https://github.com/amandaalmeidda/client-website-template.git client-website-{clientname}
cd client-website-{clientname}

# Reset git history for the new client repo
rm -rf .git
git init
```

### 2. Update project metadata

- Update `package.json` `name` and `description` for `{ClientName}`
- Replace the README content with project-specific information
- Configure any environment variables required by the client

### 3. Install dependencies

```bash
npm install
```

### 4. Customize the design system

Edit the files in `src/design-system/` to reflect `{ClientName}` brand:

- `src/design-system/colors.ts` — brand and semantic colors
- `src/design-system/typography.ts` — fonts, sizes, weights
- `src/design-system/index.ts` — exports

## Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the site.

## Building

```bash
npm run build
npm start
```

## Scripts

| Command | Purpose |
|---------|---------|
| `npm run dev` | Start the local development server |
| `npm run build` | Create a production build |
| `npm start` | Serve the production build |
| `npm run lint` | Lint TypeScript/TSX sources |
| `npm run format` | Format sources with Prettier |

## Customizing Design System

The two-layer approach lets each client project diverge visually without forking the agency base:

- For shared changes (used by every client) — open a PR to `@olmeda/design-system`
- For client-specific brand expression — edit `src/design-system/` locally in this project

## When to use this template

Use this template when you need to spin up:

- A marketing or product website for a new client
- A landing page that should consume the agency design system
- Any standalone client web property where brand customization matters

Do **not** use this for purely internal tooling or non-website client deliverables.

## License

MIT
