**Project By: Amantle Michelle Makati**

**Date of Completion: 11 March 2026**

# Alpha-Dreamers-Predictive-Credit-Risk-Modeling

📌 Project Objective
The objective of this project was to develop a robust machine learning model to identify high-risk loan applicants. By leveraging Logistic Regression, this system serves as a critical filter for financial institutions, allowing them to proactively mitigate defaults by analyzing geographic, demographic, and financial risk drivers.

🛠 Technical Stack
* Environment: Google Colab / Jupyter Notebook
* Language: Python
* Libraries: * Data Handling: Pandas, NumPy, Catergory Encoders
             * Visualization: Matplotlib, Seaborn
* Machine Learning: Scikit-Learn

🚀 Machine Learning Pipeline
1. Data Preparation & Cleaning
* Initial Exploration: Loaded CSEdata.csv to analyze data structures and feature distributions.

* Data Sanitization: Handled missing values and removed duplicates.

* Text Processing: Cleaned categorical strings (e.g., removing text incosistencies like [10] from city names) to ensure data consistency across the dataset.

2. Experimental Design
*Train-Test Split: Divided data into an 80% Training set and a 20% Testing set.

* Leakage Prevention: Strict separation was maintained; the model remained entirely "blind" to the test set during the training phase to ensure unbiased evaluation.

3. Data Preprocessing (The Engine Room)
To prepare the data for the Logistic Regression model, we performed:

* Binary Mapping: Converted "Yes/No" flags to 1 and 0.

* One-Hot Encoding: Applied to features like House_Ownership.

* Target Encoding: Used for high-cardinality features (City, Profession, State) to represent categories by their mean risk scores.

* Feature Scaling: Utilized StandardScaler to normalize numerical values (like Income vs. Age), ensuring no feature disproportionately influenced the model due to its scale.

4. Model Training & Evaluation
* Addressing Class Imbalance: Since "Safe" applicants outnumbered "Risk" applicants, we utilized the class_weight='balanced' parameter to ensure the model prioritized learning high-risk patterns.

* Exploratory Data Analysis (EDA): Visualized key trends, such as the relationship between job tenure and default probability.

*Evaluation Metrics: The model was evaluated on the unseen test set using:

>Accuracy
>Precision
>Recall (Focusing on capturing as many defaults as possible)
>F1-Score
>Confusion Matrix (shows where the Logistic Regression model succeeded and where it got confused)

📈 Key Findings
*Geography Matters: Regional economic trends (City/State) were among the strongest predictors of default.

*The Stability Factor: Professional longevity and job tenure showed significant non-linear correlations with repayment behavior.

**How to Run**
->Clone this repository.
->Ensure you have the required libraries installed: pip install pandas numpy matplotlib seaborn scikit-learn category encoders
->Open the notebook in Google Colab or Jupyter, copy the path of the CSEdata.csv and paste it on the orig_df=pd.read_csv(' **insert path here** ') again and run all cells.
