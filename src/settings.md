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


### Continent Countries

If you want to change (make other country definitions or translate country names) the pre-defined country settings you can do it by changing in the country definitions. Only countries defined in the table `ContinentCountries`  can be used in your trip notes and only with the very exact spelling.

> [!TIP]
> Other language: If you have the countries in `bewb_Events` (**CountriesDuringDay**)  written in another languange than English, then you can change the app behaviour by translating the countries in `ContinentCountries` to your own language.

```Pre-defined countries
Europe:Albania:AL
Europe:Andorra:AD
Europe:Belgium:BE
Europe:Bosnia-and-Herzegovina:BA
Europe:Bulgaria:BG
Europe:Cyprus:CY
Europe:Cyprus-Northern-Cyprus
Europe:Denmark:DK
Europe:Denmark-Faraoe-Islands:FO
Europe:Estonia:EE
Europe:Finland:FI
Europe:Finland-Åland:AX
Europe:France:FR
Europe:Georgia:GE
Europe:Greece:GR
Europe:Ireland:IE
Europe:Iceland:IS
Europe:Italy:IT
Europe:Kosovo:XK
Europe:Croatia:HR
Europe:Latvia:LV
Europe:Liechtenstein:LI
Europe:Lithuania:LT
Europe:Luxembourg:LU
Europe:Malta:MT
Europe:Moldova:MD
Europe:Moldova-Transnistria
Europe:Monaco:MC
Europe:Montenegro:ME
Europe:Netherlands:NL
Europe:North-Macedonia:MK
Europe:Norway:NO
Europe:Poland:PL
Europe:Portugal:PT
Europe:Romania:RO
Europe:Russia:RU
Europe:San-Marino:SM
Europe:Switzerland:CH
Europe:Serbia:RS
Europe:Slovakia:SK
Europe:Slovenia:SI
Europe:Spain:ES
Europe:United-Kingdom:GB
Europe:United-Kingdom-Akrotiri-and-Dhekelia:GB
Europe:United-Kingdom-Gibraltar:GI
Europe:United-Kingdom-Jersey:JE
Europe:United-Kingdom-Northern-Ireland:GB
Europe:Sweden:SE
Europe:Czech-Republic:CZ
Europe:Germany:DE
Europe:Ukraine:UA
Europe:Hungary:HU
Europe:Vatican:VA
Europe:Belarus:BY
Europe:Austria:AT
Africa:Algeria:DZ
Africa:Angola:AO
Africa:Benin:BJ
Africa:Botswana:BW
Africa:Burkina-Faso:BF
Africa:Burundi:BI
Africa:Cabo-Verde:CV
Africa:Central-African-Republic:CF
Africa:Democratic-Republic-of-the-Congo:CD
Africa:Djibouti:DJ
Africa:Egypt:EG
Africa:Equatorial-Guinea:GQ
Africa:Ivory-Coast:CI
Africa:Eritrea:ER
Africa:Eswatini:SZ
Africa:Ethiopia:ET
Africa:Gabon:GA
Africa:Gambia:GM
Africa:Ghana:GH
Africa:Guinea:GN
Africa:Guinea-Bissau:GW
Africa:Cameroon:CM
Africa:Kenya:KE
Africa:Comoros:KM
Africa:Lesotho:LS
Africa:Liberia:LR
Africa:Libya:LY
Africa:Madagascar:MG
Africa:Malawi:MW
Africa:Mali:ML
Africa:Morocco:MA
Africa:Mauritania:MR
Africa:Mauritius:MU
Africa:Mozambique:MZ
Africa:Namibia:NA
Africa:Niger:NE
Africa:Nigeria:NG
Africa:Republic-of-the-Congo:CG
Africa:Rwanda:RW
Africa:Senegal:SN
Africa:Seychelles:SC
Africa:Sierra-Leone:SL
Africa:Somalia:SO
Africa:Sudan:SD
Africa:South-Africa:ZA
Africa:South-Sudan:SS
Africa:Sao-Tome-and-Principe:ST
Africa:Tanzania:TZ
Africa:Chad:TD
Africa:Togo:TG
Africa:Tunisia:TN
Africa:Uganda:UG
Africa:Zambia:ZM
Africa:Zimbabwe:ZW
Asia:Afghanistan:AF
Asia:Armenia:AM
Asia:Azerbaijan:AZ
Asia:Bahrain:BH
Asia:Bangladesh:BD
Asia:Bhutan:BT
Asia:Brunei:BN
Asia:Cyprus:CY
Asia:Cyprus-Northern-Cyprus
Asia:Philippines:PH
Asia:United-Arab-Emirates:AE
Asia:Georgia:GE
Asia:India:IN
Asia:Indonesia:ID
Asia:Iraq:IQ
Asia:Iran:IR
Asia:Israel:IL
Asia:Japan:JP
Asia:Yemen:YE
Asia:Jordan:JO
Asia:Cambodia:KH
Asia:Kazakhstan:KZ
Asia:China:CN
Asia:Kyrgyzstan:KG
Asia:Kuwait:KW
Asia:Laos:LA
Asia:Lebanon:LB
Asia:Malaysia:MY
Asia:Maldives:MV
Asia:Mongolia:MN
Asia:Myanmar:MM
Asia:Nepal:NP
Asia:North-Korea:KP
Asia:Oman:OM
Asia:Pakistan:PK
Asia:Qatar:QA
Asia:Russia:RU
Asia:Saudi-Arabia:SA
Asia:Singapore:SG
Asia:Sri-Lanka:LK
Asia:South-Korea:KR
Asia:Syria:SY
Asia:Tajikistan:TJ
Asia:Taiwan:TW
Asia:Thailand:TH
Asia:Timor-Leste:TL
Asia:Turkey:TR
Asia:Turkmenistan:TM
Asia:Uzbekistan:UZ
Asia:Vietnam:VN
North-America:Antigua-and-Barbuda:AG
North-America:Bahamas:BS
North-America:Barbados:BB
North-America:Belize:BZ
North-America:Costa-Rica:CR
North-America:Denmark-Greenland:GL
North-America:Dominica:DM
North-America:Dominican-Republic:DO
North-America:El-Salvador:SV
North-America:Grenada:GD
North-America:Guatemala:GT
North-America:Haiti:HT
North-America:Honduras:HN
North-America:Jamaica:JM
North-America:Canada:CA
North-America:Cuba:CU
North-America:Mexico:MX
North-America:Nicaragua:NI
North-America:Panama:PA
North-America:Saint-Kitts-and-Nevis:KN
North-America:Saint-Lucia:LC
North-America:Saint-Vincent-and-the-Grenadines:VC
North-America:Trinidad-and-Tobago:TT
North-America:USA:US
Oceania:Australia:AU
Oceania:Fiji:FJ
Oceania:Kiribati:KI
Oceania:Marshall-Islands:MH
Oceania:Micronesia:FM
Oceania:Nauru:NR
Oceania:New-Zealand:NZ
Oceania:Palau:PW
Oceania:Papua-New-Guinea:PG
Oceania:Solomon-Islands:SB
Oceania:Samoa:WS
Oceania:Tonga:TO
Oceania:Tuvalu:TV
Oceania:Vanuatu:VU
South-America:Argentina:AR
South-America:Bolivia:BO
South-America:Brazil:BR
South-America:Chile:CL
South-America:Colombia:CO
South-America:Ecuador:EC
South-America:Guyana:GY
South-America:Paraguay:PY
South-America:Peru:PE
South-America:Suriname:SR
South-America:Uruguay:UY
South-America:Venezuela:VE
```


