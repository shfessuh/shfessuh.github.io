# Abstract
Chicago’s public transportation network is often perceived as a hotspot for criminal activities, raising concerns about safety and accessibility. This project investigates spatial patterns of crime within Chicago's transit network, focusing on data from the Chicago Transit Authority (CTA) stations in 2011. Using Local Indicators of Spatial Association (LISA) and Kernel Density Estimation (KDE), the analysis reveals clustering patterns of different crimes and identifies crime hotspots. Through this project, I developed skills in spatial data analysis, hypothesis testing, and using geospatial tools to study crime distribution.

## Dataset
The dataset was sourced from the Chicago Police Department’s Law Enforcement Analysis and Reporting System and accessed through the Chicago Data Portal. It was supplemented with a publicly available shapefile dataset found online to incorporate spatial data for community areas.
* **Crime Data:** 5,808 observations from 2011, including crime types, descriptions, coordinates, and community areas.
    - Link: https://data.cityofchicago.org/Public-Safety/CTA-Crime/5xiy-qnsz/about_data
* **Shapefile Data:** Includes Chicago’s community area boundaries, population data from 2010, and polygon coordinates for spatial analysis.
    - Link: https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Census-Tracts-2010/5jrd-6zik

## Spatial Crime Analysis

### *LISA Statistics*
- Applied LISA statistics with Local Moran’s I to identify spatial autocorrelation and crime clusters across 73 Chicago community areas.
- Normalized crime data to reflect crime rates per 10,000 people for accurate comparisons.
West Garfield Park, Loop, Near South

### *Kernel Density Estimation (KDE)*
- Used KDE to visualize spatial patterns of specific crime types and assess their clustering across longitude and latitude.
- Conducted ANOVA tests on 253 combinations of crime types to evaluate statistical significance.

## Key Findings
- **Central and West Chicago:** Neighborhoods like West Garfield Park, the Loop, and Near South show the highest arrest and no-arrest rates. These areas stand out prominently in the data. 
- **Northern Areas:** Neighborhoods such as Edgewater, Uptown, Lincoln Park, and West Town consistently report lower crime rates and fewer arrests.

## Limitations and Future Work
**Data Scope:** The dataset lacked the socioeconomic variables necessary for a comprehensive understanding of crime patterns. Incorporating socioeconomic factors in future work could provide deeper insights into the underlying dynamics of crime and inform targeted interventions.

## Libraries 
Numpy, pandas, geopandas, geojson, Matplotlib, scipy, sklearn, pysal, shapely, altair

