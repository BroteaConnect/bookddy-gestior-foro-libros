# Bookddy

Gestor y foro de libros — una red social de libros: organiza tu biblioteca,
guarda lo que lees y comparte reseñas con otra gente lectora.

Landing page with a requirements form, generated from Brotea's
`landing-astro` template.

## Copy and design
- User-facing copy lives in `src/locales/<code>.json` (all shipped languages)
  and reaches the UI through `t(locale, key)` — never hardcoded.
- Colors and spacing come from theme tokens in `src/styles/theme.css`.
- `src/locales/locales.test.mjs` fails the build if a language is missing keys.

## Configuration
- `PUBLIC_REQUIREMENTS_ENDPOINT` — URL that receives the form's JSON POST
  (`{project, source, submitted_by, content}` → requirements table).
  Defaults to `https://api.brotea.dev/requirements`.

## Commands
- `npm install` · `npm run dev` · `npm run build` (output in `dist/`)
- `npm test` — build stamp + locale checks + full Astro build
