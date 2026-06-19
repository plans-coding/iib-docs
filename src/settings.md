# Settings

The following settings are applicable

|Attribute Group|Attribute|Value|Description|
|-|-|-|-|
|Base|HomeContinent|**Continent**|Use this to sort your home continent first.|
|Base|HomeCountry|**Country**|Use this to remove your own country from the trip unique countries field. Use same spelling as in your notes and in the value of `ContinentCountries`.|
|Base|LanguageFile|**Filename**|Filename to the translation file located in the **languages** folder, e.g. `swedish.json`.|
|Definition|ArrangerGroups|**List**|Name of the arranger groups you want to use.|
|Definition|ContinentCountries|**List**|Definitions of continents and countries as well as their language (and spelling).|
|Definition|TripDomainColors|**List**|Color definitions of your trip domains.|
|Base|Immich|**Disabled** or **Enabled**|Enable if you want filter links from all event dates to Immich.|
|Photos|ImmichApiKey|**Key**|API key generated in Immich, used to authenticate the photo requests.|
|Photos|ImmichCoverAlbumId|**GUID**|The GUID of the cover photo album in Immich.|
|Photos|ImmichUrl|**URL**|Online URL to the Immich installation (e.g. `https://immich.example.com/`).|
|Other|ExternalMapProvider|**URL**|Set your prefered map provider.|

> [!NOTE]
> There are some Extensions too, that you can read about [here](./extension.md).

### Arranger Group
A categorisation of the arrangers of different trips.

### Trip Domains
There are three pre-defined trip domains
* Domestic trip
* Trip abroad
* Attachment trip

An attachment trip is defined as a visit to a country where you have a deeper connection. For example, if you study abroad, you might want to document that time but distinguish it from the ordinary abroad or domestic category.

Set theme colors to your different `TripDomains`.

```
Domestic: #0b5394
Abroad: #1d655e
Attachment: #C60C30
```


### Continent Countries

If you want to change (make other country definitions or translate country names) the pre-defined country settings you can do it by changing in the country definitions. Only countries defined in the table `ContinentCountries`  can be used in your trip notes and only with the very exact spelling.

> [!TIP]
> Other language: If you have the countries in your Trip notes written in another languange than English, then you can change the app behaviour by translating the countries in `ContinentCountries` to your own language.

