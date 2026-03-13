# Add Gemini pages to another site:

> Often you are putting Gemini on a site that has pages in another template. See below for how to add gemini nav and footer to Capricorn and Orion pages

- Add a _shared-gemini folder. Copy from Gemini Template
- Set _shared-gemini to not be viewable/editable by users Edit > Access > None AND Access for Contents > Overwrite > None

## Setup Location and Steps

- Data Definition lives in _shared-gemini
- Template lives in _shared-gemini
- Add Config for Page type to the site (copy from Gemini Template) - Name Config Gemini Page
  -  Default: content-rows from site -- this will get the site and shared variables.
 	-  Footer: from site
  -  Header: from site
 	-  Open Graph: copy default version from shared-gemini if not a fully gemini site. Make sure you are pointing at a valid default image
 	-  Schema: from site
 	-  Top Body Scripts: from site
-  Copy Content Type: Page to site and name "Gemini Page". Point to site Gemini Page config. SET TO DO NOT PUBLISH (only during build)
-  Update base asset: Edit > Config, change to site content type.
-  Add Asset Factories for: Home, College Landing, Overview, Program, Topic
-  Update Global Variables for site: global format
-  Update top-body-script with the correct GTM
-  Update Schema to be correct.
-  Update footer (_shared-gemini > _blocks )
-  When the nav is ready. You will need to replace site-setup. There can only be on site-setup on a site.
-  Header file has common search terms, you need to get this from Ben or Jennifer and add this before launch.
-  Check favicons are pointing to the correct place.

## Launch Process

> This may involve a multiple day outage depending on level of cleanup.
- Put a notice up on Cascade to let users know publish is off.
- Disable Publish in Destinations
- Turn off Invalidation on site
- Move over Site Setup
- Link to correct footers.
- Remove noindex (in config)
- Remove no publish (in content type)
- Vicky will clear the server
- Publish
- Redirects in Place
- Turn lambda and invalidation back on.

## For Orion Pages

> For Orion template pages using Gemini Header/Footer.
- In template update code for gemini footer: move to point to new universal version (in _shared-orion) instead of regular univeral
- In config for Universal Page, update footer to gemini version in Blocks
- In config update header field to point to one in site shared_gemini
- Add Font css in head files to pick up Lora and Lato
