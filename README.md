# Renewable Energy Generation & Weather Pattern Analytics Using Python

**Student:** Aarya Saxena  
**Roll Number:** 24202803  
**Course:** Bachelor of Science (B.Sc.)  
**College:** Government P.G. College, Dholpur  
**University:** Maharaja Surajmal Brij University  
**Program:** IBM SkillsBuild Data Analytics with AI Academic Internship (BharatCares in association with AICTE)

## Project overview

This project demonstrates an end-to-end data analytics workflow for daily solar generation across four illustrative solar sites. It includes data-quality checks, calendar feature engineering, descriptive analysis, visualisations, correlation exploration, and a time-based regression-model evaluation.

> **Important data note:** `renewable_energy_weather_dataset.csv` is a synthetic educational dataset created for this project. It is not official government data, real plant telemetry, measured weather data, or a real-world survey. The findings and model metrics describe this simulated dataset only.

## Files

| File | Purpose |
|---|---|
| `AaryaSaxena_Renewable_Energy_Analytics.ipynb` | Executable Jupyter notebook containing analysis and model evaluation. |
| `renewable_energy_weather_dataset.csv` | 4,384 daily records and 15 fields for analysis. |
| `requirements.txt` | Python dependencies used by the notebook. |
| `AaryaSaxena_ProjectReport.docx` | Formatted internship project report. |
| `README.md` | Project overview and run instructions. |

## Dataset summary

- Time period: 1 January 2022–31 December 2024
- Illustrative sites: Dholpur Solar Park, Jaipur Solar Field, Jodhpur Sun Array, Udaipur Solar Station
- Rows: 4,384 (one daily record for each of four sites)
- Columns: 15
- Main target: `solar_generation_mwh`
- Main fields: date, site, district, installed capacity, temperature, solar-resource indicator, cloud cover, humidity, wind, rainfall, panel cleanliness, outage hours, plant availability, demand indicator and solar generation.

The site names and all values are for scenario-based education. Do not interpret them as records from actual facilities.

## Analyses included

1. Dataset structure, missing-value and duplicate checks.
2. Summary indicators and site-level comparison.
3. Monthly and seasonal trends.
4. Weather/operations correlations and scatter plots.
5. Linear Regression and Random Forest regression.
6. MAE, RMSE and R² evaluation on a later-period holdout (training observations before 1 May 2024; testing observations from 1 May 2024 onward).
7. Feature-importance visualisation and limitations.

## Run the project

1. Install Python 3.10 or newer.
2. Download/extract the project files into one folder.
3. In a terminal, install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open `AaryaSaxena_Renewable_Energy_Analytics.ipynb` and run all cells from top to bottom. Keep the CSV in the same folder as the notebook.

## Reproducibility and interpretation

The notebook reads the included CSV; it does not silently create a new dataset each time. Model preprocessing is wrapped in a scikit-learn pipeline and a fixed date boundary is used for the evaluation split. Results depend on the included synthetic data and package versions.

The best model's metrics in this run are approximately:

- **Random Forest:** MAE 2.31 MWh, RMSE 3.16 MWh, R² 0.983
- **Linear Regression:** MAE 3.10 MWh, RMSE 4.37 MWh, R² 0.967

These are demonstration results, not a promise of performance on measured energy data. A real deployment would require authorised plant measurements, validation of sensors and units, rolling time-based evaluation, comparison with simple baselines and engineering review.

## Suggested GitHub repository

**Repository name:** `AaryaSaxena_Renewable_Energy_Analytics`  
**Description:** `B.Sc. Data Analytics with AI internship project analysing synthetic solar-generation and weather patterns using Python, visualisation and regression models.`

## Reference documentation

- pandas: https://pandas.pydata.org/docs/
- NumPy: https://numpy.org/doc/
- Matplotlib: https://matplotlib.org/stable/
- Seaborn: https://seaborn.pydata.org/
- scikit-learn: https://scikit-learn.org/stable/user_guide.html
- Jupyter: https://docs.jupyter.org/
