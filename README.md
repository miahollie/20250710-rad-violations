# Analysis of NYC HPD Housing Code Violations
This repository includes code analyzing the New York City Department of Housing Preservation and Development's public housing code violations and open market orders data. The findings of this analysis were used in a [story](https://www.thecity.nyc/2025/12/10/nycha-rad-pact-boulevard-linden-violations/) published by the nonprofit newsroom THE CITY on December 10, 2025. 

## Data
This analysis uses three data sources:

- [NYC HPD Housing Code Violations](https://data.cityofnewyork.us/Housing-Development/Housing-Maintenance-Code-Violations/wvxf-dwi5/about_data): Choose the "Query Data" tool in the Actions dropdown, filter the data by InspectionDate, using a range from 01-01-2021 12:00:00 AM to 09:25:2025 11:59:59 PM. Download the file.
- [NYC HPD Open Market Orders (OMO) Charges](https://data.cityofnewyork.us/Housing-Development/Open-Market-Order-OMO-Charges/mdbu-nrqn/about_data): Download the file.
- [PACT Developments Directory as of July 1, 2025](https://www.nyc.gov/assets/nycha/downloads/pdf/radpact-guide.pdf): Download the file. 

## Pre-requisites
The pact-env folder includes all packages needed to complete this analysis.

## Methodology

#### 1_extract_developments.ipynb
- Iterate through the PDF and extract addresses
- Iterate through the PDF again to extract development names, boroughs, units, and transfer dates
- Perform a series of edits to the addresses where additional information was not assigned
- Clean the addresses
- Save to file
#### 2_violations.ipynb
- Read RAD addresses file and housing code violations file
- Clean violations file
- Merge to the two files together on address and borough columns
- Perform analysis
#### 3_omo.ipynb
- Read RAD addresses file and omo charges file
- Clean charges file
- Merge to the two files together on address and borough columns
- Perform analysis
#### 4_leftovers.ipynb
- This file is not part of the final analysis. It includes code used in previous iterations of this analysis that I'd like to save and reference in the future. 

## Licensing
All code in this repository is available under the MIT License. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?
Contact Mia Hollie at mhollie@thecity.nyc.

