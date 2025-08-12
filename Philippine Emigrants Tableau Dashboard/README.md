# Philippine Emigrants Tableau Dashboard

# Table of Contents
* [Project Background](#project-background)
* [Data Structure and Initial Checks](#data-structure-and-initial-checks)
* [Executive Summary](#executive-summary)
* [Insights Deep Dive](#insights-deep-dive)
* [Recommendations](#recommendations)
* [Assumptions and Caveats](#assumptions-and-caveats)
* [Credits and Acknowledgements](#credits-and-acknowledgements)

---

# Project Background
The Philippines has one of the highest emigration rates in the world, and is among the highest in Southeast Asia ([see this repo for more details](https://github.com/Francis-Calingo/Socioeconomic-Analysis-of-The-Philippines)). In Canada, emigrants leaving the Philippines are one of the top sources of immigration ([see this repo for more details](https://github.com/Francis-Calingo/Visualizing-Migration-in-Canada?tab=readme-ov-file#time-series-analysis)), and is rapidly growing in certain regions ([see this repo for more details](https://github.com/Francis-Calingo/ELECTIONS-CANADA-RESEARCH-PROJECT-Filipino-Canadian-Demographic-Report)). Using data from the Commission of Overseas Filipinos' Registered Emigrants datasets, this Tableau dashboard visualizes emigration from the Philippines in the following areas:

- **Time-Series Progression of Migration**
- **International Destinations** 
- **Place of Origin** 

The interactive Tableau dashboard used to report and explore this topic can be found [here](https://public.tableau.com/app/profile/francis.emmanuel.calingo/viz/DataonRegisteredFilipinoEmigrantsSincethe1980s/NumberofRegisteredFilipinoEmigrantsSince1981).

To download the Tableau workbook version, [click here](https://github.com/Francis-Calingo/Tableau-Public-Policy-Dashboards/raw/refs/heads/main/Philippine%20Emigrants%20Tableau%20Dashboard/Filipino%20Emigration%20Trends%20(1981%E2%80%93Present).twbx)

<i>Preview of Dashboard:</i>

<img src=./Figures/Dashboard.png>

**Tools and Technologies Used:**

* **Visualization Platform:** Tableau Public

* **Data Wrangling:** Excel (cleaning, reshaping)

* **Interactivity Features:** Hover tooltips, Navigation buttons


Data Sources: [CFO Statistics](http://www.cfo.gov.ph/Statistics)


[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Data Structure and Initial Checks

The data structure for the data utilized to build this dashboard is as follows:

| Data Content  | Number of Entries (Records x Field) | Number of Records  | Number of Fields | Download File Link |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Emigrant Data-All Country Destinations | **465**  | 155  | 3  | [Download](https://raw.githubusercontent.com/Francis-Calingo/Philippine-Emigrants-Tableau-Dashboard/refs/heads/main/CSV%20Files/Emigrant-1981-2022-AllCountries.csv?token=GHSAT0AAAAAADD7C7WSOTOUG4AAYPRBRGRY2CHEISA)  |
| Emigrant Data-Major Country Destinations  | **559**  | 43   | 13  | [Download](https://raw.githubusercontent.com/Francis-Calingo/Philippine-Emigrants-Tableau-Dashboard/refs/heads/main/CSV%20Files/Emigrant-1981-2022-AllCountries.csv?token=GHSAT0AAAAAADD7C7WSOTOUG4AAYPRBRGRY2CHEISA) |
| Emigrant Data-Major Country Destinations (Total)  | **22**  | 11  | 2 | [Download](https://raw.githubusercontent.com/Francis-Calingo/Philippine-Emigrants-Tableau-Dashboard/refs/heads/main/CSV%20Files/Emigrant-1981-2022-MajorCountry.csv?token=GHSAT0AAAAAADD7C7WS7XU5MQG2LO54JF6I2CHEJZQ) |
| Emigrant Data-Provincial Origins | **405**  | 81  | 5  | [Download](https://raw.githubusercontent.com/Francis-Calingo/Philippine-Emigrants-Tableau-Dashboard/refs/heads/main/CSV%20Files/Emigrant-1981-2022-PlaceofOrigin%20Province.csv?token=GHSAT0AAAAAADD7C7WS5BNHX2QSPNYT6QOA2CHEKBQ) |
| **TOTAL** | **1,451**  | 290  | 23  | N/A  |

**Calculations and Data Viz Development:**
* **Panel 1:** Number of Registered Filipino Emigrants Since 1981
  * Type: Bar and Line Dual-Axis Plot
  * Data: Emigrant-1981-2022-MajorCountry
  * Column: Year
  * Row (2): SUM(Total), SUM(Total)-Running sum

* **Panel 2:** Registered Filipino Emigrants by Destination Country, 1981-2022
  * Type: Vertical Bar Chart
  * Data: Emigrant-1981-2022-MajorCountry Total
  * Column: Country
  * Row: SUM(Total)
 
* **Panel 3:** Percentage of Registered Filipino Emigrants by Country of Destination, 1981-2022
  * Type: Choropleth Map
  * Data: Emigrant-1981-2022-AllCountries
  * Measure: SUM(% Total Emigrants)
  * Dimension: Country
  * Column: Longitude(generated)
  * Row: Latitude(generated)
 
* **Panel 4:** Total Registered Filipino Emigrants by Origin, 1988-2023 (per 100,000, 2020 PH Census)
  * Type: Choropleth Map
  * Data: Emigrant-1981-2022-PlaceofOrigin Province
  * Measure: SUM(Emigrants per Capita)
  * Dimensions: Country, Province
  * Column: Longitude(generated)
  * Row: Latitude(generated)

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Executive Summary

### Overview of Findings

The main takeaways from this dashboard were: (1) Other than the early 2020s (COVID-19 pandemic) and select years (e.g., late 1990s during economic hardships in Asia), trends show that the number of people emigrating from the Philippines annually have been consistently on the rise; (2) The vast majority of emigrants choose North America as their destination; (3) On a per-capita basis, provinces in the Ilocos Region (i.e., northwest corner of the northernmost island group, Luzon) produced the most emigrants since the 1980s.

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Insights Deep Dive
### Time-Series Progression of Migration:

* **In general, the number of registered emigrants leaving the Philippines annually since the 1980s has been on the rise.** The continuation of policies such as the Labour Export Policy, as well as the increased reliance on foreign-trained professionals in certain countries such as Canada's demand for nurses, has no doubt contributed to these increases.
   
* **There were some instances of a year-to-year drop in emigrants leaving the Philippines, such as in the early 2020s (COVID-19 pandemic) and late 1990s (1990s Asian financial crisis).** Whether it is due to destination countries enacting stricter immigration policies in order to deal with an ongoing crisis, domestic policies aimed at preventing people from leaving, or a lower capacity or desire for people to emigrate, emigration has proven to be tied to current events and reactions to them.
  
* **Over 1 million people emigrated from the Philippines from 1980-1999 (19 years) and another 1 million left from 1999-2013 (14 years).** With people emigrating at a faster rate over time, the Filipino community may soon overtake other diaspora communities in size. 

<img src=./Figures/Panel%201.JPG>

### International Destinations:
  
* **The vast majority of emigrants choose to immigrate to North America.** Over 1.5 million people since 1981 have chosen to settle in the United States, while over half a million have chosen to settle in Canada.
  
* **Japan and Australia are the primary recipients of Filipino emigrants in the Aisa-Pacific region.** Nearly 160,000 Filipinos have emigrated to Japan since 1981, while over 150,000 have chosen to settle in Australia.
  
* **While relatively small compared to the emigrant data for the aforementioned countries, 42,587 Filipinos have emigrated to Italy since 1981, the most out of any European country.** This is more than double the next European country, United Kingdom, where 20,582 Filipinos have immigrated to since 1981.

<img src=./Figures/Panel%202.JPG>

<img src=./Figures/Panel%203.JPG>


### Place of Origin (Per-Capita):

* **The Ilocos Region leads the Philippines in terms of the number of Filipinos who emigrated from the Philippines since 1988 (per 100,000-population based on 2020 Philippine Census).** Ilocos North leads the country with 11,032 emigrants per 100,000.
  
* **Other provinces or regions in Luzon have high per-capita emigration rates.** In fact, Zambales (6,929 emigrants per 100,000) and the National Capital Region (5,183 emigrants per 100,000) have higher emigration rates that 2 of the 4 provinces from Ilocos Region (Pangasian-3,465 per 100,000, La Union-4,025 per 100,000), while Zambales had a higher rate than Ilocos Sur (5,260 per 100,000).
  
* **From a per-capita measurement, very few emigrants can be found from the the other two major island groups-Visayas and Mindanao.** Only Cebu has a rate exceeding 2,000 emigrants per 100,000 (2,045), while the rest of the provinces from those two island groups are below 2,000 (Sulu had the lowest rate with 5 per 100,000, whil nearby Tawi-Tawi had a near-identical 9).
  
<img src=./Figures/Panel%204.JPG>

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Recommendations:

Based on the insights and findings above, we would recommend the Philippine government to consider the following: 

* With the exception of certain periods (e.g., COVID-19 pandemic, 1997 Asian Financial Crisis), the number of people leaving the Philippines annually have been steadily rising, with more people leaving the country between 1999-2013 than between 1980-1999. **This steady increase should raise concerns about the country's potential brain drain, increasing dependency on remittances, and the prominence of emigration-related services in the bureaucracy and national economy. Therefore, structural adjustments need to be made from a public policy and economic standpoint to avoid developing an emigration-oriented economy.**
  
* The vast majority of registered emigrants (over 2 million) have settled in North America since 1981. **This warrants increasing consular services and support in both Canada and the United States, especially given both country's vastness geographically.**

* Outside of North America, Australia and Japan were the top destinations for Filipino emigrants in the Asia-Pacific region, while Italy was the top European country. **English being an official language of the Philippines makes it easier to support emigrants in Australia but more difficult for emigrants in Italy and Japan, and therefore, the government must ameliorate its efforts in helping overseas Filipino communities in both countries break the language barriers (e.g., better programs by the Philippine embassies in Rome and Tokyo, and more comprehensive Italian and Japanese translations to help emigrants integrate).**
  
* On a per-capita basis, the provinces in the northwestern part of Luzon, which are mostly connected by the Manila North Road highway, had the highest number of registered emigrants by province of origin, while the province of Cebu (which is home to Mactan–Cebu International Airport, the second-most busiest international airport in the country) had the highest amongst all provinces in the Visayas and Mindanao island groups. **This suggests that provinces with a more stronger transportation infrastucture that is well-connected to the National Capital Region or the Mactan–Cebu International Airport have a higher per-capita emigration rate. This could be more so due to an increased capability of leaving the country rather than push factors from those provinces, and, therefore, warrants further investigations into socioeconomic push factors of emigrants leaving those particular provinces versus from other provinces.**
    
[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:
  
* It is important to note that this data is based on the Commission of Overseas Filipinos' Registered Emigrants database (who defines emigrants as those who leave the Philippines to settle permanently in a destination country). The dashboard therefore does not account for Filipinos who leave the country through other means-e.g., as overseas foreign workers, as international students, as those who later gain permanent residency status in another country after several years, those who permanently settle in another country after temporarily settling in one or more intermediate countries.
  
* Tableau recognizes 84 first-level administrative divisions of the Philippines as "states/provinces" (81 provinces, National Capital Region, City of Isabela, and Cotabato City). As a result, in order to render the choropleth map usable, adjustments had to be made to the names from the [original xlxs file from CFO](https://cms-cdn.e.gov.ph/CFO/pdf/8.%20Emigrant-1988-2022-PlaceOfOrigin.xlsx), all while converting the relevant data into a csv file. In particular, Compostela Valley (which appears on CFO's database) was renamed to "Davao de Oro" in 2019 (which appears on Tableau's list of 84 recognized first-level administrative divisions.

* In a similar vein, the names of the countries Tableau recognizes and the names of the countries from CFO's datasets do not align in a few cases (e.g.,Cambodia is referred to as "Democratic Kampuchea" in CFO's database), therefore, adjustments had to be made to the names in order to match, while converting the relevant data from the [original xlxs file from the CFO](https://cms-cdn.e.gov.ph/CFO/pdf/7.%20Emigrant-1981-2022-AllCountries.xlsx) into a csv file.
  
[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Credits and Acknowledgements

"Region Support for Philippines Maps". Salesforce, https://help.salesforce.com/s/articleView?language=en_US&id=001453778&type=1.

Tableau Desktop and Web Authoring Help. https://help.tableau.com/current/public/desktop/en-us/default.htm.

"The Best of Schumann." YouTube, created by Mark Keith, https://www.youtube.com/watch?v=Iqj0ZyoeEXw.

[<b>Back to Table of Contents</b>](#table-of-contents)
