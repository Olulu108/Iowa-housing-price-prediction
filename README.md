# Iowa Housing Price Prediction 🏡

This project uses machine learning to predict housing prices based on the Ames, Iowa housing dataset. The goal is to build a regression model that accurately estimates the final sale price of a house.

---

## ⚙️ Project Workflow

1. **Data Loading:** The Iowa_housing_prices.csv dataset is loaded using pandas.

2. **Data Cleaning:** Columns with missing values (NA) were initially dropped to create a baseline dataset.

3. **Feature Selection:**

    * An initial model was built using all available features after cleaning.

    * A second, more focused model was built using a subset of features: LotArea, LotConfig, LotShape, MSZoning, BldgType, Neighborhood, and GarageCars.

4. **Preprocessing:**

    * The data was split into training and testing sets.
  
    * Numeric features were scaled using StandardScaler.

    * Categorical features were encoded using OneHotEncoder.

5. **Modeling:** Two regression models were trained and evaluated:

    * Linear Regression

    * Random Forest Regressor

6. **Evaluation:** Models were evaluated based on Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R²) metrics.

---

## 🤖 Models & Results
The project tested two different models. The Random Forest Regressor showed a better performance on the selected features compared to the Linear Regression model.

**Initial Model (All Features)**

* **Model:** Linear Regression

* **Mean Absolute Error (MAE): $21,536.86**

**Second Model (Selected Features)**

This iteration focused on a smaller set of features to see if performance could be improved.

**Linear Regression**

* **Mean Absolute Error (MAE): $32,965.99**

* **Root Mean Squared Error (RMSE): $48,947.69**

* **R-squared (R²): 0.65**

**Random Forest Regressor**

* **Mean Absolute Error (MAE): $31,199.09**

* **Root Mean Squared Error (RMSE): $46,188.55**

* **R-squared (R²): 0.69**


The key takeaway is the importance of feature selection and model choice. While the initial linear model with all features had a lower MAE, the Random Forest model provided a better R² value on a more curated feature set.

## 🚀 How to Run This Project

To replicate this analysis, you will need Python and the following libraries. You can run the code in an environment like Jupyter Notebook or Google Colab.

1.  **Install the required libraries:**
    ```bash
    pip install pandas numpy scikit-learn
    ```

2.  **Download the Dataset:**
    Ensure you have the `Iowa_housing_prices.csv` file in your project directory.

3.  **Run the Notebook:**
    Execute the cells in the notebook sequentially to see the full analysis.
