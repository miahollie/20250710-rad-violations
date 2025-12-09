# Analysis of NYC HPD Housing Code Violations
This repository includes code analyzing the New York City Department of Housing Preservation and Development's public housing code violations and open market orders data. The findings of this analysis were used in a story published by nonprofit newsroom THE CITY on TKDATE. 

## Data
This analysis uses three spreadsheets, all of which are derived from NYC OpenData, and one PDF file. 

Note: I've downloaded my data to quicken processing times (the API take ~20 minutes to load the same amount of data). One of the cons to this (other than the obvious, which is storing a lot of data locally), is that I'm unable to share the exact files I used via this repository. I've included notes below on how I filtered the data before downloading it from OpenData.

- One 2021-Onward CSV: Choose the "Query Data" tool in the Actions dropdown, filter the data by InspectionDate, using a range from 01-01-2021 12:00:00 AM to 09:25:2025 11:59:59 PM. Download the file.
- One 2015-2021 file: Choose the "Query Data" tool in the Actions dropdown, filter the data by InspectionDate, using a range from 01-01-2015 12:00:00 AM to 12:31:2020 11:59:59 PM. Download the file.
- One OMO file: Download all entries in HPD's Open Market Orders Charges file, found here.
- One RAD Developments file: This PDF may be found on NYCHA's website here. It's update every six months. 

## Methodology

1. Extract data from the PDF, write to a file.
2. Match RAD developments to those found in the housing violations files using both address and borough.
3. Perform Analysis.
4. Match RAD developments to OMO data using both address and borough.
5. Perform Analysis.

## Licensing
All code in this repository is available under the MIT License. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?
Contact Mia Hollie at mhollie@thecity.nyc.

