# Deployment Process

This is a deployment process, not a step by step development process. Feel free to add to this as needed.

## Local Environment

-   If possible, avoid working on the same template, on the same day, at the same time as your colleague
-   Confirm that Integrations is up to date, then create a Feature Branch
-   Merge Feature Branch locally with Integrations and confirm no merge conflicts
-   When ready to move to Cascade DEV, `git push origin integrations` to AWS Code Commit

## Cascade DEV

-   Build or edit the Format
-   Build or edit the Shared Field and Data Definition
-   Add the new or edited module to a beta page on the DEV site
-   Add content, images and links as if building an actual page
-   When ready for Cascade PROD, create Pull Request on AWS Code Commit and confirm there are no merge conflicts
-   Send a link to the Pull Request, and a link to the DEV page to your colleague for review
-   If time allows, show the new module to the team during our team meeting
-   Not every new thing can wait for a show and tell, and not every new thing needs to be shown to the team before it moves to PROD

## Cascade PROD

-   Whether you merge the Pull Request first or last depends on what you're merging and what impact it has on existing modules
-   It's a best practice to disable publishing for all sites using the given template before moving work to PROD
    -   Manage Site > Destinations > Prod > Edit > Uncheck 'Enable Destination' > Submit
-   Move the new or edited work to PROD
-   Merge the Pull Request if you haven't already done so
-   Build a beta page on one of the PROD sites and confirm the new or edited module works as expected
-   Send a link to the page to your colleague to review the new work
-   Share a screenshot with a short description and a link the PROD beta page in the Digital Team chat
