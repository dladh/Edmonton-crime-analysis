# Edmonton Crime Analysis (2025-2026)

## Overview
End-to-end geospatial analysis of 79,452 crime incidents across 407 Edmonton 
neighbourhoods using open data from Edmonton Police Service and Statistics Canada.

## Key Findings
- **Boyle Street, McCauley and Central McDougall** form a distinct high-violence 
  cluster — averaging 362 crimes per 1,000 residents with the highest violent 
  crime rates in the city
- **Downtown** is a unique outlier — highest raw crime count (4,519) but driven 
  by non-violent and disorder crimes rather than violence
- **Prince Rupert** has the highest residential crime rate among non-clustered 
  neighbourhoods (1,457 per 1,000 residents)
- **248 out of 276 neighbourhoods** (90%) fall into the safe residential cluster 
  with an average crime rate of just 49 per 1,000
- K-means clustering (k=4) identified 4 distinct crime profiles across Edmonton

## Visualizations
- Edmonton map coloured by most common crime type per neighbourhood
- Top 20 neighbourhoods by raw crime count
- Top 20 neighbourhoods by crime rate per 1,000 residents
- Edmonton map coloured by k-means crime cluster

## Methodology
1. Loaded and cleaned 79,452 crime incidents from Edmonton Police Service
2. Resolved coordinate system mismatches and validated data quality
3. Used GeoPandas spatial join to match GPS coordinates to 407 neighbourhood boundaries
4. Integrated 2021 Federal Census population data to calculate crime rates
5. Applied k-means clustering (k=4, selected via elbow method) on 8 features per neighbourhood

## Data Sources
- Edmonton Police Service crime incidents: communitysafetydataportal.edmontonpolice.ca
- Edmonton neighbourhood boundaries: data.edmonton.ca
- 2021 Federal Census population by neighbourhood: data.edmonton.ca

## Tools Used
Python, Pandas, GeoPandas, Shapely, Matplotlib, scikit-learn

## Limitations
- Despite the filename suggesting 30 days, the dataset covers March 2025 to March 2026
- Crime rates use residential population — overestimates crime in institutional areas 
  like University of Alberta
- 124 neighbourhoods excluded from clustering due to missing census population data
- K-means assumes spherical clusters of similar size — DBSCAN considered as alternative 
  for robustness to outliers

## How to Run
1. Download crime data from communitysafetydataportal.edmontonpolice.ca
2. Download neighbourhood boundaries and census data from data.edmonton.ca
3. Place CSVs in the data/ folder
4. Run notebooks/analysis.ipynb