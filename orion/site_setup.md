# Site Setup (EDITING IN PROGRESS)

### There are 7 Asset Factory items for Orion

-   Academic Calendar
-   Course Detail
-   Degrees and Programs
-   Faculty-Staff Profile
-   Landing Page
-   Story Page
-   Universal Page

-   Orion example

```
_shared/_cms/base assets/academic-calendar -> Orion Template/_shared-orion/_cms/base assets/academic-calendar
```

## Site Specific Files

### Root Orion Structure

This is the core structure of a site using the Orion Template. We use this template to create all new sites using Orion.

Each Orion site contains a `_shared-orion` directory that is specific **_to that site_**.

```
Orion Template Structure
|__ 404

|__ _beta
    |__ angela
        |__ private
        |__ public
    |__ ashley
        |__ private
        |__ public
    |__ codi
        |__ private
        |__ public
    |__ ed
        |__ private
        |__ public
    |__ jennifer
        |__ private
        |__ public

|__ _external-links
    |__ 404-page-links

|__ _media-library
    |__ _copy-folder
        |__ 1025x770
        |__ 1200x1200
        |__ 1200x800
        |__ 1920x1080
        |__ 770x1025
        |__ 770x575
    |__ _documents
    |__ _images
    |__ _placeholder-images

|__ _rss
|__ _shared-orion
|__ index
|__ site-setup
```

-   Orion Template > \_shared-orion > \_cms > base assets > \* (everything in this folder)

-   Orion Template > \_shared-orion > \_cms > blocks > footer
-   Orion Template > \_shared-orion > \_cms > blocks > xml > head files
-   Orion Template > \_shared-orion > \_cms > blocks > xml > mobile header
-   Orion Template > \_shared-orion > \_cms > blocks > xml > top body scripts
-   Orion Template > \_shared-orion > \_cms > formats > shared > eyebrow nav
-   Orion Template > \_shared-orion > \_cms > formats > universal > canonical

-   Orion Template > \_shared-orion > \_cms > blocks > xml > bottom scripts <-- no, i don't think we actually need this

-   Orion Template > \_shared-orion > \_cms > blocks > landing-footer
-   Orion Template > \_shared-orion > \_cms > formats > shared > landing eyebrow nav

-   do we need a base file? can we make 1 dynamic url file instead? probably.
