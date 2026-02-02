# Data Directory

## Raw Data Sources

### NYT COVID-19 Data
- **File**: `nyt_covid_counties.csv`
- **Source**: https://github.com/nytimes/covid-19-data
- **Updated**: [Date you downloaded it]
- **Description**: County-level daily cases and deaths

### County Shapefiles
- **Files**: `tl_2020_us_county.*`
- **Source**: US Census Bureau TIGER/Line
- **Year**: 2020
- **CRS**: EPSG:4269 (NAD83)

### CDC Social Vulnerability Index (Optional)
- **File**: `SVI2020_US_county.csv`
- **Source**: https://www.atsdr.cdc.gov/placeandhealth/svi/
- **Manual download required**

## Notes
- Raw data files are NOT committed to git (see .gitignore)
- Download scripts in `notebooks/01_data_collection.ipynb`