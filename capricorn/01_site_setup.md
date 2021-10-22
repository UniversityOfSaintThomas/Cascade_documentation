# Site Setup

This is the **Site Setup** documentation for the **Capricorn** template. When you make a new Cascade site, follow each of these steps to configure the new instance correctly.

The global configuration files for the Capricorn template are in the root of the University of St. Thomas site.

```
University of St. Thomas: /_shared-capricorn/
```

Each site, or instance, that uses the Capricorn template also has a shared configuration in **its own root** for things that are specific to that instance. The following setup are the steps to use the global styles and make sure things like the header, footer and navigation, etc. are unique.

You'll see `New Instance: ...` below as an example name that refers to the new site being created, the same way `University of St. Thomas: ...` refers to the Cascade instance or site for `www.stthomas.edu`. A best practice is to name the site for the school, college, department or app being created.

## Examples of how to name an instance:

-   Morrison Family College of Health **[college]**
-   Lawyer Search **[app for the School of Law]**
-   Continuing and Professional Education **[department and an app]**

---

## Content Types

### Go to Manage Site > Content Types

#### There are 5 Content Types

-   Events
-   Home
-   Interior
-   Landing
-   Sub-Landing

The home page is unique to this site or instance. There is a separate **Data Definition** called **Home** for each instance to build a unique homepage. The styles (CSS) for the homepage are global. The layout and markup still match the University of St. Thomas instance. As of this writing (10/21/2021) we have not been asked to build a new homepage for any site using the Capricorn template.

A change to the homepage would likely consist of a layout change, or adding a static module to the homepage template. You can change the styles for a single unique homepage by adding semantic classes and styling that homepage as needed.

### Click on a Content Type > then Edit

-   Under Type of Content > Select the Data Definition radio button
-   Next change the Data Definition for Home to `New Instance: Data Definitions/Home`
-   Then change the Data Definition for Interior, Landing, and Sub-Landing to `University of St. Thomas: Data Definitions/Universal`
-   Click Submit after each change

By pointing the **Content Types Data Definition** to the University of St. Thomas universal data definition, all sites using capricorn receive updates when a module style or layout is improved. So all sites using capricorn get the benefit of any updates that are made.

#### Something to consider...

We may be asked to update the styles for a module on capricorn for a specific reason, in one situation, on one site. Knowing that update will appear on all sites using capricorn, there should be consensus on the web team around the implications of this update. Most of the time it's not a big deal. Just keep it in mind.

## Site Setup

The **`site-setup`** file is in the root of the new site. This determines the structure of the main navigation.

### Go to Site Content > site-setup

-   Click on Edit > Properties
-   Change the Data Definition to `University of St. Thomas: Data Definitions/Site Setup`
-   Click Submit

## Configurations

### Go to Manage Site > Configurations

-   Change each Configurations' Template (Events, Interior, Landing, and Sub-Landing)
-   Click Interior > Edit > and change the Template to `University of St. Thomas: /_shared-capricorn/templates/Universal`

**Before you click submit, scroll down and notice that each "Region" is now pointing to "University of St. Thomas"**

-   Change the following **region** paths back to the current site's path `New Instance: ...`
    -   Canonical
    -   Footer
    -   Head Data
    -   Header
    -   ID
    -   Metadata
    -   Schema

**You're overriding the Canonical, Footer, Head Data, Header and Meta Data files to reference the current site, not the University of St. Thomas.**

-   Change (or override) individual parts of the template as needed to customize the current site.

**The Home Configuration paths all point to the new site or instance except Bottom Scripts. This should point to the University of St. Thomas**

-   Click Home > Edit > and change the Template to `New Instance: /_shared-capricorn/templates/Home`
-   Make sure you don't change Default paths.
    -   For Home the Default is `<> home`
    -   For all other Configurations the Default is `<> content-rows`
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

## Updating Formats and Blocks
