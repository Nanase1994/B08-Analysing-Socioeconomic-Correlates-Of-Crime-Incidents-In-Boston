# B08-Analysing-Socioeconomic-Correlates-Of-Crime-Incidents-In-Boston
This project analyzes the correlation between socioeconomic factors and crime incidents in the Boston area.

📘 Executive Summary

This project investigates how socioeconomic disparities correlate with crime distribution across Boston. By integrating Boston Police Department crime incident data with U.S. Census socioeconomic indicators (poverty rate, median household income), we conduct geospatial and statistical analyses to identify district-level inequalities in crime patterns.
Key findings reveal that:

Crime density clusters heavily in Dorchester, Roxbury, and Mattapan, aligning with poverty rates above 25%.

Wealthier districts (median income > $110,000) show significantly lower crime intensity.

Spatial correlation and heatmap visualization demonstrate that economic disadvantage is a strong predictor of crime prevalence.
The analysis highlights the importance of equitable socioeconomic policy and targeted policing strategies in mitigating crime concentration.

🎯 Project Motivation

Urban crime patterns are not randomly distributed — they reflect underlying socioeconomic structures. Understanding these relationships enables more data-driven public policy and resource allocation for community safety.
This project aims to:

Quantify the link between socioeconomic status (SES) and crime intensity.

Identify high-risk areas through spatial visualization and clustering.

Provide actionable insights for urban planning and law enforcement in Boston.

🧩 Data Sources
Dataset	Description	Source
crime_incident.csv	All reported crime incidents in Boston (with latitude/longitude, offense type, date, and district)	Boston Police Department Open Data Portal
ACS_S1901.csv	Median household income by census tract	U.S. Census Bureau (ACS 5-Year Estimates)
ACS_S1701.csv	Poverty status by census tract	U.S. Census Bureau (ACS 5-Year Estimates)
District_Boundaries.geojson	Spatial boundaries for Boston Police Districts	Boston GIS Open Data Portal
⚙️ Methodology & Structure
1. Data Cleaning & Preprocessing

Schema drift automation handled column inconsistencies across ACS datasets.

Type coercion & NA hygiene ensured numeric precision for SES indicators.

Text normalization standardized offense descriptions and district codes.

2. Geospatial Alignment

Constructed a tract–district crosswalk via centroid-based spatial join (geopandas.sjoin).

Reconciled boundary mismatches through nearest-neighbor reassignment.

3. Exploratory Data Analysis (EDA)

Visualized crime heatmaps using Folium.

Mapped poverty and income distributions with choropleth overlays.

Conducted correlation and regression to quantify SES–crime relationships.

4. Visualization

15 total figures were developed, including:

Folium heatmap of all incidents

Choropleth maps of poverty and income by district

Bar charts of offense types by SES group

Scatterplots linking income and crime counts

5. Key Insights

Geographic inequality: High-crime zones overlap with high-poverty tracts.

Economic gradient effect: As income rises, crime density declines sharply.

Policy implication: Targeted economic revitalization may reduce crime pressure more effectively than policing alone.

📊 Notebook Organization
Section	Description
1. Introduction & Motivation	Project goals and research rationale
2. Data Loading & Cleaning	Data preparation and validation
3. Exploratory Analysis	Spatial and statistical visualizations
4. Socioeconomic Correlation Analysis	Regression and clustering
5. Discussion & Insights	Interpretation of findings
6. Challenges & Limitations	Technical and analytical barriers
7. Conclusion	Summary and strategic recommendations
🧱 Challenges

Data Inconsistency: Varying ACS column codes across tables required pattern-based matching functions.

Spatial Misalignment: Tracts along district borders caused overlap errors, resolved through manual inspection.

Missing SES Values: Imputed median values to preserve analytical integrity.

Scaling: Handling large crime datasets (100k+ rows) with efficient geospatial joins.

📈 Conclusion

The findings confirm a clear geographic and socioeconomic divide in Boston’s crime distribution. Districts burdened by higher poverty rates face greater exposure to violent and property crimes.
The study underscores that addressing socioeconomic inequality is pivotal to sustainable crime reduction. Future work could integrate time-series analysis to explore temporal dynamics of these correlations.

📚 References

Boston Police Department Open Data: https://data.boston.gov

U.S. Census Bureau: American Community Survey (S1901, S1701)

Boston GIS Data Hub: https://boston.maps.arcgis.com

🤖 Generative AI Disclosure

In completing this project, our team utilized ChatGPT and GitHub Copilot as follows:

Idea Structuring: Brainstormed outline and refined research framing.

Code Debugging: Suggested improvements for geospatial joins, Folium visualization, and pandas operations.

Writing Assistance: Edited markdown narratives for conciseness and clarity.
All outputs were reviewed, validated, and adjusted by team members to maintain academic integrity and analytical rigor.

👥 Contributors

Kaixin Gao (Kevin Gao) — Data Cleaning, Geospatial Mapping, SES Analysis

[Add teammates here with respective roles]
