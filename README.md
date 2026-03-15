# Edmonton Crime Analysis (2025-2026)

## Overview
Analysis of 79,452 crime incidents across 407 Edmonton neighbourhoods 
using open data from Edmonton Police Service and Statistics Canada.

## Key Findings
- Prince Rupert has the highest crime rate among residential neighbourhoods (1,457 crimes per 1000 residents)
- Downtown has the most raw crime incidents (4,519) but ranks 11th by crime rate
- Non-violent property crime dominates across most Edmonton neighbourhoods
- Inner city neighbourhoods (McCauley, Boyle Street, Central McDougall) show higher rates of violent and disorder crimes

## Data Sources
- Edmonton Police Service crime incidents: communitysafetydataportal.edmontonpolice.ca
- Edmonton neighbourhood boundaries: data.edmonton.ca
- 2021 Federal Census population by neighbourhood: data.edmonton.ca

## Tools Used
- Python, Pandas, GeoPandas, Shapely, Matplotlib

## Notes
- Despite the filename suggesting 30 days of data, the dataset actually covers March 2025 to March 2026
- Crime rates use residential population which may overestimate crime in institutional areas like University of Alberta