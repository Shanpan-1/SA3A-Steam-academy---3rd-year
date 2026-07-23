# Predicting Annual Income Using U.S. Census Data

--Summary--

We built a machine learning model that predicts whether a person earns more than $50,000 per year using demographic and employment information from the U.S. Census dataset.

--Problem--

Income is affected by factors like education, work experience, and hours worked each week. Understanding these relationships can help researchers and policymakers identify economic patterns and opportunities. However, it is important to make sure machine learning models do not unfairly treat different groups of people.

--Data--

We used the UCI Adult Census Income Dataset, which contains information collected from the 1994 U.S. Census. The dataset includes variables such as age, workclass, education, education level, marital status, occupation, relationship, race, sex, capital gain, capital loss, hours worked per week, native country, and income. The original dataset contained 32,561 rows and 15 columns. After removing rows with missing values marked by "?", about 26,900 rows remained for analysis.

During exploratory data analysis (EDA), we found that education level, hours worked per week, and capital gain were strongly related to whether a person earned more than $50,000 per year. We also discovered that missing values were hidden as "?" instead of blank cells, so we had to clean the data before building our model.

--Pocudure--

Our goal was to predict whether a person's income was above or below $50,000 per year. We cleaned the dataset, converted the income values into a binary target, selected important features such as age, education level, hours worked, capital gain, capital loss, and sex, and split the data into training and testing sets. We trained a Logistic Regression model because it is a simple and effective model for binary classification. We evaluated the model using accuracy, precision, recall, and a fairness comparison between demographic groups.

--What I found--

Our model performed well overall, with an accuracy of about 81% on the test data. The chart that best explains our results is the confusion matrix, which shows how many people were correctly and incorrectly classified into the two income groups. It demonstrates that the model correctly predicted most cases while still making some mistakes, especially for higher-income individuals.

--Fairness Check--

We compared the model's performance between male and female participants. The model achieved about 77.3% accuracy for males and 88.7% accuracy for females. However, recall for predicting incomes above $50,000 was similar but slightly different (42.3% for males and 37.8% for females). These differences suggest the model may not perform equally for every demographic group, likely because of historical differences and imbalances in the Census data.

--Limits & What's Next--

One limitation of this project is that the dataset comes from the 1994 U.S. Census, so it does not represent today's economy. The model can only identify patterns in historical data and cannot explain why someone earns a certain income.

--How to Run--

Google Colab Notebook: https://colab.research.google.com/drive/10rJDaEyik4ue2Yae3PpZJKI5mYCOJFkT?usp=sharing
Files Needed: No additional files are required because the notebook downloads the Adult Census Income dataset directly from the UCI Machine Learning Repository.
Runtime: Approximately 1–5 minutes from start to finish.
