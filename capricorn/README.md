# Capricorn

This is the documentation specific to the **Capricorn** template. When you make a new Cascade instance using this template, do not proceed with anything until the following steps are completed.

**_The first steps are to make sure the Publishing Destinations and Transports have been disabled and removed._**

## :dart: Remove Destinations and Transports from a New Cascade Instance

### :point_right: Go to Manage Site > Destinations

-   Click each destination, then click **Edit**
-   Uncheck the box labeled **Enable destination**.
-   After each destination is **Disabled**, **Delete** each of the destinations

### :point_right: Next go to Manage Site > Transports

-   **Delete** each of the transports

---

### :exclamation: Why it's important...

-   Copying a **live, production site** also copies it's publishing settings
-   Anything that's published or un-published on the new copy will also be published or un-published on the live site
-   For example, if you start deleting content from the new copy before removing the destinations, content from the live site will also be deleted

### :exclamation: If this happens...

-   Go to **System Menu > Sites** and check the box next to the site you want to republish, then click **Publish**
-   Republishing the site will re-deploy the pages that were deleted
-   Notify members of the web team and ITS immediately of what happened

Avoid this mistake by confirming the **_Destinations and Transports are removed_** from the new site copy before you proceed with anything else.

## Site Settings

### Ask ITS to setup new publish destinations and transports

-   After you've made these changes, send a request to ITS (Vicky Vue)
-   ITS will go into the Cascade instance and add new publish destinations and transports

### Go to Manage Site > Site Settings

-   Change the URL
-   This field is required - use `example.com` if you don't know the new URL
-   Click Submit

## Continue with the Site Setup

-   [Capricorn Site Setup](https://github.com/UniversityOfSaintThomas/Cascade_documentation/tree/main/capricorn/site_setup.md)
