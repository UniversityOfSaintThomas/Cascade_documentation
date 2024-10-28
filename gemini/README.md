# `_shared-gemini/`

## `_blocks/`

```
These are the unique, editable footers that belong in each site.
|__ footer
|__ landing-footer
```

## `_cms/`

```
Base Assets are unique to each site.
|__ base-assets/
	|__ college-landing
	|__ program
	|__ secondary
	|__ tertiary

The head files link to the fonts, CSS and JavaScript.
This is a global file.
|__ blocks/
	|__ head-files

Some formats are global, and some formats are unique to each site.
|__ formats/
	|__ _shared/

		Each site should have it's own set of unique, editable header files.
		Also unique to each site because they #import the Utilities format
		|__ header/
			|__ header
			|__ header-landing
			|__ header-main

		|__ base - Global
		|__ canonical - Global
		|__ footer - Unique to each site. See '_blocks/' to edit site footers.
		|__ id - Global
		|__ noindex - Can be global, but easier to keep one in each site.
		|__ open-graph - Each site has unique open-graph meta tags.
		|__ sidebar- - Unique to each site because they #import the Utilities format
		|__ site-name - Global
		|__ skip-links - Global
		|__ utilities - Unique to each site. Sets up site variables.

	|__ components/
		All module formats go here.
		This is a global set of formats/files.

	|__ home/
		Unique to each site because they #import the Utilities format
		|__ hero

	|__ page/
		Unique to each site because they #import the Utilities format
		|__ default
		|__ hero-breadcrumbs

		I think this can be removed.
		Program Finder is a Vue JS component.
		|__ program-finder

|__ templates
	Global template for all pages.
	|__ HTML
```

## `assets/`

SVGs and PNGs

## Configurations (Home & Page)

### Settings

| Template | Location | Path                                  |
| -------- | -------- | ------------------------------------- |
| HTML     | Global   | `_shared-gemini: _cms/templates/HTML` |

### Regions

| Region            | Location | Path                                                                 | Type   |
| ----------------- | -------- | -------------------------------------------------------------------- | ------ |
| Base:             | Global   | `_shared-gemini: _cms/formats/_shared/base`                          | format |
| Canonical:        | Global   | `_shared-gemini: _cms/formats/_shared/canonical`                     | format |
| Compare:          |          |                                                                      |
| Custom CSS:       |          |                                                                      |
| Default:          | Unique   | `Alumni STAGING: /_shared-gemini/_cms/formats/page/default`          | format |
| Footer:           | Unique   | `Alumni STAGING: /_shared-gemini/_cms/formats/_shared/footer`        | format |
| Head Files:       | Global   | `_shared-gemini: /_cms/blocks/head-files`                            | block  |
| Header:           | Unique   | `Alumni STAGING: /_shared-gemini/_cms/formats/_shared/header/header` | format |
| Hero-Breadcrumbs: | Unique   | `Alumni STAGING: /_shared-gemini/_cms/formats/page/hero-breadcrumbs` | format |
| ID:               | Global   | `_shared-gemini: /_cms/formats/_shared/id`                           | format |
| Noindex:          |          |                                                                      |
| Open Graph:       |          |                                                                      |
| Schema:           |          |                                                                      |
| Site Name:        | Global   | `_shared-gemini: /_cms/formats/_shared/site-name`                    | format |
| Skip Links:       | Global   | `_shared-gemini: /_cms/formats/_shared/skip-links`                   | format |

## Content Types

### Home

| Type            | Name            | Location | Path                                    |
| --------------- | --------------- | -------- | --------------------------------------- |
| Configuration   | Home            | Unique   | `Alumni STAGING: Configurations/Home`   |
| Metadata Set    | Page            | Unique   | `Alumni STAGING: Metadata Sets/Page`    |
| Type of Content | Data Definition |          |                                         |
| Data Definition | Home            | Global   | `_shared-gemini: Data Definitions/Home` |

### Page

| Type            | Name            | Location | Path                                    |
| --------------- | --------------- | -------- | --------------------------------------- |
| Configuration   | Page            | Unique   | `Alumni STAGING: Configurations/Page`   |
| Metadata Set    | Page            | Unique   | `Alumni STAGING: Metadata Sets/Page`    |
| Type of Content | Data Definition |          |                                         |
| Data Definition | Page            | Global   | `_shared-gemini: Data Definitions/Page` |
