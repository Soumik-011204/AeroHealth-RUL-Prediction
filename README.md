# AeroHealth: Turbofan Engine RUL Prediction

A machine learning and deep learning project for predicting the Remaining Useful Life (RUL) of turbofan engines using the NASA C-MAPSS FD001 dataset.

## Project Overview

AeroHealth compares traditional machine learning models with recurrent neural networks for predictive maintenance.

## Models Implemented

- Linear Regression
- Ridge Regression using 30-cycle windows
- Random Forest
- Random Forest using 30-cycle windows
- LSTM
- GRU
- GRU with Temporal Attention

## Dataset

NASA C-MAPSS FD001 simulated turbofan engine dataset.

Dataset source:
https://data.nasa.gov/dataset/cmapss-jet-engine-simulated-data

## Methodology

- Remaining Useful Life (RUL) target capped at 125 cycles
- Input sequence length of 30 cycles
- Engine-wise training and validation split
- Feature selection and scaling using training data
- Evaluation using MAE, RMSE, R-squared and NASA score

## Reported Results

The current report identifies GRU as the best model for MAE, with an average reported MAE of 10.78 cycles across five runs. These results should be reproduced from the notebook before being treated as independently verified.

## Tools and Technologies

Python, Jupyter Notebook, NumPy, Pandas, scikit-learn, TensorFlow/Keras and Matplotlib.

## Limitations

The experiments use simulated FD001 data. The model has not been validated for real-world aircraft maintenance.

## Author

Soumik Sarkar
B.Tech, Computer Science and Engineering
Jorhat Engineering College
