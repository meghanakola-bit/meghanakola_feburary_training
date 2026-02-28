Loan Prediction Project
conclusion:
1. Missing Value Handling
During preprocessing, missing values in numerical features were handled using median imputation, while categorical features were filled using mode imputation.
Median performed better than mean because the dataset contained skewed features such as ApplicantIncome and LoanAmount. Median is more robust to outliers and does not get affected by extreme values. Mode was appropriate for categorical variables since it preserves the most frequent category.
Therefore, median and mode imputation were selected as the final missing value handling techniques.

2.Categorical Encoding Techniques
Multiple encoding techniques were implemented including:
Label Encoding
One-Hot Encoding
Ordinal Encoding
Frequency Encoding
Target Encoding
Label Encoding worked well for binary variables such as Loan_Status.
One-Hot Encoding was suitable for nominal features like Gender where no order exists.
Ordinal Encoding was effective for ordered features such as Education.
Frequency and Target Encoding were useful for capturing category importance in features with multiple levels.
Among these, One-Hot Encoding and Target Encoding provided better representation of categorical variables without introducing misleading order relationships.

3. Feature Scaling Analysis
Four feature scaling methods were applied:
Min-Max Scaling
Max Absolute Scaling
Vector Normalization
Z-Score Standardization
Z-Score Standardization (StandardScaler) was found to be most effective because it centers the data around mean 0 with standard deviation 1. This improves model convergence and ensures fair contribution of all features.
finally i conclude that , StandardScaler was selected for final modeling.

4. Outlier Treatment and Skewness Transformation
Outliers were detected using the IQR method and treated accordingly.
Highly skewed features such as LoanAmount and ApplicantIncome were transformed using log transformation.
Log transformation reduced right skewness and improved distribution symmetry, which enhanced model stability and performance.

5. Final Preprocessing Decisions
Based on analysis:
Median and Mode imputation were chosen for missing values.
One-Hot and Target Encoding were most effective for categorical features.
Z-Score Standardization was selected as the final scaling method.
Log transformation improved skewed distributions.
Outliers were treated to reduce extreme influence.
These preprocessing steps ensured clean, consistent, and well structured data for reliable model training and prediction.
