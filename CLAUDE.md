# Claude AI Assistant Guidelines

## Project Context
This is an Astro + TypeScript frontend project with Tailwind CSS. When working on this codebase, you must adhere to the established conventions and patterns.

## Important Instructions

### 1. Project Structure Compliance
**ALWAYS** follow the structure and conventions defined in `README.project-structure.md` when:
- Creating new files or folders
- Organizing code modules
- Naming files, folders, functions, types, components, etc.
- Implementing features or pages

### 2. Rules and Patterns
**ALWAYS** check the `rules/` folder for specific implementation patterns before:
- Creating components → See `rules/components-and-pages.md`
- Implementing services → See `rules/service-layer.md`
- Managing styles → See `rules/styling-guidelines.md`
- Writing tests → See `rules/testing-guidelines.md`
- Implementing any feature that might have established patterns

### 3. Code Generation Guidelines
When generating or modifying code:
1. First, understand the existing patterns in the codebase
2. Check if there are similar implementations to reference
3. Follow the established naming conventions strictly
4. Place files in the correct folders according to the project structure
5. Use appropriate component patterns based on interactivity needs

### 4. Key Conventions Summary
- **File/Folder naming**: `kebab-case` (use `_kebab-case` for feature-specific modules)
- **Components/Types/Classes**: `PascalCase`
- **Functions/Variables/Props**: `camelCase`
- **API data**: `snake_case` for JSON request/response
- **Package Manager**: Always use `pnpm`
- **Framework**: Astro
- **Styling**: Tailwind CSS (primary), component styles, CSS modules
- **Validation**: Zod
- **Testing**: Vitest (if applicable)

### 5. Before Making Changes
Always:
1. Read the relevant documentation in `README.project-structure.md`
2. Check for existing patterns in `rules/` folder
3. Look for similar implementations in the codebase
4. Maintain consistency with existing code style
5. Run all checks for TypeScript and linting: `pnpm check:all` (if available)

### 6. When Creating New Features
Follow this checklist:
- [ ] Determine if it's a shared module or feature domain
- [ ] Create the appropriate folder structure as defined in the project structure
- [ ] Follow the naming conventions for all files and exports
- [ ] Check rules folder for implementation patterns
- [ ] Use existing utilities and shared modules when possible
- [ ] Implement proper TypeScript types
- [ ] Use Zod for external data validation
- [ ] Ensure components are accessible
- [ ] Optimize images using Astro's Image component

### 7. Component Development
- **Astro Components**: For static or server-rendered content
- **Interactive Components**: Use React/Vue/Svelte with proper hydration directives
- **Styling**: Prefer Tailwind classes, use component styles for specific needs
- **Props**: Define proper TypeScript interfaces
- **Composition**: Prefer composition over inheritance

### 8. Performance Considerations
- Use partial hydration for interactive components
- Optimize images with Astro's Image component
- Minimize JavaScript bundle size
- Leverage Astro's static generation when possible
- Use proper loading strategies for external resources

### 9. Checks Commands
- `pnpm build` - Build for production
- `pnpm dev` - Run development server
- `pnpm preview` - Preview production build
- `pnpm check` - Type check (if configured)
- `pnpm format` - Format code with Prettier (if configured)
- `pnpm lint` - Lint code (if configured)

Remember: Consistency and adherence to established patterns is crucial for maintaining a clean, scalable codebase.