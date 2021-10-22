# Updating Formats and Blocks

## Structure for `New Instance: _shared-capricorn`

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
        |__ hero-slider
        |__ id
        |__ noindex
    |__ home

|__ templates
    |__ Home
```

### Footer

#### `New Instance: _shared-capricorn > blocks > footer`

-   This is where the footer HTML lives. Every Cascade Instance has its own footer. Scripts are not loaded in this block. All capricorn sites use the global `bottom-scripts` block.

### Head Data

#### `New Instance: _shared-capricorn > blocks > head-data`

-   This is where GTM scripts and CSS files live.
-   There are two sets of GTM scripts. The first is the global GTM for all of St. Thomas. The second is a script specific to the new instance.

### Metadata

#### `New Instance: _shared-capricorn > blocks > metadata`

-   This is where garden variety metadata tags live like charset, links to favicons, and open graph image tags.

### Schema

#### `New Instance: _shared-capricorn > blocks > schema`

-   This is the SEO schema data. Ask Kathy on the Analytics team for updated schema data for the new site.

### Base URL

#### `New Instance: _shared-capricorn > formats > base`

-   We use the `<base>` element to set the base URL on the 404 page. You'll see this region path when you edit the configuration of all page, but we only use it on the 404 page.

### Canonical

#### `New Instance: _shared-capricorn > formats > universal > canonical`

-   Update this to the new site's URL.
-   I update this to the new site's development URL, and then again to the production URL when the site is launched.
