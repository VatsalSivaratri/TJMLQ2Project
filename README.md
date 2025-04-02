#   Flood Probability Classification Project

This project focuses on developing a predictive model for determining the likelihood of a flood (percent chance of an area to flood). The motivation is that flood frequency and severity has been rising due to climate change, and reliable prediction systems can help communities plan and mitigate disasters.

##   Dataset

The dataset used in this project is from a Kaggle competition. It consists of 1.12 million instances and 21 features, all numerical.

Key features include:

* Environmental Factors: Monsoon intensity, watershed count.
* Geographic & Infrastructure: Drainage systems, river management. 
* Human Impact Factors: Urbanization, deforestation.

The target variable is Flood Probability, a continuous value from 0 to 1.

##   How to Run the Code

The main script (`Q2.ipynb`) performs the following steps:

1.  **Data Loading and Preprocessing:**
    * Loads the dataset (`flood_data.csv`).
    * Handles missing values by dropping rows with `NaN` values.
    * Splits the data into training, validation, and test sets.
    * One-hot encodes categorical variables.
    * Scales numerical features using StandardScaler.
2.  **Model Training and Evaluation:**
    * Trains a Deep Neural Network (DNN), Gradient Boosting Machine (GBM), Support Vector Regression (SVR), Bayesian Ridge, Decision Tree, Linear Regression, and Random Forest models.
    * For the DNN, uncertainty is estimated using Monte Carlo Dropout.
    * For GBM and SVR, uncertainty is estimated using bootstrap resampling.
    * Combines the predictions of DNN, GBM, and SVR using uncertainty-weighted averaging.
    * Evaluates the models using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2) score.
    * Generates visualizations to compare model performance.

###   Running the Main Script

To run the main analysis:

1.  Ensure that you have the required Python libraries installed (e.g., `pandas`, `numpy`, `scikit-learn`, `tensorflow`, `lightgbm`).
2.  Place the dataset file (`flood_data.csv`) in the same directory as the `Q2.ipynb` file, or modify the file path in the script.
3.  Run the `Q2.ipynb` script. This will execute the data preprocessing, model training, evaluation, and visualization steps.