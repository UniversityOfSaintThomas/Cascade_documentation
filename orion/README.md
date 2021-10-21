# Orion

## READ THIS BEFORE YOU PROCEED

**The first thing to do before proceeding with anything is to make sure the **Publishing Destinations** have been disabled and removed.**

### Go to Manage Site > Destinations

-   Click each destination, then click **Edit**
-   Uncheck the box labeled **Enable destination**.
-   After each destination is **Disabled**, **Delete** each of the destinations

### Next go to Manage Site > Transports

-   **Delete** each of the transports

### Why it's important...

-   Copying a **live, production site** also copies it's publishing settings
-   Anything that's published or un-published will also take place on the live site
-   For example, if you start deleting content from the copy before removing the destinations, content from the live site will also be deleted

### If this happens...

-   Go to **System Menu > Sites**. Check the box next to the site you want to republish. Then click **Publish**
-   Republishing the site will re-deploy the pages that were deleted
-   Notify members of the web team and ITS immediately of what happened

**Avoid this mistake by confirming the destinations are removed from the new site copy before you proceed with anything.**

### Ask ITS to setup new publish destinations and transports

-   After you've made these changes, send a request to ITS (Vicky Vue)
-   ITS will also setup a new publish destinations and transports

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
