# Capricorn &amp; Orion Vue Components

## Capricorn

| Vue Name                      | URL                                                                                   | Notes                                                                           |
| ----------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Admissions Visit              | https://www.stthomas.edu/admissions/undergraduate/campus-visits/schedule/index.html   | Summit Events/Salesforce API                                                    |
| Campus Visit                  | can't find the page, but is a Cascade json module to filter campus visits             | Cascade json data                                                               |
| Career Development            | https://www.stthomas.edu/career-development/resources/index.html                      | Cascade json data                                                               |
| Catalog Filter                | https://www.stthomas.edu/catalog/curricula/index.html                                 | Cascade json data                                                               |
| Catalog                       | https://www.stthomas.edu/catalog/curricula/classics/index.html                        | Cascade json data                                                               |
| Center Well-Being             | https://www.stthomas.edu/center-for-well-being/services/index.html                    | Cascade json data                                                               |
| Course Listing                |                                                                                       | Table that appears as last accordion on faculty profiles; ClassFinder API       |
| Dean's List                   | https://www.stthomas.edu/academics/deans-list/index.html                              | https://webapi.aws.stthomas.edu/deanslist/getDeansListByTerm                    |
| DFC Interviews                | https://dfc.stthomas.edu/interviews/index.html                                        | Summit Events/Salesforce API                                                    |
| Dining Filter                 | https://www.stthomas.edu/dining/locations-menus-hours/index.html                      | Cascade json data                                                               |
| Disclosure Container & Button |                                                                                       | Not used with an API; the accordion functionality for faculty profiles          |
| Donation/Double the Donation  | https://give.stthomas.edu/about/matching-gifts/index.html                             |                                                                                 |
| Estimate Your Bill            | https://www.stthomas.edu/financial-aid/undergraduate/estimate-your-bill/index.html    |                                                                                 |
| Events                        | https://dfc.stthomas.edu/about/news-events/index.html                                 | DONE - Summit Events/Salesforce API                                             |
| Faculty Directory             |                                                                                       | Esploro/Research Online API, ask Chad Kluck to add new endpoints to the AWS App |
| Faculty Profile               |                                                                                       | Esploro/Research Online API, Banner API, Cascade json data                      |
| General Counsel               | https://www.stthomas.edu/policies/index.html                                          | Cascade json data                                                               |
| Group Visits                  | https://www.stthomas.edu/admissions/undergraduate/campus-visits/group/index.html      | Summit Events/Salesforce API                                                    |
| Library Directory             | library.stthomas.edu                                                                  |                                                                                 |
| Library Hours                 | library.stthomas.edu                                                                  |                                                                                 |
| Library Knowledgbase          | library.stthomas.edu                                                                  |                                                                                 |
| Library Room Reservation      | library.stthomas.edu                                                                  |                                                                                 |
| Library Search                | library.stthomas.edu                                                                  |                                                                                 |
| Lightning Web Component       |                                                                                       | DONE - Salesforce script                                                        |
| Locate Counselor              | https://www.stthomas.edu/admissions/undergraduate/contact/locate-counselor/index.html | Lightning Web Component/Salesforce script                                       |
| Online Learning               | online.stthomas.edu                                                                   | ClassFinder API                                                                 |
| Posters                       | posters.stthomas.edu                                                                  | Cascade json data                                                               |
| Scholarships                  | https://www.stthomas.edu/financial-aid/undergraduate/scholarships/                    | Cascade json data                                                               |
| Social Sharing                | social icons that share data about the page via respective social links               | Could really just be vanilla javascript                                         |
| Student Affairs               | https://www.stthomas.edu/current-students-families/resources/index.html               | Cascade json data                                                               |
| Study Abroad                  | https://www.stthomas.edu/academics/study-abroad/programs/index.html                   | Does not use an API                                                             |
| Video Player                  | https://www.stthomas.edu/about/sustainability/index.html                              | Uses the YouTube iframe API                                                     |
| Video Gallery                 |                                                                                       | Uses the YouTube iframe API                                                     |
| Vimeo                         |                                                                                       | Not sure if we use this anywhere                                                |
| Global Header                 |                                                                                       | Used for the header                                                             |
| Program Filter                | https://www.stthomas.edu/academics/undergraduate/index.html                           | ClassFinder API                                                                 |

### Services JS

