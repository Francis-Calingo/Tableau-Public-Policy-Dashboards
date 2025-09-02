# Measles on the Rise Globally: A Comprehensive Tableau Dashboard

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

The rise of the prevalence of measles globally within the past several years alone has been a very concerning phenomenon, despite the fact that it had technically not been classified as a Public Health Emergency of International Concern by the World Health Organization. While it is difficult to pinpoint the exact root causes of the rise in measles prevalence, I nevertheless built a Tableau dashboard visualizing the recent history of the epidemiology of measles and vaccination efforts. The surface-level insights from the interactive dashboard should not be treated as a substitute for meaningful comprehensive analysis, but should serve as a gateway for further investigations. In other words, the dashboard helps users understand the geography and timeline of measles and vaccination efforts, but does not answer *why*. That will have to be explored when we consider cultural, historical, geopolitical, and socioeconomic factors contributing to a country's measles infection and vaccination rates (e.g., colonial history contributing to vaccine hesitancy, global vaccine inequalities, conflicts, etc.). 

The dashboard will explore both confirmed measles cases and vaccination across the globe using the following metrics:

- **Total**
- **Per-Capita** 
- **Growth Rate** 

The interactive Tableau dashboard used to report and explore this topic can be found [here]().

To download the Tableau workbook version, [click here]()

<i>Preview of Dashboard:</i>

<img src=>

**Tools and Technologies Used:**

* **Visualization Platform:** Tableau Public

* **Data Wrangling:** Excel (cleaning, reshaping)

* **Interactivity Features:** 


Data Sources: []()

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Data Structure and Initial Checks

All datasets were sourced from the World Health Organization:
* [Measles - number of reported cases](https://www.who.int/data/gho/data/indicators/indicator-details/GHO/measles---number-of-reported-cases)

* [Measles-containing-vaccine first-dose (MCV1) immunization coverage among 1-year-olds (%)](https://www.who.int/data/gho/data/indicators/indicator-details/GHO/measles-containing-vaccine-first-dose-(mcv1)-immunization-coverage-among-1-year-olds-(-))

* [Measles-containing-vaccine second-dose (MCV2) immunization coverage by the locally recommended age (%)](https://www.who.int/data/gho/data/indicators/indicator-details/GHO/measles-containing-vaccine-second-dose-(mcv2)-immunization-coverage-by-the-nationally-recommended-age-(-))

The data structure for the data utilized to build this dashboard is as follows:

| Data Content  | Number of Entries (Records x Field) | Number of Records  | Number of Fields | Download File Link |
| ------------- | ------------- | ------------- | ------------- | ------------- |
|  | ****  |   |   | [Download](https://raw.githubusercontent.com/Francis-Calingo/Philippine-Emigrants-Tableau-Dashboard/refs/heads/main/CSV%20Files/Emigrant-1981-2022-AllCountries.csv?token=GHSAT0AAAAAADD7C7WSOTOUG4AAYPRBRGRY2CHEISA)  |
|   | ****  |    |   | [Download](https://raw.githubusercontent.com/Francis-Calingo/Philippine-Emigrants-Tableau-Dashboard/refs/heads/main/CSV%20Files/Emigrant-1981-2022-AllCountries.csv?token=GHSAT0AAAAAADD7C7WSOTOUG4AAYPRBRGRY2CHEISA) |
|   | ****  |   |  | [Download]() |
|  | ****  |   |   | [Download]() |
| **TOTAL** | ****  |   |   | N/A  |

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

 | WHO Name  | Matching Tableau Name | Reason for Discrepancy |
| ------------- | ------------- | ------------- |
|  | ****  |   |  
|   | ****  |    | 
|   | ****  |   |
|  | ****  |   | 
|  | ****  |   |  
|  | ****  |   |  
|  | ****  |   |  
|  | ****  |   |  
|  | ****  |   |  
|  | ****  |   |  
|  | ****  |   |  
|  | ****  |   |  

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Executive Summary

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Insights Deep Dive

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Recommendations

Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following: 

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Assumptions and Caveats

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

[<b>Back to Table of Contents</b>](#table-of-contents)

---

# Credits and Acknowledgements

https://community.tableau.com/s/question/0D54T00000C65j3SAB/list-of-world-countries-accessible-with-tableau-public

https://www.youtube.com/watch?v=MmKC86fn1Tg

"The ONLY Data Analytics Portfolio Project You Need - Walkthrough". Uploaded by Lore So What, 2022-12-01. YouTube, https://www.youtube.com/watch?v=g6cjhUhrhY8

[<b>Back to Table of Contents</b>](#table-of-contents)
