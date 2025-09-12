# Feeds in Gemini

## RSS feeds
In gemini rss feeds go in _external-links/rss

To add:
1. Navigate to the rss folder
2. Click Add Content
3. Select Default > Block
4. Select Block Type is Feed
5. Name and give url.
6. Confirm the rss feed is generating and submit.
   
## JSON feeds
These are feeds where we are generating json based on page data (usually cards). A directory or filter module then uses that json data.

### Parts of a Feed
- Card Component format - added to Page data definition in "Full-Width Row" only, doesn't have a component format
- JSON feed format - will live in /format/feeds and rely on Cascade Query API
- Feed Type Data Defintion - feed is added to Feed data defition
- Feed Type format - update format with the new feed from data defition name
- Directory/Filter format - will live in formats/compontents and generate module based on json data added to filter modules in "Full-Width Row" only
- Update utilities - so you don't get an import error. Must update macro processRows so you don't get an error.

### Add a Feed Page
There is a specific page type that you must add to generate a JSON file. Take the following steps:
1. Navigate to the folder to add the JSON, it is usually in the same folder as the index page where you will be generating the feed compnonent.
2. Click Add Content
3. Select Default > Page
4. Change site dropdown to _shared-gemini
5. Select Feed and Choose
6. Page Name will be the type of feed like "faculty" or "funds" not "index"
7. Select feed type from drop down and submit.

### Current Feeds
#### Search for a Fund
- Located in Alumni under /funds.
- Json format: causefeed
- Card: Search for a Fund Card in Shared Fields/feeds
- Directory: Search for a Fund Directory
  
## Faculty/Staff Profile Feeds
