# Terrorism & Economics

## Overview
This was a mostly self-guided project aimed at determining whether or not there is a link between incidents of terrorism and economic factors, specifically GDP per capita, inflation, and unemployment. The final results of my analysis can be found in the script "6.7 Creating Data Dashboards" and as an [interactive Tableau presentation](https://public.tableau.com/app/profile/errol.hinkamp/viz/TerrorismEconomics/TerrorismEconomics#1).

## Background
The final project of the CareerFoundry data analytics course was to perform a complete analysis using data that the student obtained themselves from the internet on a topic of their choosing. Initially, I began an analysis of global conflict events over time using information from the [GDELT Conflict Dataset](https://www.kaggle.com/vladproex/gdelt-conflict-events-1979-2021). As I progressed, I noticed some irregularities in the data that made me question its validity. Specifically, as time went on the number of conflict events grew to such astronomically high levels that they could not be believed.

Rather than continuing with bad data, I chose perform my analysis using several new datasets. I chose a list of terrorist attacks from the [Global Terrorism Database](https://www.start.umd.edu/gtd/access/) and information on [GDP per capita](https://data.worldbank.org/indicator/NY.GDP.PCAP.PP.CD?view=chart), [inflation](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?view=chart), and [unemployment](https://data.worldbank.org/indicator/SL.UEM.TOTL.ZS?view=chart) from the World Bank.

The project management folder contains the documentation for the CareerFoundry assignment and the terrorism dataset.

The data folder contains all of the datasets used over the course of this analysis, both good and bad. The "original" subfolder contains the datasets as they were downloaded; the only change is their filenames. The original terrorism dataset is not present, as it is too large to upload. The "intermediate" subfolder contains small edits that were done in Excel; mostly formatting issues so that they would load in Python. This includes an edited version of the terrorism dataset, with far fewer columns and some edits to the country names to make them consistent with current political borders. The "prepared" subfolder contains the final datasets which form the basis of the analysis.

The script folder contains all of the Python scripts made over the course of the project. The first six scripts represent the assignments done using the original, bad dataset (6.3 had to be uploaded as a .rar due to size contraints). The final script, "6.7 Creating Data Dashboards," utilizes the new datasets and is the only one relevant to the final analysis.

The analysis folder contains a choropleth map made in Python as part of script "6.3 Geographical Visualizations." It uses the old dataset and is irrelevant to the final analysis, but serves as evidence of just how crazy the original conflict dataset was.

## Data Sources
[GDELT Conflict Events (1979-2021)](https://www.kaggle.com/vladproex/gdelt-conflict-events-1979-2021) ___Not used in final analysis___

[Country Polygons as GeoJSON](https://datahub.io/core/geo-countries#resource-countries) ___Not used in final analysis___

[Global Terrorism Database](https://www.start.umd.edu/gtd/access/)

[GDP per capita, PPP (current international $)](https://data.worldbank.org/indicator/NY.GDP.PCAP.PP.CD?view=chart)

[Inflation, consumer prices (annual %)](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?view=chart)

[Unemployment, total (% of total labor force) (modeled ILO estimate)](https://data.worldbank.org/indicator/SL.UEM.TOTL.ZS?view=chart)

## Limitations

The main limitation of this analysis was gaps in the data. Much of the economic data was incomplete; many datasets didn't contain information prior to 1990 and not all countries were equally well-reported. Since I wanted my final analysis to be based on a complete picture of the number of attacks, GDP per capita, inflation, and unemployment of a given country in a given year, a single missing datapoint meant that the entire row had to be discarded. I still had 4000+ rows to work with, but more information would obviously have been preferred.

Additionally, the Global Terrorism Database and World Bank datasets used different lists of countries. The World Bank datasets used current political borders while the Global Terrorism Database listed the countries ___as they existed at the time of the attack.___ I tried to rectify them as best I could by updating country names to be consistent with current borders and--in cases where countries were unified (like Germany) or dissolved (like Yugoslavia)--used the coordinates provided in the terrorism dataset to determine in which present-day country the event took place. There were a handful of instances where no coordinates were provided; in those cases I made no changes to the country name. There were also certain regions that were present in one dataset but not in the other (British overseas territories, for example) that I was unable to reconcile. These instances were left out of the final analysis.
