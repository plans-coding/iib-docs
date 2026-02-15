# Settings

## Path to database

Change the relative path to the database file in `server_db_path.txt` if you want your own database to load automatically when self-hosting.

## Database file

The settings is configured the database file table `bewx_Settings`. The following fields are applicable

|Attribute Group|Attribute|Value|Description|
|-|-|-|-|
|Base|HomeCountry|**Country**|Use this to remove your own country from the trip unique countries field. Use same spelling as in your notes and in the value of `ContinentCountries`.|
|Base|LanguageFile|**Filename**|Filename to the translation file located in the **personal** folder, e.g. `swedish.json`.|
|Definition|ContinentCountries|**List**|Definitions of continents and countries as well as their language (and spelling).|
|Definition|TripDomainColors|**List**|Color definitions of your trip domains.|
|Base|Immich|**Disabled** or **Enabled**|Enable if you want filter links from all event dates to Immich.|
|Photos|ImmichApiKey|**Key**||
|Photos|ImmichCoverAlbumId|**GUID**|The GUID of the cover photo album in Immich.|
|Feature|ImmichUrl|**URL**|Online URL to the Immich installation (e.g. `https://immich.example.com/`).|
|Other|Dataset|**Disabled** or **Enabled**|If enabled, the link to Dataset is shown.|
|Other|ExternalMapProvider|**URL**|Set your prefered map provider.|

### Trip Domains
There are three pre-defined trip domains
* Domestic trip
* Trip abroad
* Attachment trip

An attachment trip is defined as a visit to a country where you have a deeper connection. For example, if you study abroad, you might want to document that time but distinguish it from the ordinary abroad or domestic category.

Set theme colors to your different `TripDomains`.

```
Domestic:#0b5394
Abroad:#1d655e
Attatchment:#C60C30
```

### Participant Groups

Add the names of your different travel groups.<br /><br />**Syntax:** `<string without space>`


### Continent Countries

If you want to change (make other country definitions or translate country names) the pre-defined country settings you can do it by changing in the country definitions. Only countries defined in the table `ContinentCountries`  can be used in your trip notes and only with the very exact spelling.

> [!TIP]
> Other language: If you have the countries in `bewb_Events` (**CountriesDuringDay**)  written in another languange than English, then you can change the app behaviour by translating the countries in `ContinentCountries` to your own language.

```Pre-defined countries
Europe:Albania
Europe:Andorra
Europe:Austria
Europe:Belarus
Europe:Belgium
Europe:Bosnia and Herzegovina
Europe:Bulgaria
Europe:Croatia
Europe:Cyprus
Europe:Czech Republic
Europe:Denmark
Europe:Estonia
Europe:Finland
Europe:Finland-Åland
Europe:France
Europe:Georgia
Europe:Germany
Europe:Greece
Europe:Hungary
Europe:Iceland
Europe:Ireland
Europe:Italy
Europe:Kosovo
Europe:Latvia
Europe:Liechtenstein
Europe:Lithuania
Europe:Luxembourg
Europe:Malta
Europe:Moldova
Europe:Moldova-Transnistria
Europe:Monaco
Europe:Montenegro
Europe:Netherlands
Europe:North Macedonia
Europe:Norway
Europe:Poland
Europe:Portugal
Europe:Romania
Europe:Russia
Europe:San Marino
Europe:Serbia
Europe:Slovakia
Europe:Slovenia
Europe:Spain
Europe:Sweden
Europe:Switzerland
Europe:Ukraine
Europe:United Kingdom
Europe:United Kingdom-Akrotiri and Dhekelia
Europe:United Kingdom-Gibraltar
Europe:United Kingdom-Jersey
Europe:Vatican City
Asia:Afghanistan
Asia:Armenia
Asia:Azerbaijan
Asia:Bahrain
Asia:Bangladesh
Asia:Bhutan
Asia:Brunei
Asia:Cambodia
Asia:China
Asia:Cyprus
Asia:Georgia
Asia:India
Asia:Indonesia
Asia:Iran
Asia:Iraq
Asia:Israel
Asia:Japan
Asia:Jordan
Asia:Kazakhstan
Asia:Kuwait
Asia:Kyrgyzstan
Asia:Laos
Asia:Lebanon
Asia:Malaysia
Asia:Maldives
Asia:Mongolia
Asia:Myanmar
Asia:Nepal
Asia:North Korea
Asia:Oman
Asia:Pakistan
Asia:Philippines
Asia:Qatar
Asia:Russia
Asia:Saudi Arabia
Asia:Singapore
Asia:South Korea
Asia:Sri Lanka
Asia:Syria
Asia:Taiwan
Asia:Tajikistan
Asia:Thailand
Asia:Timor-Leste
Asia:Turkey
Asia:Turkmenistan
Asia:United Arab Emirates
Asia:Uzbekistan
Asia:Vietnam
Asia:Yemen
North America:Antigua and Barbuda
North America:Bahamas
North America:Barbados
North America:Belize
North America:Canada
North America:Costa Rica
North America:Cuba
North America:Dominica
North America:Dominican Republic
North America:El Salvador
North America:Grenada
North America:Guatemala
North America:Haiti
North America:Honduras
North America:Jamaica
North America:Mexico
North America:Nicaragua
North America:Panama
North America:Saint Kitts and Nevis
North America:Saint Lucia
North America:Saint Vincent and the Grenadines
North America:Trinidad and Tobago
North America:United States
South America:Argentina
South America:Bolivia
South America:Brazil
South America:Chile
South America:Colombia
South America:Ecuador
South America:Guyana
South America:Paraguay
South America:Peru
South America:Suriname
South America:Uruguay
South America:Venezuela
Africa:Algeria
Africa:Angola
Africa:Benin
Africa:Botswana
Africa:Burkina Faso
Africa:Burundi
Africa:Cabo Verde
Africa:Cameroon
Africa:Central African Republic
Africa:Chad
Africa:Comoros
Africa:Democratic Republic of the Congo
Africa:Djibouti
Africa:Egypt
Africa:Equatorial Guinea
Africa:Eritrea
Africa:Eswatini
Africa:Ethiopia
Africa:Gabon
Africa:Gambia
Africa:Ghana
Africa:Guinea
Africa:Guinea-Bissau
Africa:Ivory Coast
Africa:Kenya
Africa:Lesotho
Africa:Liberia
Africa:Libya
Africa:Madagascar
Africa:Malawi
Africa:Mali
Africa:Mauritania
Africa:Mauritius
Africa:Morocco
Africa:Mozambique
Africa:Namibia
Africa:Niger
Africa:Nigeria
Africa:Republic of the Congo
Africa:Rwanda
Africa:Sao Tome and Principe
Africa:Senegal
Africa:Seychelles
Africa:Sierra Leone
Africa:Somalia
Africa:South Africa
Africa:South Sudan
Africa:Sudan
Africa:Tanzania
Africa:Togo
Africa:Tunisia
Africa:Uganda
Africa:Zambia
Africa:Zimbabwe
Oceania:Australia
Oceania:Fiji
Oceania:Kiribati
Oceania:Marshall Islands
Oceania:Micronesia
Oceania:Nauru
Oceania:New Zealand
Oceania:Palau
Oceania:Papua New Guinea
Oceania:Samoa
Oceania:Solomon Islands
Oceania:Tonga
Oceania:Tuvalu
Oceania:Vanuatu
```


