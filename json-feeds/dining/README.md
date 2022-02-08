# Dining Feed

Documentation for the dining feed data definition, related shared fields, and formats.

## JSON Format

**Note**: Asterisk `*` indicates a property required in the data definition.

### Dining Feed Format

The overall format of what the JSON feed provides

```javascript
DiningLocation[]
```

### Dining Location Format

A dining location indicates a location on campus where a person can dine at.

```javascript
{
  "name": String*                 // The name of the dining facility
  "locationType": String          // The type of the dining facility
  "description": String           // An overview of the dining facility
  "payment": String[]             // Payment types accepted at the facility
  "typesOfFood": String[]         // Types of food available at the dining facility
  "monday": String                // Open to close hour range (e.g. 7:00am - 8:30pm)
  "tuesday": String               // Open to close hour range (e.g. 7:00am - 8:30pm)
  "wednesday": String             // Open to close hour range (e.g. 7:00am - 8:30pm)
  "thursday": String              // Open to close hour range (e.g. 7:00am - 8:30pm)
  "friday": String                // Open to close hour range (e.g. 7:00am - 8:30pm)
  "saturday": String              // Open to close hour range (e.g. 7:00am - 8:30pm)
  "sunday": String                // Open to close hour range (e.g. 7:00am - 8:30pm)
  "link": String                  // A relative link to the dining facility's page in Cascade
  "image": String                 // An absolute URL for an image representative of the dining facility
  "stations": DiningStation[]     // Dining stations available at a dining facility
  "exceptions": DiningException[] // Exception notices for a dining facility
}
```

### Dining Station Format

A dining station represents a station within a dining location where a person can obtain food. (e.g. World Eats, Greens)

```javascript
{
  "name": String*       // The name of the dining station
  "description": String // An overview of what the dining station provides
  "meals": DiningMeal[] // A list of meals available at a dining station
}
```

### Dining Meal Format

A dining meal represents a meal at a dining location, generally associated with a certain time of day. (e.g. Breakfast, Lunch).

**Note**: Overall hours for a dining facility should take precident over hours for a given station's meal

```javascript
{
  "name": String*         // The name of a given meal
  "mondayFriday": String  // Beginning to end hour range (e.g. 7:00am - 8:30pm) 
  "saturday": String      // Beginning to end hour range (e.g. 7:00am - 8:30pm) 
  "sunday": String        // Beginning to end hour range (e.g. 7:00am - 8:30pm) 
}
```

### Dining Exception Format

A dining exception represents a duration where a given dining location may have different hours from what is shown.

```javascript
{
  "message": String // A description of what the exception is for and/or affects
  "start": Date*    // A datetime for the beginning of the exception
  "end": Date*      // A datetime for the end of the exception
}
```
