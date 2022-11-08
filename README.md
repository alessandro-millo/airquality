# airquality
## HOW TO RETRIEVE THIS DATASET (https://www.luchtmeetnet.nl)
To download this dataset go to https://www.luchtmeetnet.nl/rapportages.
Select the following from the drop-drown menues:
 - component: PM10
 - report: mean_year_day
 - period: 2016 to 2021
 Click on request data, then click again on GGD.  
 Finally, press "download CSV".

## (PM10) PARTICULATE MATTER
 The concentration of PM10 in the air is measured in micrograms per cubic meter air (μg/m3).
 The daily concentration of PM10 is greatly influenced by the weather. In cities the concentrations are slightly higher during the day than at night, due to traffic. PM10 is a collective term for suspended particles that can be inhaled and have a maximum diameter of 0,01 millimetres. The yearly average limit value is 40 (μg/m3). The 24 hour limit value may not exceed 50 (μg/m3) more than 35 times per year.

## AIR QUALITY CLASSES FOR PM10 in μg/m3
Good 0 - 30
Fair 30 - 75
Poor 75 - 125
Very Poor  125 - 200
Extremely Poor >200

## TIME FORMAT
 All readings are hourly averages and are stored in winter time (UTC/GMT). An hourly value from hour X (date_from) to hour X+1 (date_to) is stored under hour X. On the website the value is shown in local time, so with summer/winter time correction at the hour X+1. This means that the values associated with a time relate to the situation prior to the specified hour (the concentration at 2:00 PM gives the hourly average concentration measured between 1:00 PM and 2:00 PM). Downloadable data is raw and states the date_from, this applies to both the csv files that can be downloaded via reporting and data that can be downloaded via the API. The API's datetime format conforms to ISO8601.

## TYPES OF MEASURING STATIONS
The measuring stations are located at different types of locations:

- Regional (Regionaal): in a rural area, not near major roads or nearby industry
- City background (Stedelijk): in urban areas, but not near busy roads or industry
- Traffic (Verkeerbelast): near a busy road
- Industry (Industrieel Belast): Close to major industrial companies
- Others (Overig): measuring stations that do not meet the above definitions.

## MEASURING STATIONS IN THIS DATASET ORDERED BY TYPE (IDENTIFICATION NUMBER + NAME)

**REGIONAL**
NL49556 De Rijp-Oostdijkje 
NL49565 Oude Meer-Aalsmeerderdijk 
NL49703 Spaarnwoude-Machineweg

**CITY BACKGROUND**
NL49014 Amsterdam-Vondelpark 
NL49016 Amsterdam-Westerpark 
NL49701 Zaandam-Wagenschotpad

**TRAFFIC**
NL49007 Amsterdam-Einsteinweg 
NL49012 Amsterdam-Van Diemenstraat 
NL49017 Amsterdam-Stadhouderskade 
NL49020 Amsterdam-Jan van Galenstraat

**INDUSTRIAL**
NL49546 Zaanstad-Hemkade 
NL49551 IJmuiden-Kanaalstraat 
NL49553 Wijk aan Zee-De Banjaert 
NL49557 Wijk aan Zee-Bosweg 
NL49572 Velsen-Staalstraat 
NL49573 Velsen-Reyndersweg 
NL49704 Zaanstad-Hoogtij

**OTHERS**
NL49561 Badhoevedorp-Sloterweg 
NL49564 Hoofddorp-Hoofdweg 
NL49570 Beverwijk-Creutzberglaan

## ADDITIONAL INFORMATION
Meetpunten van GGD Amsterdam						
* = *=  Minder dan 90% van de gekozen periode beschikbaar (uur/dag)						
Wijzigingen van eerder gerapporteerde data zie https://www.luchtmeetnet.nl/informatie/download-data/rapportage-correcties					

* = *= Less than 90% of the selected period available (hour/day)
Changes to previously reported data see https://www.luchtmeetnet.nl/informatie/download-data/rapportage-corrections
micrograms/m3

## PROCESS OF CLEANING THE DATA
From the file I removed the additional information on the measurements and I included it in this file.I replaced missing values marked with "-" with blanks instead. I added the column name "location" to the column containing the measuring stations. I added "year" in all other columns containing the measurements. I made a second file where I replaced the station identification numbers with their names, using underscores instead of spaces.

## About the files
senza_nomi.csv contains the data with the stations identification numbers.
con_nomi.csv contains the data with the replaced station names.
