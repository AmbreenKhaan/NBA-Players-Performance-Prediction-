# NBA Player Performance Prediction

This project predicts NBA player performance using historical data, focusing on the prediction of points scored per game. Two machine learning models, **Linear Regression** and **Ridge Regression**, are implemented to compare their performance.

## **Project Overview**

### **Goal:**
To predict player performance (specifically points scored per game) based on various player statistics such as assists, rebounds, usage percentage, and more.

### **Models Used:**
- **Linear Regression**: A simple and interpretable model.
- **Ridge Regression**: A regularized version of linear regression that helps prevent overfitting.

---

## **Steps Involved**

### 1. **Data Loading & Exploration**

- **Data Loading**: The dataset `all_seasons.csv` is loaded using Pandas.
- **Data Inspection**: The first and last few rows of the data are displayed, and an overview of the dataset's columns and data types is generated.
- **Missing Values**: Checks for missing data and performs necessary cleaning (e.g., replacing or dropping missing values).

### 2. **Data Preprocessing**

- **Feature Engineering**: New features like rolling averages are generated to capture trends in player performance.
- **Feature Transformation**: Some categorical variables are converted to numerical values.
- **Data Scaling**: Numerical features are scaled using **StandardScaler** to ensure all features have the same scale.

### 3. **Exploratory Data Analysis (EDA)**

- **Visualizations**: Distribution of key metrics (points, assists, rebounds, etc.) is visualized using histograms and pairplots.
- **Correlation Analysis**: The correlation between different variables and the target variable (points scored) is analyzed using a heatmap.

### 4. **Feature Selection**

- Features are selected based on their correlation with the target variable (`pts` for points).
- **Feature Importance**: Features with a correlation greater than 0.2 or less than -0.1 with the target are selected for modeling.

### 5. **Model Training & Evaluation**

- **Train-Test Split**: The dataset is split into training and testing sets.
- **Model Training**: Both **Linear Regression** and **Ridge Regression** models are trained on the training set.
- **Evaluation Metrics**: The models are evaluated using **R²**, **Mean Absolute Error (MAE)**, and **Mean Squared Error (MSE)**.

### 6. **Results and Conclusion**

- **Model Comparison**: The performance of both models is compared, and it is concluded that both models perform similarly. **Linear Regression** is chosen due to its simplicity and effectiveness.

### 7. **Feature Analysis**

- **Important Features**: Key features influencing player performance are discussed, including `pts`, `ast`, `usg_pct`, and `ts_pct`.
  
---
### Prerequisites:
- Python 3.8+
Before running the code, ensure you have the following libraries installed:
- `pandas` (for data handling)
- `numpy` (for numerical operations)
- `scikit-learn` (for machine learning models and evaluation)
- `matplotlib` and `seaborn` (for data visualization)
- `sklearn` (for model training and metrics)
## **How to Use**

1. **Clone this repository** or download the project files.
2. **Install dependencies**: Ensure you have the required libraries installed.
3. **Run the Jupyter notebook** (`nba_player_performance_prediction.ipynb`) to replicate the analysis. The notebook contains all steps, including data preprocessing, model training, and evaluation.

---

## **Key Files**
- `nba_player_performance_prediction.ipynb`: Jupyter notebook containing the full code for the analysis.
- `all_seasons.csv`: The dataset used for prediction (ensure it's in the same directory as the notebook).


## **Results Summary**

The performance of **Linear Regression** and **Ridge Regression** is nearly identical. Both models exhibit similar values for **R²**, **Mean Squared Error (MSE)**, and **Mean Absolute Error (MAE)**. This suggests that **Linear Regression** is a simpler and equally effective choice for predicting player performance.

**Important Features**:
- **'pts' (Points)**: The most significant feature, directly indicating player performance.
- **'ast' (Assists)**: A key indicator of a player's playmaking ability, which positively impacts performance.
- **'usg_pct' (Usage Percentage)**: Higher usage percentage indicates a player's involvement in offensive plays.
- **'ts_pct' (True Shooting Percentage)**: Players with higher shooting efficiency tend to score more, making this an important predictor.

### **Conclusion**

Both **Linear Regression** and **Ridge Regression** perform similarly for predicting player performance, with **Linear Regression** being the preferred model due to its simplicity and interpretability.

---

