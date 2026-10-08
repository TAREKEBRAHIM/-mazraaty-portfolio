# Tarek Ibrahim — Mazraaty Application Portfolio

A bilingual, unofficial social media concept portfolio. Built with HTML, CSS and vanilla JavaScript only, with no build dependencies. Arabic is the default; English switches instantly and the choice is saved on the current browser.

## Files
- `index.html`: semantic, pre-rendered Arabic page, SEO and Open Graph title/description, viewport and favicon.
- `css/style.css`: mobile-first design, RTL/LTR logical properties, responsive grids, dialog and reduced-motion support.
- `js/main.js`: both translation records, section templates, language storage, navigation, Reel preview and local Story interactions.
- `assets/images/ima-*.png`: farm photography used by the hero, posts, Reel preview and Stories.
- `assets/images/profile/`: portrait and favicon placeholders.
- `PLAN.md`: decisions recorded before implementation.
- `PROGRESS.md`: completed work and verification results.

## Sections
Header → Hero → Why I fit → Content samples → AI Reel → Instagram Stories → Content strategy → Weekly calendar → Skills → About → Contact → Disclaimer/footer.

## Open locally
Open `index.html` directly in a modern browser. For a consistent localStorage origin, use VS Code Live Server, or serve the directory with an existing static server. No installation or build step is required.

Optional, if Python is installed:
```sh
python -m http.server 8000
```
Then visit `http://localhost:8000`. File-based localStorage behavior varies by browser; HTTP is preferred for checking preference persistence.

## Edit the content
Edit the corresponding entries in **both** `translations.ar` and `translations.en` in `js/main.js`. The renderer updates all content, alt text, accessible labels and metadata. Keep the Arabic fallback in `index.html` synchronized for visitors without JavaScript and initial rendering.

If Node is available, regenerate the Arabic fallback after translation/template changes with this one-time terminal command (run in Git Bash in the project directory; for PowerShell, edit the Arabic fallback directly):
```sh
node -e "const fs=require('fs');const {buildPage}=require('./js/main.js');const p='index.html';const s=fs.readFileSync(p,'utf8');fs.writeFileSync(p,s.replace(/<div id=\"page\">[\s\S]*<\/div>\s*<\/body>/,'<div id=\"page\">'+buildPage('ar')+'</div>\n</body>'));"
```
When changing the Arabic SEO title/description, also update the initial `<head>` metadata in `index.html`. Styles are controlled by CSS variables at the top of `css/style.css`.

## Farm photography
The hero, four content samples, Reel preview and three Stories use the local PNG photographs in `assets/images/`. Their paths and bilingual alternative text are configured in `IMAGE_ALT`, `POST_IMAGES` and `STORY_IMAGES` in `js/main.js`.

The About section still uses a portrait placeholder because no personal portrait was supplied. Replace it only with an approved photo of Tarek; `assets/images/profile/favicon.svg` can also be replaced with a personal mark.

## Contact email
Find `CONTACT_EMAIL` near the beginning of the shared code in `js/main.js` and fill in the empty string. The source includes an explicit placeholder comment. Until then, the button shows a bilingual 'contact details not added' notice. No email address or contact service is invented.

## Reel and Stories
The Reel is a 30-second **animated six-scene storyboard**, with play, pause, replay, Escape/backdrop close and focus restoration. It is not a rendered AI video. Replace the preview with a final local video later if you create one. Story poll/quiz choices and question previews are local demonstrations; questions are never submitted to Mazraaty or any server.

## Deploy on GitHub Pages
1. Create a GitHub repository and upload `index.html`, `css`, `js`, `assets` and the Markdown files to the repository root. Do not put the project inside an extra nested folder.
2. Open repository **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose `main` and `/ (root)`, then save.
5. Wait for GitHub to show the published URL, normally `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.
6. Open the published URL and check both languages and contact behavior.

All asset URLs are relative, so project-subdirectory GitHub Pages URLs work. No custom domain or build configuration is required. Add your final URL as `og:url` in `index.html` if desired. No publication was performed by the assistant.

## Accessibility and dependencies
Native buttons, labeled input, visible keyboard focus, skip link, native modal dialog, semantic headings, localized image descriptions and reduced-motion styles are included. Current Chrome, Edge, Firefox and Safari support the native dialog API. Cairo is optionally loaded from Google Fonts; Tahoma/Arial fallbacks keep the site readable without network access. There are no external image URLs, JavaScript libraries, analytics or translation APIs.

## Truthful positioning
All work is clearly identified as an unofficial application concept. There are no invented metrics, paid-campaign claims, prior Mazraaty employment claims or years of Social Media Specialist experience.
