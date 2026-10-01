# Pipita landing page

Responsive, static HTML + CSS + JavaScript. No build step or dependencies.

Open `index.html` directly, or run `python3 -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Content status

Product copy is adapted from the user-provided `Pipita - Description.pdf`: browser-based practice management for healthcare providers in Curaçao, including scheduling, patient information, SVB declarations, invoicing, and data safeguards. The time-saving example is explicitly scoped to one physiotherapist with 50 patients (monthly SVB claims preparation reduced from 16 to 2 hours); it is not presented as a guaranteed result. Future expansion is described as planned, not already available. No launch date is asserted because the numeric date in the document is ambiguous. Papiamentu is a draft translation and should receive a fluent speaker's review.

The page includes the hero and app preview, three healthcare category cards, three feature columns, a two-phone product section, gradient CTA, accessible FAQ accordions, and footer. Fake ratings, customer counts, prices, legal policies, and social accounts have intentionally not been invented.

All three languages live in `translations` in `script.js`. The selectors update the whole page, document language, title, and description; the selection is persisted in local storage when available. Direct links: `?lang=en`, `?lang=nl`, `?lang=pap`. Language switching requires JavaScript. Google Fonts is optional; system sans-serif fallbacks work offline.

Set `config.signupUrl` in `script.js` to the actual onboarding URL. Until then, CTA buttons open a clear preview notice. No forms send or store personal information.

## Image handoff

Supply original exports without device frames, added text, rounded corners, or shadows. CSS provides those treatments. All dimensions below are recommended source sizes; larger originals are welcome.

| Asset | Recommended size | Format / notes |
| --- | --- | --- |
| Logo | SVG preferred; PNG at least 600 px wide | Transparent background; dark and white variants. Temporary text wordmark appears in header and footer. |
| Desktop app screenshot | 2400 × 1400 px | PNG or WebP, approximately 12:7. Replaces `.browser` contents. |
| Mobile calendar screenshot | 900 × 1800 px | PNG or WebP, 1:2. Reused in hero and product section. |
| Mobile patient/profile screenshot | 900 × 1800 px | PNG or WebP, 1:2. Replaces `.profile` contents. |
| Healthcare photos (3) | 1200 × 1200 px each | WebP or high-quality JPEG. Subject centered with space around edges; cropped to 6:5 on desktop and 3:2 on mobile. Keep the lower quarter clear for category labels. |
| Optional favicon | SVG or 512 × 512 px PNG | Square brand mark. |

Business photo slots are marked `data-image-slot="business-1"` through `business-3` (physiotherapy, psychology, and other care professionals). Add images with `width:100%; height:100%; object-fit:cover; position:absolute; inset:0`, remove `.placeholder-icon` and `.image-note`, and keep the existing gradient and headings. Use empty alt text for decorative photos already described by category headings. For app screenshot replacements, preserve the surrounding translated accessible preview label and use empty alt text on the images inside it.

If screenshots contain readable interface text, localized versions for all three languages are ideal. Otherwise the marketing page can translate while app images retain the source language.

## Before publishing

Review the translations, connect onboarding, add final assets, and remove the preview notice. The PDF specifies a monthly subscription but supplies no prices or onboarding URL, so those remain unset. Add genuine privacy, terms, and contact destinations when supplied. For search-indexed language versions, consider separate pre-rendered language pages; this version switches language in the browser.
