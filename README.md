# Spatial-Temporal Analysis of COVID-19 Spread and Social Determinants of Health

A geospatial analysis examining the spread of COVID-19 at the county level, with focus on identifying spatial patterns, disease clusters, and relationships with social determinants of health.

## Project Overview

This project analyzes COVID-19 case data across multiple states to:
- Map disease spread over time using choropleth visualizations
- Identify statistically significant disease hotspots using spatial statistics
- Examine correlations between COVID-19 outcomes and social vulnerability factors
- Demonstrate proficiency in GIS, spatial statistics, and epidemiological data analysis

**Current Status:** Minimum Viable Product (MVP) - Temporal snapshot analysis for California and Virginia complete

## Key Features

- **Temporal Analysis**: Snapshot maps showing disease progression at three critical time points
  - Early Pandemic (April 2020)
  - Winter Peak (January 2021)
  - Later Stage (October 2021)

- **Spatial Statistics** *(In Progress)*:
  - Global Moran's I for spatial autocorrelation
  - Local indicators of spatial association (LISA)
  - Getis-Ord Gi* hotspot analysis

- **Data Integration**: Multi-source data pipeline combining:
  - NYT COVID-19 county-level time series data
  - US Census Bureau TIGER/Line shapefiles
  - CDC Social Vulnerability Index *(Planned)*
  - Census demographic data *(Planned)*

## Technologies Used

**Languages & Libraries:**
- Python 3.x
- GeoPandas - Spatial data manipulation
- Pandas - Data processing
- Matplotlib/Plotly - Visualization
- PySAL/ESDA - Spatial statistics *(Planned)*
- Jupyter Notebooks - Analysis workflow

**Data Sources:**
- [NYT COVID-19 Data](https://github.com/nytimes/covid-19-data)
- [US Census Bureau TIGER/Line](https://www.census.gov/geographies/mapping-files.html)
- [CDC Social Vulnerability Index](https://www.atsdr.cdc.gov/placeandhealth/svi/)

## Project Structure
```
covid-spatial-analysis/
├── data/
│   ├── raw/              # Original downloaded data (not tracked in git)
│   ├── processed/        # Cleaned, analysis-ready data
│   └── README.md         # Data documentation
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb     # Planned
│   ├── 04_spatial_analysis.ipynb         # Planned
│   └── 05_visualization.ipynb            # Planned
├── src/                  # Reusable Python modules (future)
├── outputs/
│   ├── figures/          # Generated visualizations
│   └── maps/             # Final map products
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## Installation & Setup

### Prerequisites
- Python 3.8+
- pip package manager

### Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/covid-spatial-analysis.git
cd covid-spatial-analysis
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Run data collection**
```bash
jupyter notebook notebooks/01_data_collection.ipynb
```

*Visualizations available in `outputs/figures/`*

## Methodology

### Data Processing Pipeline
1. Download county-level COVID-19 case data from NYT GitHub repository
2. Acquire US Census county boundary shapefiles (2020)
3. Standardize FIPS codes for accurate geographic matching
4. Filter to target states and temporal snapshots
5. Merge disease data with geographic boundaries
6. Calculate rates and derived metrics

### Spatial Analysis Approach *(In Progress)*
- **Global Spatial Autocorrelation**: Moran's I statistic to test for overall spatial clustering
- **Local Hotspot Detection**: Getis-Ord Gi* to identify statistically significant clusters
- **Temporal Comparison**: Track how spatial patterns evolve over time

## Next Steps

- [ ] Add Census demographic variables (population, poverty, age structure)
- [ ] Incorporate CDC Social Vulnerability Index
- [ ] Calculate disease rates per 100,000 population
- [ ] Perform complete spatial statistics analysis (Moran's I, LISA, Gi*)
- [ ] Build interactive dashboard for exploration
- [ ] Expand analysis to additional states
- [ ] Add predictive modeling component

## Key Insights *(To Be Updated)*

*This section will be populated as analysis progresses*

## Limitations

- Current analysis uses raw case counts rather than population-adjusted rates
- Does not yet account for testing availability variations across counties
- Social determinant correlations pending additional data integration
- Spatial statistics implementation in progress

## Author

Luke Hatchl  
hatchl.luke24@gmail.com

## License

This project is licensed under the MIT License - see LICENSE file for details.

## Acknowledgments

- New York Times for maintaining open COVID-19 data
- US Census Bureau for geographic boundary files
- CDC for Social Vulnerability Index data

## References

- NYT COVID-19 Data Repository: https://github.com/nytimes/covid-19-data

---

*Last Updated: February 4 2026*  
*Project Status: Active Development*