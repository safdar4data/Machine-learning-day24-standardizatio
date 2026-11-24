Machine Learning: Feature Standardization
Project Overview
This project demonstrates feature standardization in a
machine-learning workflow using the Social_Network_Ads.csv dataset. It
explores how scaling numerical features such as Age and
EstimatedSalary changes their scale and how standardization can affect
model performance.
Trainer
- Name: Md Safdar
- Designation: Senior Trainer -- Data Analyst
- Institute: Intensive Institute, New Delhi
- Mobile: 9810845947
- Email: safdar.ncpul@gmail.com
Objectives
- Load and inspect the Social Network Ads dataset.
- Separate the input features and target variable.
- Split the data into training and testing sets.
- Apply StandardScaler to standardize numerical features.
- Compare feature distributions before and after scaling.
- Compare Logistic Regression and Decision Tree classification
  accuracy with and without scaling.
- Explore the effect of outliers on feature values.
Dataset
The notebook reads a file named Social_Network_Ads.csv.

The notebook removes the first two columns using df.iloc[:, 2:] and
uses: - Input features: Age, EstimatedSalary - Target:
Purchased

Place Social_Network_Ads.csv in the same working directory as the
notebook, or update the file path in the pd.read_csv() statement.
Technologies and Libraries
- Python
- Jupyter Notebook
- NumPy
- pandas
- Matplotlib
- Seaborn
- scikit-learn
Workflow
1. Import the required Python libraries.
2. Load the dataset with pandas.
3. Select the feature columns and target column.
4. Split the dataset using train_test_split with test_size=0.3 and
   random_state=0.
5. Fit StandardScaler on the training features only.
6. Transform both training and test features using the fitted scaler.
7. Convert the scaled arrays back into pandas DataFrames.
8. Compare descriptive statistics and visualizations before and after
   scaling.
9. Train Logistic Regression and Decision Tree Classifier models on
   original and scaled features.
10. Compare predictions using accuracy_score.
11. Inspect feature values and visualizations when considering outliers.
Standardization
StandardScaler transforms a feature using:
z = (x - mean) / standard_deviation
The scaler is fitted on X_train and then used to transform both
X_train and X_test. This avoids calculating scaling parameters from
the test set.
Models Compared
- LogisticRegression
- DecisionTreeClassifier
The notebook compares accuracy for each model using the original
features and standardized features. Actual accuracy values depend on the
dataset and the execution environment; run the notebook to obtain them.
How to Run
1. Install Python and Jupyter Notebook, or use Google Colab.
2. Keep Machine_learning_day24_standardization.ipynb and
   Social_Network_Ads.csv in the same folder (or upload both to
   Colab).
3. Install the required libraries if they are not already available:
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
4. Open the notebook and run the cells in order.
Key Learning Points
- Standardization changes the scale of numerical features; it does not
  make the original data distribution automatically normal.
- Fit preprocessing steps on training data, then apply the same fitted
  transformation to test data.
- Scaling can be important for distance-based and gradient-based
  methods and may affect Logistic Regression.
- Decision Trees are generally not dependent on feature scaling, so
  their results may remain similar.
- Outliers can influence the mean and standard deviation used by
  standardization.
Project Files
- Machine_learning_day24_standardization.ipynb --- notebook
  containing the analysis and model comparison.
- Social_Network_Ads.csv --- input dataset required to run the
  notebook.
- README.md --- project description and instructions.
Author
Md Safdar
Senior Trainer -- Data Analyst
Intensive Institute, New Delhi
Mobile: 9810845947
Email: safdar.ncpul@gmail.com
