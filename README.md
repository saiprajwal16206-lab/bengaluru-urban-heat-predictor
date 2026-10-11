# Bengaluru Urban Heat Island Predictor

A Jupyter Notebook project that uses machine-learning models to estimate land surface temperature (LST) at sampled locations in Bengaluru.

## What the notebook does

- Loads and cleans the tabular dataset
- Separates nearby locations into training and test groups
- Compares five models: Linear Regression, Random Forest, XGBoost, MLP, and a 1D CNN
- Shows the most useful model features
- Plots and maps predicted temperatures

## Results

Random Forest performed best in this experiment:

| Model | MAE (°C) | RMSE (°C) | R² |
|---|---:|---:|---:|
| Random Forest | 1.153 | 1.524 | 0.465 |
| 1D CNN | 1.271 | 1.584 | 0.422 |
| XGBoost | 1.259 | 1.636 | 0.384 |
| MLP | 1.294 | 1.657 | 0.368 |
| Linear Regression | 1.310 | 1.705 | 0.330 |

MAE is the average size of the model’s prediction error. R² describes how well its predictions match the measured values; closer to 1 is better.

## Dataset

The notebook expects a file named `ultimate_uhi_dataset_with_rwi.csv` in the same folder as the notebook.

Dataset source: [Predicting UHI Intensity](https://github.com/arnavvnn/Predicting-UHI-Intensity)

Check the dataset’s reuse terms before redistributing the CSV.

## Run the notebook

1. Download the notebook and dataset.
2. Put both files in the same folder.
3. Open the notebook in Jupyter.
4. Run the cells from top to bottom.

## Limitations

This project uses the locations and measurements available in the dataset. The map shows sampled points, not every place in Bengaluru. The “hotter” and “cooler” groups are relative to this dataset; they are not official heat warnings. This notebook estimates land surface temperature and does not forecast future weather.
