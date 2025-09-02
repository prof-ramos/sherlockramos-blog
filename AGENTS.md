# Repository Guidelines

This repository hosts a Docusaurus site (docs, blog, and a small React UI layer). Use Node 18+ and Yarn.

## Project Structure & Module Organization
- `docs/`: Documentation in Markdown/MDX; sidebar in `sidebars.js`.
- `blog/`: Blog posts (`YYYY-MM-DD-title.md[x]`), `authors.yml`, `tags.yml`.
- `src/`: UI code — `components/` (PascalCase React components), `pages/` (route pages), `css/`.
- `static/`: Static assets served at site root (e.g., `img/`).
- `docusaurus.config.js`: Site configuration; broken links fail builds.

## Build, Test, and Development Commands
- Install deps: `yarn`
- Local dev: `yarn start` (hot reload at localhost)
- Production build: `yarn build` (outputs to `build/`)
- Preview build: `yarn serve` (serves `build/`)
- Clear caches: `yarn clear`
- Theme override (advanced): `yarn swizzle <theme> <component>`

## Coding Style & Naming Conventions
- Indentation: 2 spaces; keep lines concise and readable.
- Components: PascalCase filenames in `src/components` (e.g., `HeroBanner.tsx` or `.jsx`).
- Routes/Docs slugs: kebab-case (e.g., `/getting-started/`).
- Blog posts: `YYYY-MM-DD-my-post.mdx`; include frontmatter (`title`, `tags`, optional `slug`).
- Imports: prefer relative within `src/`; group by external → internal.
- Formatting/Lint: none enforced here — match existing style; run Prettier locally if available.

## Testing Guidelines
- No unit test suite; validate by:
  - Running `yarn start` and exercising pages with no console errors.
  - Running `yarn build`; build throws on broken links (`onBrokenLinks: 'throw'`).
  - Checking code blocks render (use fenced blocks with language, e.g., ```ts).

## Commit & Pull Request Guidelines
- Commits: imperative mood (“Add …”, “Fix …”); concise scope in subject; reference issues (`#123`) when relevant.
- PRs: clear description of changes, screenshots/GIFs for UI or content diffs, reproduction steps, and impact on navigation/links.
- Keep PRs focused; note any follow-ups. Ensure `yarn build` passes before requesting review.

## Security & Config Tips
- Do not commit secrets; this site is static. Update external links to use HTTPS. Review `docusaurus.config.js` before changing URL/baseUrl or GitHub Pages settings.

