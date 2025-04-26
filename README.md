# Comparative Analysis of Neighborhoods | Introduction

## Business Brief
As someone who's been used to relocate every two to three years, I frequently find myself needing to research new cities to assess their layouts and available amenities in order to decide where to settle next. This ongoing need to evaluate new locations drives the development of a tool that could:

***Recommend the best areas to live within my target city based on my personal criteria.***

## Problem Statement
The purpose of this project is to assist individuals moving to a specific city in selecting a suitable neighborhood to live in based on their informed preferences and our data-driven recommendations. 

The tipical new resident would be considering the following factors when searching at a rental:

- His personal rental budget bracket;
- His need to access a studio, 1 bedroom, 2 bedrooms or 3 bedrooms accomodations.
- His preferences for proximity to certain amenities. A family-driven profile would prioritise to be nearby outdoor areas like parcs, the ability to handle health emergencies at hospitals, the accessiblity to educational facilities from nursery to college and to have a decent range of retail shops and grocery stores. Conversely, a social-driven profile would prioritise the accessibility to restaurants, bars, recreational facilities like cinemas or museums and to retail and shopping. Finally, a career-driven profile would prioritise the.

Hence the goal is to:

***Guide users in identifying the ideal neighborhood within a chosen city that best matches their budget, accomodation size needs and preferences in amenities proximity.***

The expect output will work as follows:

The user will select the city within the available list, his budget, his accomodation size preferences and his profile. The analysis will retrieve and compare data whithin the city neighborhoods, venues and rents to provide the users with visual results.

Along the journey, we will enjoy the opportunity to analyse and compare the cities property markets and urban development.

## Scope of work
The analysis will not:
- Include neighborhoods from other parts of the city we want to investigate.
- Include long-term forecasting in real estate prices or demographic predictions. I will focus on: 
- Include in-depth analysis of complex social or cultural dynamics in the city. I will focus on basic amenities and housing prices.
- Include other cities than Paris, Montreal, Toronto, Ottawa, Quebec city.

- ## Tools

**Data Access and Web Scraping**
- Beautiful Soup & Requests: to access external data via web scraping and http requests
- time: to set up a timer when calling for APIs

**Data Storage and File Handling**

- JSON: to handle JSON files.
- openpyxl: to handle Excel files.
- XML: to separate data from presentation and XML stores data in plain text format.
- Zipfile and BytesIO: to read and extract from zip folders

**Data Manipulation and Processing**
- Pandas: to create and manipulate dataframes.
- Numpy: to handle data in a vectorized manner.
- re : to match patterns and manipulate strings through regular expressions (regex).
- unicodedata: to handle accents across many languages and characters.
- unidecode: to normalize and handle non-ASCII characters.
- fuzzywuzzy: for string similarity and fuzzy matching.
- difflib.get_close_matches: to find close matches between strings.

**Geolocation and Mapping**
- ArcGIS geocoder API: get latitude and longitude for specific postal codes combined with the city name.
- Nominatim geocoder API: the OpenStreetMap geocoding service will help us find the geographical coordinates of the whole city we are investigating.

**Statistical Analysis and Clustering**
- scipy.stats: for statistical functions and hypothesis testing.
- researchpy: for statistical testing and data summaries.
- Scikit-Learn: to implement unsupervised machine learning like clustering.

**Data Visualization**
- Matplotlib: to create visualizations and to plot results.
- Folium: to visualize the clustering of neighborhoods using interactive maps.

**Miscellaneous**
- Warnings: to stop non useful warning messages.

## Sources

**Wikipedia**

Select wikipedia pages listing the most up to date postal codes, neighborhoods and boroughs of the cities we want to investigate.
- Halifax: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_B
- Quebec City: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_G
- Montreal: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_H
- Ottawa: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_K
- Toronto: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M
- Vancouver: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_V
- Paris: https://fr.geneawiki.com/wiki/Liste_des_quartiers_de_Paris

**Foursquare**

Collect data on local amenities and services such as cafes, schools, shops, hospitals, etc. Use the location platform providing data through its API to retrieve the most up to date venue names, types of venues or categories, and their location. Though we should note that with the free http request version, we will be limited to 100 places per search.
- Venues: https://docs.foursquare.com/developer/reference/foursquare-apis-overview  
- Categories: https://docs.foursquare.com/data-products/docs/categories#places-api--flat-file

**Canada Mortgage and Housing Corporation**

This is Canada's national housing agency. It is responsible for providing reliable housing market data and analysis. We will retrieve 2023 canadian median rent prices.
- Link: https://www.cmhc-schl.gc.ca/professionnels/marche-du-logement-donnees-et-recherche/donnees-sur-le-logement/tableaux-de-donnees/donnees-sur-le-marche-locatif/enquete-sur-les-logements-locatifs-centres-urbains-loyers-moyens

**French Public Housing Data**

The website data.gouv.fr is the French government's open data platform, managed by Etalab, which provides public access to datasets from various governmental institutions. We will also retrieve 2023 french median rent prices.
- Link: https://www.data.gouv.fr/fr/datasets/carte-des-loyers-indicateurs-de-loyers-dannonce-par-commune-en-2023/#/resources

## Workflow
- [1] Wikipedia Data Preparation
- [2] Geolocation Data Preparation
- [3] Venue Data Preparation
- [4] Canadian Rent Data Preparation
- [5] French Rent Data Preparation
- [6] Descriptive Analysis
- [7] Explanatory Analysis
- [8] Predictive Analaysis
- [9] Conclusive Insights
