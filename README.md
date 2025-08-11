# Predicting Global CO2 Emissiomns to Enhance Energy Sustainability

A data science project focused on predicting global carbon dioxide ($CO_2$) emissions using machine learning. By analyzing worldwide energy consumption patterns and demographic data, this project aims to provide an advanced approach for forecasting $CO_2$ emissions and identifying key drivers to enhance energy sustainability.

---

## Project Overview

The burning of fossil fuels for electricity, heat, and transport accounts for approximately 90% of global carbon emissions, making it a primary driver of climate change. This project uses a machine learning approach to analyze global energy and demographic data to build a predictive model for $CO_2$ emissions. The goal is to provide a tool that can not only forecast emissions but also help identify the most impactful factors for reducing carbon footprints and promoting sustainable energy sources.

---

## Data Sources

* **Global Energy Consumption and Generation:** This dataset from Our World in Data contains country-level energy consumption records from 2000-2020.
  * Features include: per capita energy consumption, share of fossil fuels (coal, oil, gas), and renewables (wind, solar, hydro, nuclear).
  * Source: [https://ourworldindata.org/grapher/access-to-electricity-vs-gdp-per-capita](https://ourworldindata.org/grapher/access-to-electricity-vs-gdp-per-capita)

* **World Demographics per Country:** This dataset from the U.S. Census Bureau provides demographic information for each country.
  * Features include: population count, area, population density, and growth rate.
  * Source: [https://www.census.gov/data-tools/demo/idb/#/table](https://www.census.gov/data-tools/demo/idb/#/table?COUNTRY_YEAR=2024&COUNTRY_YR_ANIM=2024&menu=tableViz&quickReports=CUSTOM&CUSTOM_COLS=AREA_KM2,POP,GR,RNI,POP_DENS,MEDAGE_F,MEDAGE_M,NATINCR,TFR,CBR,GRR,E0,CDR,DEATHS,NMR,NIM&TABLE_RANGE=2000,2020&TABLE_YEARS=2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014,2015,2016,2017,2018,2019,2020&TABLE_USE_RANGE=Y&TABLE_USE_YEARS=N&TABLE_STEP=1)

---

## Methodology

* **Data Cleaning and Preparation:**
  * Merged the two datasets on common parameters (country and year).
  * Standardized column names, handled null values by replacing them with the mean, and identified and validated outliers.
  * Performed data extractions and feature transformations to prepare the data for modeling.

* **Feature Engineering & Dimensionality Reduction:**
  * Correlation analysis showed that fossil fuels are positively correlated with $CO_2$ emissions, while renewable sources are negatively correlated.
  * Used **Principal Component Analysis (PCA)** to reduce the number of features to a highly correlated subset, retaining the most essential information for prediction.
  * Split the data into an 80:20 training and testing ratio.

* **Model Development and Evaluation:**
  * Trained nine different regression models to predict $CO_2$ emissions.
  * Evaluated models using R-squared ($R^2$), Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).
  * Performed **hyperparameter tuning** using a grid search algorithm on the best-performing models to find optimal parameters.

---

## Results

* Initial analysis showed a strong positive correlation between fossil fuel consumption and $CO_2$ emissions and a strong negative correlation with renewable energy sources.
* The **Random Forest Classifier** and **K-Nearest Neighbor (KNN)** models demonstrated the highest performance, achieving $R^2$ scores over **0.91**.
* Hyperparameter tuning on the KNN model further improved its accuracy, resulting in an optimal $R^2$ score of **0.918**. The model's key parameters were tuned to `n_neighbors=9`, `p=1`, and `weights='distance'`.

---

## Challenges and Limitations

* The dataset is limited to $CO_2$ as the primary greenhouse gas, which does not provide a complete picture of overall climate impact.
* The economic and ethical challenges of transitioning to renewable energy, such as high initial costs and land requirements, are important factors not fully captured in the data.
* Data from less developed countries may be sparse, which can impact the model's global generalizability.

---

## Technology Stack

* **Programming Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Tools:** Jupyter Notebook

---

## Contact

For questions or collaboration, please reach out via [E-mail](sayalinage@gmail.com) or connect on [LinkedIn](https://www.linkedin.com/in/sayali-nage-34303b136/).

---
