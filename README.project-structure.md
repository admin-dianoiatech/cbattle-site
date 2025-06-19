# Project Structure & Code Organization

## Package Manager
- Use `pnpm` for all package installations and management

## Core Libraries and Versions
- Astro: ^4.x.x
- TypeScript: ^5.x.x
- Tailwind CSS: ^3.x.x
- Zod: ^3.x.x (for validation)
- React: ^18.x.x (if using React integrations)
- Node: LTS version (check .nvmrc)

## Naming Conventions
- `kebab-case` - for all folders/files
- `_kebab-case` - for feature domain's specific common modules
- `PascalCase` - for classes, types, and Astro components
- `snake_case` - for API request/response params and JSON data
- `camelCase` - for functions, variables, and props

## Miscellaneous Folders
- `public` - for static assets (images, fonts, etc.)
- `docs` - for any to-do plan workflows or documentation
- `prompts` - for prompts format
- `rules` - for standards or rules of the repo
- `.husky` - for husky configuration (if applicable)

## Common Modules
- `assets` - for images, SVGs, and other assets imported in code
- `components` - for reusable Astro/React/Vue components
  - `components/ui` - for basic UI components (buttons, cards, etc.)
  - `components/layout` - for layout components (header, footer, etc.)
  - `components/features` - for feature-specific components
- `layouts` - for page layouts
- `pages` - for Astro pages (routing)
- `lib` - for 3rd party integrations and utilities
- `utils` - for utility functions
- `types` - for TypeScript type definitions
- `constants` - for constant values
- `services` - for API calls and external service integrations

## Domain Folders
- `src` - main source code and shared common modules
- `src/features` - main features folder **(Only if necessary)**

## Files
- `astro.config.mjs` - Astro configuration
- `tailwind.config.mjs` - Tailwind CSS configuration  
- `tsconfig.json` - TypeScript configuration
- `src/env.d.ts` - environment type definitions

## Shared Modules Structure
Shared modules follow this structure:

```
src/
├── assets/                 # Images, SVGs, and other assets
├── components/             # Reusable components
│   ├── ui/                 # Basic UI components
│   ├── layout/             # Layout components
│   └── features/           # Feature-specific components
├── constants/              # Shared constants
├── layouts/                # Page layouts
├── lib/                    # 3rd party integrations
├── pages/                  # Astro pages (routing)
├── services/               # API calls and external services
├── styles/                 # Global styles
├── types/                  # Shared types
└── utils/                  # Shared utilities
```

## Feature Domain Structure (Optional)
When creating new feature files, follow this structure:

```
src/features/<feature-name>/
├── index.ts                # Feature's entry point
├── _assets/                # Feature's assets
├── _components/            # Feature's components
├── _constants/             # Feature's constants
├── _lib/                   # Feature's 3rd party integrations (only if necessary)
├── _services/              # Feature's API calls
├── _styles/                # Feature's styles
├── _types/                 # Feature's types
└── _utils/                 # Feature's utilities
```