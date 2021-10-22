# Site Setup

This is the **Site Setup** documentation for the **Capricorn** template. When you make a new Cascade site, follow each of these steps to configure the new instance correctly.

The global configuration files for the Capricorn template are in the root of the University of St. Thomas site.

```
University of St. Thomas: /_shared-capricorn/
```

Each site, or instance, that uses the Capricorn template also has a shared configuration in **its own root** for things that are specific to that instance. The following setup are the steps to use the global styles and make sure things like the header, footer and navigation, etc. are unique.

Note that `New Instance: ` is an example name that refers to the new site being created, the same way `University of St. Thomas: ` refers to the instance for `www.stthomas.edu`. A best practice is to name the site for the school, college, department or app being built.

---

## Content Types

### Go to Manage Site > Content Types

#### There are 5 Content Types

-   Events
-   Home
-   Interior
-   Landing
-   Sub-Landing

### Click on a Content Type > then Edit

-   Under Type of Content > Select the Data Definition radio button
-   Change the Data Definition for **Home** to
    -   `New Instance: Data Definitions/Home`
-   Change the Data Definition for **Events, Interior, Landing, and Sub-Landing** to
    -   `University of St. Thomas: Data Definitions/Universal`
-   Click Submit after each change

By pointing the **Content Types Data Definition** to the University of St. Thomas universal data definition, all sites using capricorn receive updates when a module is updated. So all sites using capricorn get the benefit of any updates that are made.

Each site has its own **Home Data Definition** because a homepage is always unique.

## Site Setup

The **`site-setup`** file is in the root of the new site. This determines the structure of the main navigation.

### Go to Site Content > site-setup

-   Click on Edit > Properties
-   Change the Data Definition to `University of St. Thomas: Data Definitions/Site Setup`
-   Click Submit

## Configurations

### Go to Manage Site > Configurations

-   Change each Configuration Template (Events, Interior, Landing, and Sub-Landing)
-   Click Interior > Edit > and change the Template to
    -   `University of St. Thomas: /_shared-capricorn/templates/Universal`

**Before you click submit, scroll down and notice that each "Region" is now pointing to "University of St. Thomas"**

-   Change the following **region paths** to the current site's path `New Instance: ...`

    -   Canonical
    -   Footer
    -   Head Data
    -   Header
    -   ID
    -   Metadata
    -   Schema

-   Make sure the **Default** path is `<> content-rows`

#### Home Configuration

**Each Home Configuration path points to the new site except Bottom Scripts. This should point to the University of St. Thomas**

-   Click Home > Edit > and change the Template to `New Instance: /_shared-capricorn/templates/Home`
-   Make sure the Home **Default** path is `<> home`
-   Click Submit

## Asset Factories

### Go to Manage Site > Asset Factories

### There are 4 Asset Factory items for Capricorn

-   Event
-   Interior Page
-   Landing Page
-   Program Filter
-   Sub-Landing Page

### Click each Asset Factory and change the Base Asset from the old instance to the new instance

**From this**

```
Capricorn Template: /_shared-capricorn/base-assets/interior
```

**To this**

```
New Instance: /_shared-capricorn/base-assets/interior
```

## Base Assets

### Go to Site Content > `New Instance: _shared-capricorn > Base Assets`

-   Click `_shared-capricorn > base-assets` to enter the directory
-   Next click More in the upper right-hand corner and choose Bulk Change from the drop down
-   Property to Change > Content Type
-   Check the box for `STTHOMAS DEV: /_shared-capricorn/base-assets/interior`
-   New Content Type > Content Types > Interior

## Continue with Formats and Blocks

-   [Update Capricorn Formats and Blocks](https://github.com/UniversityOfSaintThomas/Cascade_documentation/blob/main/capricorn/02_update_formats_blocks.md#updating-formats-and-blocks)
