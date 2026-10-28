# AeroHealth: Turbofan Engine Remaining Useful Life Prediction

A machine learning and deep learning project for predicting the **Remaining Useful Life (RUL)** of turbofan engines using the NASA C-MAPSS FD001 simulated dataset.

## Project Overview

AeroHealth investigates predictive maintenance by comparing traditional machine learning algorithms with recurrent neural networks. The goal is to estimate how many operational cycles remain before a turbofan engine reaches its end of useful life.

## Models Implemented

The project evaluates seven model configurations:

- Linear Regression
- Ridge Regression with 30-cycle windows
- Random Forest
- Random Forest with 30-cycle windows
- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)
- GRU with Temporal Attention

## Dataset

- **Dataset:** NASA C-MAPSS FD001
- **Data type:** Simulated turbofan engine degradation data
- **Source:** [NASA C-MAPSS Dataset](https://data.nasa.gov/dataset/cmapss-jet-engine-simulated-data)

The dataset contains engine operating conditions and sensor measurements used to model degradation over successive operational cycles.

*Note: Download the dataset from the source and follow the notebook's expected file paths before running the experiments.*

## Methodology

The project follows these main steps:

1. **Data preprocessing:** Prepare engine operating data and calculate RUL targets.
2. **RUL capping:** Cap target values at 125 cycles.
3. **Sequence generation:** Use a 30-cycle input window for sequence-based experiments.
4. **Data splitting:** Split training and validation data by engine.
5. **Feature processing:** Perform feature selection and scaling using training data.
6. **Model training:** Train and compare traditional machine learning models and deep learning architectures.
7. **Evaluation:** Compare predictions using MAE, RMSE, R² and the NASA scoring metric.

## Reported Results

The current project report identifies GRU as the best model for Mean Absolute Error (MAE), with a reported average MAE of **10.78 cycles across five runs**.

The report also compares RMSE, R² and NASA score across the evaluated models.

**Reproducibility note:** These values are reported experimental results and should be independently confirmed by executing the notebook and checking its generated evaluation outputs.

## Tools and Technologies

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Data processing:** NumPy, Pandas
- **Machine learning:** scikit-learn
- **Deep learning:** TensorFlow/Keras
- **Visualization:** Matplotlib

## How to Run

1. Clone or download this repository.
2. Install the required Python packages listed in `requirements.txt`, once that file is available.
3. Download the NASA C-MAPSS dataset.
4. Place the dataset in the directory expected by the notebook, or update the dataset path accordingly.
5. Open `AeroHealth_RUL_Prediction_Final.ipynb` in Jupyter Notebook or Google Colab.
6. Execute the notebook cells in order to preprocess the data, train the models and evaluate their performance.

## Limitations

- Experiments use the simulated NASA C-MAPSS FD001 dataset.
- Results on simulated data do not establish performance on real-world aircraft engines.
- Performance may vary across random seeds and experimental settings.
- Further validation on additional datasets and real-world maintenance data would be required before practical deployment.

## Repository Contents

- `AeroHealth_RUL_Prediction_Final.ipynb` — Model development, training and evaluation.
- `AEROHEALTH FINAL REPORT.pdf` — Project report.
- `aerohealth_figures.zip` — Project figures.
- `README.md` — Project documentation.

## Author

**Soumik Sarkar**  
B.Tech, Computer Science and Engineering  
Jorhat Engineering College

---

*Academic machine learning project focused on predictive maintenance and turbofan engine health estimation.*