```Pre-defined countries
{
  "Africa": {
    "Algeria": "DZ",
    "Angola": "AO",
    "Benin": "BJ",
    "Botswana": "BW",
    "Burkina-Faso": "BF",
    "Burundi": "BI",
    "Cabo-Verde": "CV",
    "Cameroon": "CM",
    "Central-African-Republic": "CF",
    "Chad": "TD",
    "Comoros": "KM",
    "Democratic-Republic-of-the-Congo": "CD",
    "Djibouti": "DJ",
    "Egypt": "EG",
    "Equatorial-Guinea": "GQ",
    "Eritrea": "ER",
    "Eswatini": "SZ",
    "Ethiopia": "ET",
    "Gabon": "GA",
    "Gambia": "GM",
    "Ghana": "GH",
    "Guinea": "GN",
    "Guinea-Bissau": "GW",
    "Ivory-Coast": "CI",
    "Kenya": "KE",
    "Lesotho": "LS",
    "Liberia": "LR",
    "Libya": "LY",
    "Madagascar": "MG",
    "Malawi": "MW",
    "Mali": "ML",
    "Mauritania": "MR",
    "Mauritius": "MU",
    "Morocco": "MA",
    "Mozambique": "MZ",
    "Namibia": "NA",
    "Niger": "NE",
    "Nigeria": "NG",
    "Republic-of-the-Congo": "CG",
    "Rwanda": "RW",
    "Sao-Tome-and-Principe": "ST",
    "Senegal": "SN",
    "Seychelles": "SC",
    "Sierra-Leone": "SL",
    "Somalia": "SO",
    "South-Africa": "ZA",
    "South-Sudan": "SS",
    "Sudan": "SD",
    "Tanzania": "TZ",
    "Togo": "TG",
    "Tunisia": "TN",
    "Uganda": "UG",
    "Zambia": "ZM",
    "Zimbabwe": "ZW"
  },
  "Asia": {
    "Afghanistan": "AF",
    "Armenia": "AM",
    "Azerbaijan": "AZ",
    "Bahrain": "BH",
    "Bangladesh": "BD",
    "Bhutan": "BT",
    "Brunei": "BN",
    "Cambodia": "KH",
    "China": "CN",
    "Cyprus": "CY",
    "Cyprus-Northern-Cyprus": null,
    "Georgia": "GE",
    "India": "IN",
    "Indonesia": "ID",
    "Iran": "IR",
    "Iraq": "IQ",
    "Israel": "IL",
    "Japan": "JP",
    "Jordan": "JO",
    "Kazakhstan": "KZ",
    "Kuwait": "KW",
    "Kyrgyzstan": "KG",
    "Laos": "LA",
    "Lebanon": "LB",
    "Malaysia": "MY",
    "Maldives": "MV",
    "Mongolia": "MN",
    "Myanmar": "MM",
    "Nepal": "NP",
    "North-Korea": "KP",
    "Oman": "OM",
    "Pakistan": "PK",
    "Philippines": "PH",
    "Qatar": "QA",
    "Russia": "RU",
    "Saudi-Arabia": "SA",
    "Singapore": "SG",
    "South-Korea": "KR",
    "Sri-Lanka": "LK",
    "Syria": "SY",
    "Taiwan": "TW",
    "Tajikistan": "TJ",
    "Thailand": "TH",
    "Timor-Leste": "TL",
    "Turkey": "TR",
    "Turkmenistan": "TM",
    "United-Arab-Emirates": "AE",
    "Uzbekistan": "UZ",
    "Vietnam": "VN",
    "Yemen": "YE"
  },
  "Europe": {
    "Albania": "AL",
    "Andorra": "AD",
    "Austria": "AT",
    "Belarus": "BY",
    "Belgium": "BE",
    "Bosnia-and-Herzegovina": "BA",
    "Bulgaria": "BG",
    "Croatia": "HR",
    "Cyprus": "CY",
    "Cyprus-Northern-Cyprus": null,
    "Czech-Republic": "CZ",
    "Denmark": "DK",
    "Denmark-Faraoe-Islands": "FO",
    "Estonia": "EE",
    "Finland": "FI",
    "Finland-Åland": "AX",
    "France": "FR",
    "Georgia": "GE",
    "Germany": "DE",
    "Greece": "GR",
    "Hungary": "HU",
    "Iceland": "IS",
    "Ireland": "IE",
    "Italy": "IT",
    "Kosovo": "XK",
    "Latvia": "LV",
    "Liechtenstein": "LI",
    "Lithuania": "LT",
    "Luxembourg": "LU",
    "Malta": "MT",
    "Moldova": "MD",
    "Moldova-Transnistria": null,
    "Monaco": "MC",
    "Montenegro": "ME",
    "Netherlands": "NL",
    "North-Macedonia": "MK",
    "Norway": "NO",
    "Poland": "PL",
    "Portugal": "PT",
    "Romania": "RO",
    "Russia": "RU",
    "San-Marino": "SM",
    "Serbia": "RS",
    "Slovakia": "SK",
    "Slovenia": "SI",
    "Spain": "ES",
    "Sweden": "SE",
    "Switzerland": "CH",
    "Ukraine": "UA",
    "United-Kingdom": "GB",
    "United-Kingdom-Akrotiri-and-Dhekelia": "GB",
    "United-Kingdom-Gibraltar": "GI",
    "United-Kingdom-Jersey": "JE",
    "United-Kingdom-Northern-Ireland": "GB",
    "Vatican-City": "VA"
  },
  "North-America": {
    "Antigua-and-Barbuda": "AG",
    "Bahamas": "BS",
    "Barbados": "BB",
    "Belize": "BZ",
    "Canada": "CA",
    "Costa-Rica": "CR",
    "Cuba": "CU",
    "Denmark-Greenland": "GL",
    "Dominica": "DM",
    "Dominican-Republic": "DO",
    "El-Salvador": "SV",
    "Grenada": "GD",
    "Guatemala": "GT",
    "Haiti": "HT",
    "Honduras": "HN",
    "Jamaica": "JM",
    "Mexico": "MX",
    "Nicaragua": "NI",
    "Panama": "PA",
    "Saint-Kitts-and-Nevis": "KN",
    "Saint-Lucia": "LC",
    "Saint-Vincent-and-the-Grenadines": "VC",
    "Trinidad-and-Tobago": "TT",
    "USA": "US"
  },
  "Oceania": {
    "Australia": "AU",
    "Fiji": "FJ",
    "Kiribati": "KI",
    "Marshall-Islands": "MH",
    "Micronesia": "FM",
    "Nauru": "NR",
    "New-Zealand": "NZ",
    "Palau": "PW",
    "Papua-New-Guinea": "PG",
    "Samoa": "WS",
    "Solomon-Islands": "SB",
    "Tonga": "TO",
    "Tuvalu": "TV",
    "Vanuatu": "VU"
  },
  "South-America": {
    "Argentina": "AR",
    "Bolivia": "BO",
    "Brazil": "BR",
    "Chile": "CL",
    "Colombia": "CO",
    "Ecuador": "EC",
    "Guyana": "GY",
    "Paraguay": "PY",
    "Peru": "PE",
    "Suriname": "SR",
    "Uruguay": "UY",
    "Venezuela": "VE"
  }
}
```


