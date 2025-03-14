# task_imagoAI_python
# Hyperspectral Imaging Data Analysis for DON Prediction

## Project Overview

This project aims to predict mycotoxin levels (DON concentration) in corn samples using hyperspectral imaging data. The dataset contains spectral reflectance values across multiple wavelength bands, and the target variable is **`vomitoxin_ppb`** (representing DON concentration).

## Objective

- Preprocess the hyperspectral imaging data.
- Perform data visualization and dimensionality reduction using PCA.
- Train and evaluate regression models (including Random Forest and XGBoost) for DON concentration prediction.
- Optimize model performance using GridSearchCV.

## Dataset Description

- **Features:** Spectral reflectance values across multiple wavelength bands.
- **Target Variable:** `vomitoxin_ppb` (DON concentration in ppb).

## Steps Followed

### 1. Data Exploration and Preprocessing

- Identified and confirmed no missing values in the dataset.
- Performed visualization of selected spectral bands to understand data trends.
- Applied IQR method for outlier detection and capped extreme values at upper and lower bounds.
- Normalized the dataset using `StandardScaler` to ensure consistent feature scaling.

### 2. Dimensionality Reduction

- Applied **PCA** to reduce dimensionality to 4 components.
- Visualized the first two principal components to observe data distribution.

### 3. Model Training

- Split the dataset into 80% training and 20% testing data.
- Implemented and evaluated two models:
  - **Random Forest Regressor** (MAE: 2412.1256, RMSE: 6853.0178, R²: 0.8320)

### 4. Model Evaluation

- Evaluated the model's performance using:
  - **Mean Absolute Error (MAE)**
  - **Root Mean Squared Error (RMSE)**
  - **R² Score**
- Created a scatter plot to compare actual vs predicted DON concentrations.

## Key Results

- The Random Forest model achieved an R² score of **0.8320**.
- The XGBoost model, after hyperparameter tuning, outperformed the Random Forest model with improved metrics.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository-link>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Python script:
   ```bash
   python hyperspectral_ml.py
   ```

## Dependencies

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`

## Future Improvements

- Implementing a transformer model with attention mechanisms to capture complex patterns in the spectral data.
- Developing a Streamlit app for interactive DON concentration predictions from user-uploaded spectral data.

