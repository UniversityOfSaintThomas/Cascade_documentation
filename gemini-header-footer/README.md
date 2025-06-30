# Gemini Header &amp; Footer

## Files Added

| File                          | Type       | Notes                                                          |
| ----------------------------- | ---------- | -------------------------------------------------------------- |
| `_gemini_footer-landing.scss` | SCSS       | Footer Landing Styles '.FooterLanding'                         |
| `_gemini_footer.scss`         | SCSS       | Footer Styles '.Footer'                                        |
| `_gemini_header-landing.scss` | SCSS       | Header Landing Styles '.HeaderLanding'                         |
| `_gemini_header.scss`         | SCSS       | Header Styles '.Header'                                        |
| `_gemini_props.scss`          | SCSS       | Gemini foundational styles, scoped to Gemini Header and Footer |
| `_gemini_utility.scss`        | SCSS       | Gemini foundational styles, scoped to Gemini Header and Footer |
| `js/scripts/gemini-header.js` | JavaScript | Open/Close subnav when `<button>` is clicked                   |
| `js/scripts/expand.js`        | JavaScript | This script enables expandable UI elements                     |
| `js/scripts/scroll.js`        | JavaScript | Scroll attribute on `<html>` for sticky nav                    |

### Scoped Styles

All files are scoped to the class names specific to the Gemini Header &amp; Footer. The JavaScript and styles won't run unless the Header and Footer are added to the page.

### `js/scripts/expand.js`

This script enables expandable UI elements (like toggles, popups, or accordion groups) using the `data-expand` attribute, while also supporting focus trapping for accessibility inside popups or modals. It's meant to be run once on page load or when the DOM is ready.

### `js/scripts/scroll.js`

This script adds a data attribute (`data-scroll`) to the `<html>` element based on the user's scroll direction or position relative to the header. It also adds a CSS hook (`.js-header`) to `<body>` for styling Gemini-specific headers.

### `.js-header` Class

Some styles rely on `.js-header` as a body class, so I'm adding it via scroll.js. If the page loads too slow, you'll probably see a jump in white space at the top of the page while the DOM is loading. I recommend adding `.js-header` to the `<body>` element in the template when the Header and Footer are added to production sites. It's added with JavaScript while the current (old) Header and Footer are still in place.

### `js/scripts/gemini-header.js`

This script powers accessible, interactive headers for a site that appears to have two header variants (`.Header__main` and `.HeaderLanding__main`). It handles:

-   Menu and submenu toggling
-   Smooth scrolling to headers
-   Focus trapping for keyboard users
-   Resetting state on resize or outside clicks
-   Search input focus
