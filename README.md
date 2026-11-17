# Prodigy InfoTech - Machine Learning Internship

## Task 01: House Price Prediction

### 📌 Objective
Implement a Linear Regression model to predict the prices of houses based on their square footage (`GrLivArea`), number of bedrooms (`BedroomAbvGr`), and number of bathrooms (`FullBath`).

### 📊 Dataset
The dataset used is the [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data) dataset from Kaggle.

### 🛠️ Tools & Technologies
*   **Python**
*   **Google Colab / Jupyter Notebook**
*   **Pandas & NumPy** (Data Manipulation)
*   **Scikit-Learn** (Machine Learning)
*   **Matplotlib** (Data Visualization)

### 🧠 Approach & Model Enhancement
While the core task required using only three features, I decided to experiment and enhance the model to see how it impacts the accuracy:
1.  **Base Features:** Square footage, Bedrooms, and Bathrooms.
2.  **Added Features:** I included `OverallQual` (rates the overall material and finish of the house) and `TotalBsmtSF` (total square feet of the basement) as they are highly correlated with house prices.
3.  **Log Transformation:** I applied a logarithmic transformation (`np.log1p`) to the target variable (`SalePrice`). This normalizes the distribution of house prices, making the Linear Regression model perform significantly better.

### ⚙️ How the Code Works
1.  **Data Loading:** Reads the `train.csv` file.
2.  **Feature Selection:** Selects the 5 relevant columns for `X` and applies `np.log1p` to `y`.
3.  **Train/Test Split:** Splits the data into 80% training and 20% testing sets.
4.  **Model Training:** Fits a `LinearRegression()` model using Scikit-Learn.
5.  **Evaluation:** Calculates and prints the R-squared (\(R^2\)) score to evaluate accuracy.
6.  **Visualization:** Plots a scatter graph comparing Actual vs. Predicted prices.
7.  **Interactive Prediction:** The script includes an interactive block that asks the user to input values for square footage, bedrooms, bathrooms, quality, and basement size, and outputs the estimated house price using `np.expm1` to reverse the log transformation.

### 📈 Results
*   **Base Model (3 features):** Achieved an R-squared score of approximately 0.63.
*   **Enhanced Model (5 features + Log Transform):** Achieved an R-squared score of **~0.84** 

### 🚀 How to Run
1. Open the `.ipynb` file in Google Colab.
2. Ensure you have uploaded the `train.csv` dataset to the Colab environment.
3. Run all the code cells.
