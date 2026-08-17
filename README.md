# Quality of Life Analysis

Exploratory data analysis of a country-level Quality of Life dataset, examining how factors like purchasing power, safety, healthcare, climate, cost of living, and pollution relate to overall quality of life across countries.

## Overview

Quality of life is a multifaceted concept shaped by economic, social, and environmental factors. This project explores a country-level dataset to uncover which factors most strongly correlate with quality of life outcomes, and surfaces those patterns through visualization.

## Tech Stack

- **Data handling:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, Plotly Express, GeoPandas
- **Modeling/ML:** scikit-learn (KMeans, LinearRegression, LabelEncoder)

## Data Cleaning

The raw dataset required non-trivial cleanup before analysis:

- Removed inconsistent null representations (`"NaN"`, `"nan"`, `"NAN"`) and normalized them to proper `NaN` values
- Stripped stray formatting artifacts (quotes, colons) from scraped string fields
- Handled missing numeric values via **median imputation** rather than dropping rows, to preserve as much of the (already limited) country-level sample as possible
- Encoded categorical fields (e.g. Safety Category) for inclusion in correlation analysis

## Analysis

- **Correlation matrix / heatmap** across all numeric and encoded categorical features
- **Distribution analysis** of quality-of-life scores and other metrics via histograms
- **Top 10 countries** ranked by Quality of Life Value
- **Category breakdowns** (Very High → Very Low) for metrics like Safety, visualized with boxplots
- **Country-level radar chart** comparing a single country (Germany) across all metrics
- **Geographic choropleth map** showing the global distribution of Quality of Life scores

## Key Insights

1. Countries with higher purchasing power tend to have a higher quality of life.
2. Safety and healthcare are strongly correlated with quality of life.
3. Pollution and traffic commute time negatively impact quality of life.

## Recommendations

1. Governments should prioritize improving safety and healthcare systems.
2. Reducing pollution and improving transportation infrastructure can meaningfully enhance quality of life.
3. Lower-scoring countries can look to top-performing countries as models for improvement.

## Project Structure

```
Quality of Life/
├── datasets/
│   └── Quality_of_Life.csv
└── Quality_of_Life_Final.ipynb
```

## Requirements

```
pandas
numpy
seaborn
matplotlib
geopandas
scikit-learn
plotly
```
