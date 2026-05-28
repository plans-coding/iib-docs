# Trip Syntax

## Trip Object

Each trip object has fields according to the following. The key of each trip object is the InnerId — a six-character hexadecimal string (characters `0`–`9` and `a`–`f`) generated randomly when the trip is created. You do not set it manually.

> [!NOTE]
> Date, time and coordinate fields below should follow the stated format so they display correctly and feed the statistics. The editor auto-formats most of these, but the format is not strictly enforced — malformed values may simply be ignored (e.g. a pin with an unparseable coordinate is not plotted).

|Field|Description|
|-|-|
|TripDomain|The category of the trip. Allowed values are the keys defined in `TripDomainColors` (see [Settings](settings.html#trip-domains)); by default **Domestic**, **Abroad**, or **Attachment**.<br /><br />**Syntax:** `<one of the defined trip domains>`
|ArrangerGroup|Who arranged the trip, e.g. **Family**, **Private**, or **Work**. Allowed values are the entries in `ArrangerGroups` (see [Settings](settings.html)).<br /><br />**Syntax:** `<one of the defined arranger groups>`
|OuterId|The OuterId is the trip identifier exposed to the end-user of the web app. In the editor it is auto-filled as the first letter of `TripDomain` plus the first letter of `ArrangerGroup` (uppercased), followed by a dash and a sequential number per prefix — e.g. a **Domestic** **Family** trip becomes `DF-1`, the next `DF-2`. You can override it with any value.<br /><br />**Syntax:** `XX-N` (auto), or a custom string.
|OverallDestination|Type in you trip primary destination. E.g. **Finland**, or **Italia, Spain etc.**<br /><br />**Syntax:** `<string>`
|DepartureDate|Your departure date in ISO format.<br /><br />**Syntax:** `YYYY-MM-DD`
|ReturnDate|Your return date in ISO format.<br /><br />**Syntax:** `YYYY-MM-DD`
|TripLabels|Add keywords to the trip for filter purposes.<br /><br />**Syntax:** `LabelA, LabelB, LabelC, ...`
|MapPins|The main stops of your trip that you want to plot on the map. One pin per line.<br /><br />**Syntax (multi-line accepted):** `[ NAME_OF_MAP_PIN ]( latitude, longitude )` — decimal degrees, comma-separated.
|StartNode|Where the trip started. **N.B.** *Not exposed in the web app* — for your own records.<br /><br />**Syntax:** `<string>`
|EndNode|Where the trip ended. **N.B.** *Not exposed in the web app* — for your own records.<br /><br />**Syntax:** `<string>`
|TripDescription|A short description that explain the aim of the trip. E.g. **My fantastic summer trip to France**.<br /><br />**Syntax:** `<string>`
|PhotoStarttime|*For use with Immich.* If you leave your home at let say 8 pm and don't want to include photos from earlier on **departure day**, then you can set a time here. If left empty, all photos from departure day will be included.<br /><br />**Syntax:** `HH:MM`
|PhotoEndtime|*For use with Immich.* Same as above, but for **return day**.<br /><br />**Syntax:** `HH:MM`
|PhotoAlbums|*For use with Immich.* Names of Immich albums to link from the trip. Each `[ Album Name ]` becomes a button that opens the matching album in Immich. You can also add `!desc[ text ]` to create a button that searches Immich for photos with that description.<br /><br />**Syntax (multi-line accepted):** `[ Album Name ] !desc[ description ]`
|CoverPhoto|The cover image of the trip, shown in **Cards view** and in the report. Provide a direct image URL.<br /><br />**Syntax:** `<image URL>`
|DocumentationNote|Free-text note for the whole trip. **N.B.** *Not exposed in the web app* — for your own records.<br /><br />**Syntax (multi-line accepted):** `<string>`
|Days|An array containg each day and their related data. See below.|

## Trip Day Object
There is a second level array object (`Days`) in the trip object with fields according to following.

> [!NOTE]
> Date and coordinate fields below should follow the stated format so they display and map correctly. The format is not strictly enforced — malformed values are simply ignored where they can't be parsed.

|Field|Description|
|-|-|
|Date|Your date in ISO format.<br /><br />**Syntax:** `YYYY-MM-DD`
|Events|This is your fully description of what you did this day.<br /><br />**Syntax (multi-line accepted):** `<string>`
|Accommodation|The name and the address of your accommodation.<br /><br />**Syntax:** `<string>`
|AccommodationCountry|The name of the country you stayed in during the night.<br /><br />**Syntax:** `<string>`
|AccommodationCoordinates|The GPS coordinates of your accommodation in decimal degrees, e.g. **59.329444, 18.068611**. The space after the comma is optional.<br /><br />**Syntax:** `latitude, longitude`
|AccommodationCoordinatesAccuracy|Free-text note on the accuracy of the coordinates, shown next to the accommodation, e.g. **exact** or **approximate**. Optional.<br /><br />**Syntax:** `<string>`
|TravelParticipants|The name of your travel buddies, separated by comma. **N.B.** *This is not exposed in web app.*<br /><br />**Syntax:** `<string>`
|AdditionalNotes|**N.B.** *Additional notes are not exposed in web app.*<br /><br />**Syntax (multi-line accepted):** `<string>`
|CountriesDuringDay|This field is for enhanced statistics. Enter all countries in chronological order during that day, separated by comma. The country names need to conform to the country names defined in `ContinentCountries`. In front of a country name the prefixes `*`, `**`, and `+` are allowed. Read more under [Special syntax used for Countries During Day (Events)](#special-syntax-used-for-countries-during-day-events).<br /><br />**Syntax (prefix allowed):** `<country name without space>, <country name without space>, <country name without space> [...]`

### Special syntax used for Countries During Day (Events)

|Prefix|Function
|-|-|
|`*`|Shorter visit, but of significant importance
|`**`|Very short visit, without significant importance
|`+`|Re-entry / pass-through of a country. Like `**`, it is **not** added to your count of unique visited countries.

> [!NOTE]
> Countries During Day: Using a prefix in front of a country name in the **CountriesDuringDay** field of a day affects how that country is counted on the **Statistics** page.
