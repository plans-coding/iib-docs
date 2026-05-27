# Trip Syntax

## Trip Object

Each trip object has fields according to the following. The name of the key of each trip is the InnerId, which is a unique six characters long string randomly generated at creation.

> [!NOTE]
> Regarding validation: Some fields are checked for syntax and must comply to that.

|Field|Description|
|-|-|
|ArrangerGroup|Could e.g. be **Family**, **Private**, or **Work**.<br /><br />**Syntax:** `<string>`
|OuterId|The OuterID is exposed to end-user of the web app. Normally you can take the first letter of the TripDomain and the first letter of ParticipantGroup and add a chronological number.<br /><br />**Syntax:** `<letters and dashes and serial numbers of your choice>`
|OverallDestination|Type in you trip primary destination. E.g. **Finland**, or **Italia, Spain etc.**<br /><br />**Syntax:** `<string>`
|DepartureDate|Your departure date in ISO format.<br /><br />**Syntax:** `YYYY-MM-DD`
|ReturnDate|Your return date in ISO format.<br /><br />**Syntax:** `YYYY-MM-DD`
|TripLabels|Add keywords to the trip for filter purposes.<br /><br />**Syntax:** `LabelA, LabelB, LabelC, ...`
|MapPins|The main stops of your trip that you want to plot on the map.<br /><br />**Syntax (multi-line accepted):** `[ NAME_OF_MAP_PIN ]( LATITUDE, LONGITUDE )`
|TripDescription|A short description that explain the aim of the trip. E.g. **My fantastic summer trip to France**.<br /><br />**Syntax:** `<string>`
|PhotoStarttime|*For use with Immich.* If you leave your home at let say 8 pm and don't want to include photos from earlier on **departure day**, then you can set a time here. If left empty, all photos from departure day will be included.<br /><br />**Syntax:** `HH:MM`
|PhotoEndtime|*For use with Immich.* Same as above, but for **return day**.<br /><br />**Syntax:** `HH:MM`
|Days|An array containg each day and their related data. See below.|

## Trip Day Object
There is a second level array object in the trip object with fields according to following.

> [!NOTE]
> Regarding validation: Some fields are checked for syntax and must comply to that.

|Field|Description|
|-|-|
|Date|Your date in ISO format.<br /><br />**Syntax:** `YYYY-MM-DD`
|Events|This is your fully description of what you did this day.<br /><br />**Syntax (multi-line accepted):** `<string>`
|Accommodation|The name and the address of your accommodation.<br /><br />**Syntax:** `<string>`
|AccommodationCountry|The name of the country you stayed in during the night.<br /><br />**Syntax:** `<string>`
|AccommodationCoordinateAccuracy|Possibility to mark the accuracy of the coordinates.<br /><br />**Syntax:** `<string>`
|AccommodationCoordinates|The gps coordinates of your accommodation, e.g. **59.329444, 18.068611**.<br /><br />**Syntax:** `lat_decimal,lng_decimal`
|TravelParticipants|The name of your travel buddies, separated by comma. **N.B.** *This is not exposed in web app.*<br /><br />**Syntax:** `<string>`
|AdditionalNotes|**N.B.** *Additional notes are not exposed in web app.*<br /><br />**Syntax (multi-line accepted):** `<string>`
|CountriesDuringDay|This field is for enhanced statistics. Enter all countries in cronologial order during that day, separated by comma. The country names need to conform to the country names defined in `ContinentCountries`. In front of the country name prefix `*`, `**`, and `+` is allowed. Read more under [Special syntax used for Countries During Day (Events)](#special-syntax-used-for-countries-during-day-events).<br /><br />**Syntax (prefix allowed):** `<country name without space>, <country name without space>, <country name without space> [...]`

### Special syntax used for Countries During Day (Events)

|Prefix|Function
|-|-|
|*|Shorter visit of significant importance
|**|Very short visit of without significant importance
|+|Restore, counts only if * and ** count

> [!NOTE]
> Countries During Day: When a prefix is used in front of a country name in field **CountriesDuringDay** in table `bewb_Events` it affect the **Statistics** page.
