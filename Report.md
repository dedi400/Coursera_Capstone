# Neighbourhood recommendation for movers
## 1. Introduction and Description of Business Problem
This is the Capstone project of IBM Data Sicence Professional Certificate. It was required to prepare a data science project that using geological data and *foursquare.com* information. As I live in Budapest (capital of Hungary) I wanted to include this city to the project. So I came up with the following idea: let's assume that someone in Budapest gets an opportunity to work in London, New York or Toronto. I want to recommend her/him similar neighbourhoods to move with the family.

Just as in previous weeks I'm going to calculate "similarity" by looking for similar facilities/venues in the neighbourhood. I want to focus on facilities that are important to families with children, so I'm going to give some facilities/venues (nurseries, schools, playgrounds, parks, medical centers) higher weight in this project. The final target is to prepare DataFrame that lists 5 most similar neighbourhoods in London/New York/Toronto for each neighbourhood in Budapest.
## 2. Description of Data
For this project I'm going to use the following sources:
1. **Neighbourhood names** that are geocoded with their centroid coordinates:
    - I'm reusing the DataFrames for New York and Toronto from the previous weeks
    - For London neighbourhoods I'm web scraping outer postal codes from this wiki page: https://en.wikipedia.org/wiki/London_postal_district
    - For Budapest neighbourhoods it was not that simple. I found a Hungarian webpage from where geographical data can be downloaded (https://data2.openstreetmap.hu/hatarok/index.php?admin=10) I got an *.shp* file that must have been converted to neighbourhood centroids and saved to a *.csv* file.

2. **Geocoding** London neighbourhoods with *Google Maps API*. (The other cities are already geocoded in previous sessions) I'm using Google Maps as I realized that OpenStreetMap gives incorrect results if I put only postal codes as search keywords.

3. *Foursquare.com* searches for **facilities and venues** within the neighbourhoods. The tipical venues include restaurants, shops, bakeries, etc. I may use additional *Google Places* searches for special facilities (e.g. playgrounds, nurseries) if the original search is not satisfactory. The disadvantage of Google Places search is that it provides only 20 results with one request so I will not fully replace Foursquare. Though I found Google more precise with non-profit (or governmental) facilities (e.g. clinics, libraries, playgrounds etc.)

With the list of the nearby facilities for each neighbourhoods I'm going to calculate a similarity index among Budapest neighbourhoods and other cities. 
## 3. Methodology
## 4. Results
## 5. Discussion
## 6. Conclusion
