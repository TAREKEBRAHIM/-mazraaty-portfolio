# Implementation plan

## Purpose and truthful positioning
Create a bilingual social media concept portfolio for Tarek Ibrahim Abdullah's application to Mazraaty. Lead with content work, industry understanding, visual thinking and AI-assisted planning. Never imply employment at Mazraaty, campaign results or years of professional social media experience. Display the supplied unofficial-project disclaimer.

## Page structure
1. Minimal sticky header and language controls
2. Hero: animal-production knowledge meets digital content
3. Four fit cards
4. Four detailed educational/social post mockups
5. AI-assisted reel: timed six-scene preview, storyboard and prompt
6. Three interactive story mockups
7. Five content pillars
8. Seven-day weekly calendar
9. Relevant skill chips
10. About Tarek
11. Contact CTA with an honest email-not-configured state
12. Disclaimer and footer

## Design system
Editorial social-content direction, rounded cards, strong section typography, fine borders, generous but compact spacing and restrained motion. Content previews use local, replaceable typographic graphic placeholders; no remote image dependencies or fabricated company identity.

## Palette
Deep navy #112b36, forest green #245b46, fresh green #d8efb0, warm beige #f4eee2, white #ffffff, soft gray #eef2f1. Primary dark text and dark buttons maintain readable contrast.

## Typography
Arabic: Cairo with system sans-serif fallbacks. English: clean system sans-serif. Use readable body sizes (16px minimum), larger headlines, generous Arabic line height, and no Arabic letter spacing. Font loading is optional; site works without network fonts.

## Responsive strategy
Mobile-first single columns; fit cards and samples grow to 2 columns, storyboard and pillars use adaptive grids. Hero becomes two columns on larger screens. Calendar wraps rather than scrolling horizontally. Check 375, 768, 1024 and 1440px in both languages, including modal and mobile menu.

## Bilingual strategy
Arabic initial document with lang=ar and dir=rtl. Central JS translation object drives all visible copy, accessible labels, alt text, page title, description and Open Graph metadata. AR/EN switches immediately and persists via guarded localStorage. CSS logical properties support both directions. Render Arabic content before interaction, with functional anchors without JavaScript.

## Content plan
Use all supplied titles, captions, objectives, CTAs, storyboard scenes, stories, pillars, calendar, skills and biography. Render original captions in full. Clearly identify mockups and AI-assisted concept; the reel is an animated storyboard, not a completed video. No invented metrics. Contact email remains blank with a source comment and localized notice.

## Assets and implementation
Only index.html, css/style.css and js/main.js; local SVG typographic placeholder panels under assets/images/{posts,reel,stories,profile}. Each placeholder gets a replacement HTML comment. Add site favicon placeholder. No frameworks, build step or translation service.

## Verification and delivery
Check JS syntax, translation completeness, local assets and anchors. Use browser automation if available for both languages at requested widths, storage persistence, menu, focus/modal, stories and buttons. Record actual results and limits in PROGRESS.md. README explains editing, running locally and GitHub Pages deployment. Do not publish to another provider: user's requested destination is GitHub Pages.
