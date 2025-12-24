# SONAR Rock vs. Mine Prediction

## Project Overview
This project uses **Sonar data** to predict whether an underwater object is a **Rock (R)** or a **Mine (M)**. The data consists of sonar signals bounced back from metal cylinders (mines) and rocks at various angles and under different conditions.

The core objective is to build a binary classification model that helps submarines navigate safely by identifying potential explosives.

### Workflow
1. **Data Collection:** Sourced sonar data (60 features representing sound frequencies). 
2. **Data Pre-processing:** Loading data into Pandas DataFrames and handling header-less CSV files. 
3. **Statistical Analysis:** Using `.describe()` and `.groupby()` to understand feature distributions for Rocks vs. Mines.
4. **Train-Test Split:** Dividing the dataset into training (90%) and testing (10%) sets using `stratify` to maintain class balance.
5. **Model Training:** Implementing a **Logistic Regression** model (ideal for binary classification). 
6. **Evaluation:** Assessing accuracy scores on both training and test data. 
7. **Predictive System:** Building a pipeline to input new sonar data and output a human-readable prediction ("The object is a Rock" or "The object is a Mine"). 

### Tech Stack
- **Languages:** Python
- **Libraries:** NumPy, Pandas, Scikit-learn
- **Environment:** Google Colab

### Results
- **Training Accuracy:** ~83.4%
- **Test Accuracy:** ~76.2%
*Note: Results may vary slightly depending on the random state.*

### Dataset
The dataset contains **208 instances** with **60 features** each.
- **M:** Represents a Metal Cylinder (Mine)
- **R:** Represents a Rock

### How to Run
1. Upload the `sonar data.csv` to your Google Colab environment. 
2. Run the cells in the provided notebook.
3. Use the "Predictive System" section to input new data points for real-time prediction.

---

## Future Ideas to Implement

1. **Implement Diverse ML Models:** Compare Logistic Regression with Support Vector Machine (SVM), Random forest classifier, k-Nearest neighbours, XGBoost etc.
2. **Comparison Metrics:** Calculate the F1 sscore and explore the balance between Recall and Precision. Also plot the ROC-AUC Curve to visualize the model's ability to distinguish between classes.
3. **Hyperparameter tuning:** Use GridSearchCV or RandomizedSearchCV to find the best parameters for your SVM (C and Gamma values) or Random Forest (number of trees, max depth).
4. **User interface development:** Integrate a Streamlit app where a user can upload a CSV of sonar readings or manually input values to get instant visual feedback.
