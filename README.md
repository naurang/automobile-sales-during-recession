# automobile-sales-during-recession
# Table of Contents
1. [Objectives](#objectives)
2. [Setup](#setup)
3. [Installing Required Libraries](#installing-required-libraries)
4. [Importing Required Libraries](#importing-required-libraries)
5. [Scenario](#scenario)
6. [Data Description](#data-description)
7. [Importing Data](#importing-data)
8. [Creating Visualizations for Data Analysis](#creating-visualizations-for-data-analysis)

## Objectives
- Create informative and visually appealing plots with Matplotlib and Seaborn.
- Apply visualization to communicate insights from the data.
- Analyze data through using visualizations.
- Customize visualizations.

## Setup
We will be using the following libraries:
- pandas for managing the data.
- numpy for mathematical operations.
- matplotlib for plotting.
- seaborn for plotting.
- Folium for plotting.

## Installing Required Libraries
The following required libraries are in the environment. You will need to install these libraries by removing the # sign before %pip in the code cell below.

```python
# All Libraries required for this lab are listed below. The libraries pre-installed on Skills Network Labs are commented.
# %pip install -qy pandas==1.3.4 numpy==1.21.4 matplotlib==3.5.0 seaborn folium
# Note: If your environment doesn't support "%pip install", use "!mamba install"
%pip install seaborn
%pip install folium
```

## Importing Required Libraries
We recommend you import all required libraries in one place (here):

```python
import numpy as np
import pandas as pd
%matplotlib inline
import matplotlib as mpl
import matplotlib.pyplot as plt
import seaborn as sns
import folium
```
You will require:
- Numpy for many scientific computing in Python
- Pandas for creating and working on dataframes, also for plotting directly on dataframe/series
- The inline backend to generate the plots within the browser [%matplotlib inline]
- Matplotlib and its pyplot package for plotting
- Seaborn for plotting

## Scenario
Creating plots which answer questions for analyzing "historical_automobile_sales" data to understand the historical trends in automobile sales during recession periods.
- Recession period 1 - year 1980
- Recession period 2 - year 1981 to 1982
- Recession period 3 - year 1991
- Recession period 4 - year 2000 to 2001
- Recession period 5 - year end 2007 to mid 2009
- Recession period 6 - year 2020 - Feb to April (Covid-19 Impact)

## Data Description
The dataset used for this visualization assignment contains historical_automobile_sales data representing automobile sales and related variables during recession and non-recession periods.

The dataset includes the following variables:
1. **Date**: The date of the observation.
2. **Recession**: A binary variable indicating recession period; 1 means it was recession, 0 means it was normal.
3. **Automobile_Sales**: The number of vehicles sold during the period.
4. **GDP**: The per capita GDP value in USD.
5. **Unemployment_Rate**: The monthly unemployment rate.
6. **Consumer_Confidence**: A synthetic index representing consumer confidence, which can impact consumer spending and automobile purchases.
7. **Seasonality_Weight**: The weight representing the seasonality effect on automobile sales during the period.
8. **Price**: The average vehicle price during the period.
9. **Advertising_Expenditure**: The advertising expenditure of the company.
10. **Vehicle_Type**: The type of vehicles sold; Superminicar, Smallfamilycar, Mediumfamilycar, Executivecar, Sports.
11. **Competition**: The measure of competition in the market, such as the number of competitors or market share of major manufacturers.
12. **Month**: Month of the observation extracted from Date.
13. **Year**: Year of the observation extracted from Date.

By examining various factors mentioned above from the dataset, we aim to gain insights into how recessions impacted automobile sales for your company.

## Importing Data
```python
from js import fetch
import io

URL = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DV0101EN-SkillsNetwork/Data%20Files/historical_automobile_sales.csv"
resp = await fetch(URL)
text = io.BytesIO((await resp.arrayBuffer()).to_py())
import pandas as pd
df = pd.read_csv(text)
print('Data downloaded and read into a dataframe!')
```

## Creating Visualizations for Data Analysis
1. Load and explore the dataset.
2. Create time series plots for automobile sales, GDP, unemployment rate, consumer confidence, and other variables.
3. Compare sales trends during recession and non-recession periods.
4. Visualize relationships between variables, e.g., sales vs. GDP, sales vs. unemployment rate, etc.
5. Customize visualizations for better readability and insight.
