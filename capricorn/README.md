# Capricorn :school_satchel:

-   After you've made these changes, send a Web Help Desk Ticket to ITS (Vicky Vue) and ask for a new domain.
-   ITS will also setup a new transfer/publish protocol.
-   AFTER this has been setup, you can delete the content you don't need from your new site.
-   If you start deleting content from your new site before this is setup, you will delete content, from the originating site, from the server.
-   If you make this mistake (like I did), go to all Sites and republish the entire originating site.
-   Republish individual directories as needed.

## Go to Manage Site > Site Settings

-   Change the URL
-   Even if you enter example.com, make sure you change the URL
-   Click Submit

## Go Back to Manage Site > Destinations

-   Delete the destination

## Go Back to Manage Site > Transports

-   Delete the transport

## Go Back to Manage Site > Asset Factories

## There are 4 Asset Factory items for Capricorn

-   Interior Page
-   Landing Page
-   Program Filter
-   Sub-Landing Page

## There are 7 Asset Factory items for Orion

-   Academic Calendar
-   Course Detail
-   Degrees and Programs
-   Faculty-Staff Profile
-   Landing Page
-   Story Page
-   Universal Page

## Click on an Asset Factory and change the Base Asset from the old instance to the new instance

### Do this for each of the Asset Factory items

-   Capricorn example

```
University of St. Thomas: /_shared-capricorn/base-assets/interior -> STTHOMAS DEV: /_shared-capricorn/base-assets/interior
```

-   Orion example

```
_shared/_cms/base assets/academic-calendar -> Orion Template/_shared-orion/_cms/base assets/academic-calendar
```

### Go to Site Content and do this for each Base Asset

-   Click to enter the `_shared-capricorn > base-assets` folder
-   Next click More in the upper right-hand corner and choose Bulk Change from the drop down
-   Property to Chnage > Content Type
-   Check the box for `STTHOMAS DEV: /_shared-capricorn/base-assets/interior`
-   New Content Type > Content Types > Interior

### Go Back to Manage Site > Content Types

#### There are 5 Content Types

-   Home
-   Interior
-   Landing
-   Program-Filter
-   Sub-Landing

## Click on a Content Type > then Edit

-   Type of Content > Select Data Definition
-   Change the Data Definition for Home to "University of St. Thomas: Data Definitions/Home"
-   Change the Data Definition for Interior, Landing, Program Filter and Sub-Landing to "University of St. Thomas: Data Definitions/Universal"
-   Click Submit after each change

## Next go to Site Content > then site-setup

## Click on Edit > Properties

-   Change the Data Definition to "University of St. Thomas: Data Definitions/Site Setup"
-   Click Submit

## Next go to Manage Site > then Configurations

-   Change each Configurations' Template (Home, Interior, Landing, Program Filter and Sub-Landing)
-   Click Home > then Edit > then change the Template to "University of St. Thomas: /\_shared-capricorn/Templates/Universal"
-   Before you click submit, scroll down and notice that each "Region" is now pointing to "University of St. Thomas"
-   Change the "Canonical", "Footer", "Head Data", "Header" and "Metadata" paths back to the current site's path
-   You're overriding the Canonical, Footer, Head Data, Header and Meta Data files to referrence the current site, not the .EDU. Now you can edit those files as needed.
-   Change (or override) individual parts of the template as needed to customize the current site.
-   Make sure you don't change Default paths.
    -- For Home the Default is "<> home"
    -- For all other Configurations the Default is "<> content-rows"
-   Click Submit

## Next go to Site Content

-   Go to \_shared-capricorn > formats > universal > canonical
-   Update the URL to the new site's URL
