# Campaign Pages

This campaign page process documents the requirements and the steps to creating a landing page.

## :dart: Important to Remember

> Some requestors will try to make their own page, or at least offer to make their own page. Even when we trust them to do it, campaign pages should be a development task. After we confirm the requirements of the page, we can hand it back to the requestor to add and edit content and images.

## Requirements

Whether or not the requestor specifies a URL or program code, we always confirm those details with Kathy and Cassie on the Analytics team.

-   URL of the page
-   Salesforce Program/Major/Concentration
    -   ex. **AS_CS_MA|CATH**, Master of Arts in Catholic Studies

### Elements of a Campaign Page

-   Hero Image
-   RFI (Lightning Web Component)
    -   Thank you page
-   Content

---

### Example Orion Campaign Page

Fresh campaign page for the College of Arts and Sciences graduate study abroad program. We added the hero image, but the requestor will add content.

![Campaign page when first created](/images/page.png)

---

### Content &amp; Images

-   Requestors must provide their own images, or ask the Creative team for help with image sourcing.
-   Hero image dimensions should be approximately 1920px x 1080px, and the image size around 200kb.
-   Some requestors need help with content. If provided, we can add provided content, then requestors add or edit content as needed.

### :dart: Important to Remember

> It's not a development task to copyedit content, make multiple content revisions, or source images.

## Cascade

The campaign page templates in Capricorn and Orion are different, but the folder structure is the same.

### Folder Structure

```
name-of-campaign-page/
|__ thank-you/
    |__ index
|__ index
```

### Orion

-   Select the **Landing Page** template
-   Select the **Landing Page with RFI Form v2** module
    -   The modules available exist in the **Left Modules** content row
        -   Intro Block
        -   Gray Box
        -   Stat Box
        -   Left Image
        -   Accordion
        -   Intro Block Purple
        -   Test Tips (Law School only!)
-   Select **RFI Type v2 > Lightning Web Component**

---

|             Orion Landing Page              |     Orion Landing Page with RFI Form v2      |
| :-----------------------------------------: | :------------------------------------------: |
| ![Orion Landing](/images/orion-landing.png) | ![Orion Edit Screen](/images/orion-edit.png) |

---

### Capricorn

## Salesforce RFIs

## :dart: Important to Remember

> Unless there's a special request for additional fields, most campaign pages use these fields.

---

### Graduate

| Graduate campaign page RFI                 |                                                |
| :----------------------------------------- | :--------------------------------------------- |
| First name                                 | required                                       |
| Last Name                                  | required                                       |
| Email                                      | required                                       |
| Phone                                      | required when consent is checked               |
| I would like to receive text messages      |                                                |
| ![RFI phone not required](/images/rfi.png) | ![RFI phone required](/images/rfi-checked.png) |

---

### Undergraduate

| Undergraduate campaign page RFI               |          |
| :-------------------------------------------- | :------- |
| I will Apply to St. Thomas as a               | required |
| First name                                    | required |
| Last Name                                     | required |
| Email                                         | required |
| High School Attended                          | required |
| I can't find my High School                   |          |
| High School Graduation (YYYY)                 | required |
| ![RFI phone not required](/images/ug-rfi.png) |          |

---

### Lightning Web Components

First and Last name are automatically added to the RFI/Lightning Web Component, and are required fields.