-   admissions-eda.js (Salesforce EDA API)
-   classes.js (ClassFinder https://classes.aws.stthomas.edu/index.htm?year=2025&term=20&schoolCode=XX&levelCode=ALL)
-   courses.js (ClassFinder)
-   deans-list.js (https://webapi.aws.stthomas.edu/deanslist/getDeansListByTerm)
-   degrees-certificates.js (Classfinder)
-   directories.js (Banner https://directory.aws.stthomas.edu/)
-   events.js (Summit Events/Salesforce EDA)
-   give.js (https://givedesignations.aws.stthomas.edu)
-   library.js

## Orion

| Vue Name                | URL                                                                                                   | Notes                                                                                           |
| ----------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| CAS Event Filter        | https://cas.stthomas.edu/news-events/calendar/index.html                                              | Summit Events salesforce/Thad API                                                               |
| Class Feed              | https://health.stthomas.edu/graduate-psychology/courses/index.html                                    | Class Finder (James) API                                                                        |
| Course Detail           | Blue box in the Exec Ed program pages with course dates, times and costs                              | Flatbridge/Execuctive Education (cbecrm) API                                                    |
| Course Listing          | https://business.stthomas.edu/faculty-research/faculty-bios/berry-katie/index.html                    | Bottom of accordion on faculty bios Class Finder (James) API                                    |
| Course Listing Exec Ed  | I'm not aware of this module used anywhere                                                            | Flatbridge/Executive Education API                                                              |
| Directory ExecEd        | Appears to be a faculty directory for Exec Ed, and seems like it's not fully built                    | Does not have an API associated with it.                                                        |
| Donation                | I'm not sure where on the Give site this is being used. Script for Double the Donation                | No API, just loadsd scripts to embed a donation form.                                           |
| Event Detail            | I think this is old. The last person to work on this was Chase, 6 years ago                           | Summit Events (salesforce) API                                                                  |
| Event Finder            | https://business.stthomas.edu/opus-advantage/events/index.html                                        | Opus Events Filter/Summit Events (salesforce) API                                               |
| Event Finder Law        | https://law.stthomas.edu/about/news-events/events-calendar/index.html                                 | Law School Events Filter/Summit Events (salesforce)                                             |
| Event Listing Module    | https://business.stthomas.edu/                                                                        | Many pages on Orion have this module.                                                           |
| Faculty Directory       |                                                                                                       | Esploro/Research Online API, ask Chad Kluck to add new endpoints to the AWS App                 |
| Faculty Profile         |                                                                                                       | Esploro/Research Online API, Banner API, Cascade json data                                      |
| Favorites               | https://business.stthomas.edu/executive-education/program-finder/index.html                           | Some of this has been removed from Orion sites, but some favorites still exist on Exec Ed pages |
| Filter                  | Appears to be a generic filter, but Angela has never worked on it and is not aware of it being in use | No APIs                                                                                         |
| Give/iDonate            | not sure where on the Give site this is being used                                                    | Uses this API: https://givedesignations.aws.stthomas.edu                                        |
| Health Event Filter     | I can't find this on MFCOH, so I don't think it's actually being used                                 | Summit Events if used                                                                           |
| Lawyer Search           | https://law.stthomas.edu/lawyer-search/index.html                                                     | Salesforce EDA                                                                                  |
| Library Search          | Do not know where this module is being used                                                           | Supposed to be a text/search input                                                              |
| Lightning Web Component |                                                                                                       | DONE                                                                                            |
| Program Filter          | https://business.stthomas.edu/executive-education/program-finder/index.html                           | Flatbridge/Execuctive Education (cbecrm) API                                                    |
| Social Sharing          | https://engineering.stthomas.edu/degree-stories/electric-vehicle-market-trends/index.html             | No API, dynamic links to share on social media                                                  |
| Video Gallery           |                                                                                                       | Gemini has a video module componenet made from vanilla javascript.                              |
| Vimeo                   |                                                                                                       | I think don't we have a Vimeo exclusive module in Orion.                                        |

### Services JS

-   admissions.js (Salesforce EDA API)
-   cape.js (OLD/Deprecated was a Salesforce API)
-   cbecrm.js (Flatbridge)
-   classes.js (ClassFinder https://classes.aws.stthomas.edu/index.htm?year=2025&term=20&schoolCode=XX&levelCode=ALL)
-   directories.js (Banner https://directory.aws.stthomas.edu/)
-   events.js (Summit Events/Salesforce EDA)
-   give.js (https://givedesignations.aws.stthomas.edu)
-   lawsearch.js (Salesforce EDA)
