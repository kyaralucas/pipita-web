# Pipita landing page

Responsive, static HTML + CSS + JavaScript. No build step or dependencies.

Open `index.html` directly, or run `python3 -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Search and link previews

`index.html` contains the search description, canonical URL, Open Graph tags, and Twitter large-image card tags. Link previews use the English title and description and `images/Desktop_Screenshot_Pipita.png`; these tags are static so preview crawlers do not need JavaScript. Language switching updates the browser title and search description, but social previews remain English for all language query parameters.

Metadata changes and image assets must be deployed before external share previews can use them. Existing previews may be cached by the sharing platform. The page content still renders with JavaScript; separate pre-rendered language pages would be needed for language-specific static previews.
