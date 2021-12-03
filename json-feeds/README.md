# JSON Feed (Dining, Faculty Directory)

## Content Type

### Faculty-Staff Profile

#### Settings

-   Configuration
    -   Faculty-Staff Profile
-   Metadata Set
    -   Page
-   Data Definition
    `_shared-orion: Data Definitions/Faculty-Staff Profile`

### Json Feed

#### Settings

-   Configuration
    -   Json
    -   `University of St. Thomas: Configurations/Json`
-   Metadata Set
    -   `University of St. Thomas: Metadata Set/Default`
-   Data Definition
    -   `University of St. Thomas: Data Definition/Json Feed`

#### Publish Options

-   NONE

## Configuration

### Json

-   Name
    -   Json
-   Type of Data
    -   JSON
-   File Extension
    -   .json
-   Template
    -   Json Feed
-   Publishable
    -   Checked
-   Path
    -   `University of St. Thomas: /_shared-capricorn/formats/modules/feed/feed type`

## Publish Sets

### Faculty Json

-   Faculty/Staff Directory page
-   Do not publish on a schedule, just create the publish set

## Data Definitions

### Feed Type

-   Identifier: Feed Type
-   Label: Feed Type
-   Select
    -   Label: Dining
    -   Value: dining

## Asset Factories

### STUFF GOES HERE ABOUT ASSET FACTORIES

## Templates

### Json Feed

```xml
<!--#cascade-skip-->
<pass-through>
	<system-region name="JSON-DATA"/>
</pass-through>
```

## Formats

### <> feed type

-   Create additional templates and add them to the feed type

```java
#import("_shared-capricorn/formats/modules/feed/dining feed")

#set ($feed = $currentPage.getStructuredDataNode("feed"))
#set ($feedType = $feed.getChild("Feed Type").textValue)

#if ($feedType == "dining")
    #diningFeed($currentPage)
#end
```

```java
#import("_shared-orion/_cms/formats/feed/faculty bio")

#set ($feed = $currentPage.getStructuredDataNode("feed"))
#set ($feedType = $feed.getChild("Feed Type").textValue)

#if ($feedType == "Faculty Bio")
    #facultyBio($currentPage)
## #elseif ($type == "Observatory")
##     ## #simpleXmlFeed($row)
#end
```
