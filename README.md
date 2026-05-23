# Brasil Te Ama — Website & Design System

Official website for Brasil Te Ama with integrated design system.

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

This project uses two design systems:

1. **Agency Base** (`@olmeda/design-system`)
   - Shared colors, spacing, typography
   - Base component structure

2. **Client Custom** (`src/design-system/`)
   - Brasil Te Ama brand colors & typography
   - Custom components for this client

## Installation

```bash
npm install
```

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

## Customizing Design System

Edit `src/design-system/colors.ts` and `src/design-system/typography.ts` to customize the brand appearance.

## License

MIT
