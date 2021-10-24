# Updating Formats and Blocks

Each of these files is unique to the new site being built. Plan to edit every file below when you create the site, and when you launch the site. And for some files, many times in between.

1.  [Base Assets](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/capricorn/02_update_formats_blocks.md#base-assets)
2.  [Blocks](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/capricorn/02_update_formats_blocks.md#blocks)
3.  [Formats](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/capricorn/02_update_formats_blocks.md#formats)
4.  [Templates](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/capricorn/02_update_formats_blocks.md#templates)

## Structure for `New Instance: /_shared-capricorn`

These are the files that are unique to the new site or instance being created.

```
_shared-capricorn

|__ base-assets
    |__ event
    |__ interior
    |__ landing
    |__ sub-landing

|__ blocks
    |__ footer
    |__ head-data
    |__ metadata
    |__ schema

|__ formats
    |__ universal
        |__ base
        |__ cononical
        |__ header
        |__ id
        |__ noindex
    |__ home

|__ templates
    |__ Home
```

---

## Base Assets

-   [Explained in Site Setup](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/capricorn/01_site_setup.md#base-assets)

## Blocks

### :white_check_mark: Footer

#### `New Instance: /_shared-capricorn/blocks/footer`

-   This is where the footer HTML lives.
-   Every Cascade Instance has its own footer.
-   Scripts are not loaded in this block. All capricorn sites use the global `bottom-scripts` block.

### :white_check_mark: Head Data

#### `New Instance: /_shared-capricorn/blocks/head-data`

-   There are two sets of GTM scripts. Ask the Analytics team for the new GTM code.
    1.  The global GTM for all of St. Thomas
    2.  A script specific to the new instance

### :white_check_mark: Metadata

#### `New Instance: /_shared-capricorn/blocks/metadata`

-   This is where metadata tags like charset, links to favicons, and open graph image tags live.
-   Add `<meta name="robots" content="noindex, nofollow" />` to the top of this file during development.

### :white_check_mark: Schema

#### `New Instance: /_shared-capricorn/blocks/schema`

-   This is the SEO schema data.
-   Ask the Analytics team for updated schema data for the new site.

## Formats

### :white_check_mark: Base URL

#### `New Instance: /_shared-capricorn/formats/base`

-   We use the `<base>` element to set the base URL on the 404 page.
-   This region path appears in the configuration of all pages, but we only use it on the 404 page.

### :white_check_mark: Canonical

#### `New Instance: /_shared-capricorn/formats/universal/canonical`

-   This is the new site's development URL.
-   When the site is launched this is updated to the production URL.

### :white_check_mark: Header

#### `New Instance: /_shared-capricorn/formats/universal/header`

-   Some of the headers have an additional class like `edu` for unique CSS as needed
-   Update the `href` to the development URL during the new setup
-   When the site is launched the `href` is updated to the production URL

```html
<a class="header__logo-wrap edu" href="https://www.stthomas.edu"></a>
```

-   This is where the main navigation markup lives
-   This is where the search icon and off canvas **search drawer** lives
-   This file also has a **global breadcrumbs file import** at the bottom of the page
-   Breadcrumbs appear on Sub Landing and Interior pages

```xml
#if ($type == 'sublanding' || $type == 'interior')
    #import ('site://University of St. Thomas/_shared-capricorn/formats/universal/breadcrumbs')
#end
```

#### :dart: The Logo

-   All logos are SVGs
-   The logo class is `class="header__logo"`
-   The SVG has three additional classes to change the fill color depending on whether the user is on the homepage, landing, sub landing or interior page.
    -   The first two paths have classes of
        -   `<path class="divider" ...`
        -   `<path class="st-thomas" ...`
    -   The last group has a class of
        -   `<g class="common-good" ...`
-   When creating a new site, ask the creative team (usually John Mau) for a new logo, or lockup
    -   Specify that you need a color SVG
    -   Edit the SVG to match the markup of the main site's logo
    -   See the [University of St. Thomas Logo](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/svgs/edu-logo.svg?short_path=6d5bd80) as an example

### :white_check_mark: ID

#### `New Instance: /_shared-capricorn/formats/universal/id`

-   A meta tag to create content ids for each page

### :white_check_mark: Noindex

#### `New Instance: /_shared-capricorn/formats/universal/noindex`

-   This isn't specific to each site, but I like having it on each site
-   Use this meta tag as needed on individual pages by editing the page configuration

### :white_check_mark: Home

#### `New Instance: /_shared-capricorn/formats/home`

-   This is the homepage, which is basically a header, slider and footer
-   **These styles are heavily intertwined with the styles for all sliders and hero images**
-   Be extra careful to test all hero and banner modules on desktop and mobile before pushing to production
    -   The styles are global for all Capricorn sites
    -   The module is not global, it is specific to each site
    -   If editing both the module and styles, each site's module needs to be updated
    -   **To do:** Should we break up the styles on a per site basis?

## Templates

### :white_check_mark: Home

#### `New Instance: /_shared-capricorn/templates/Home`

-   Templates are the core page structure
-   Templates are specified for a page layout in **Manage Site > Configurations**
-   Template Regions `<system-region name=""/>` are how **Region Paths** are added to page configurations
-   There are two templates
    -   Home
        -   Specific to the site
    -   Universal
        -   Global - lives in `University of St. Thomas: /_shared-capricorn/templates/Universal`
