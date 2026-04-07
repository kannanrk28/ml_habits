Problem Statement
You are a junior data analyst at a retail company. Your manager hands you a dataset of past customer orders and asks you to build a model that predicts whether a customer will make a repeat purchase within 30 days.

Task 1
Identify which column in the dataset is the label, and which column, if included as a feature, would introduce data leakage. For each, write one sentence justifying your choice.

Label : Based on the column list is provided, found label as "repeat_purchase_flag" and type is "Classification" since the business model for ML built whether customer can purchase within 30 days frequently 

Leakage : "discount_used_on_repeat_order" if we consider as feature, then it should be data leakage. Discount will not be applicable for all the customer who purchased. It may discount could be for specific order or promotion of sales. It override our label output and prediction will be wrong

Task 2:
Your manager skips straight to training a gradient boosting model. Suggest two steps from the complete ML workflow that should have been completed first, and briefly explain why each step matters before jumping to a complex model.

Before proceeding with model training, it is critical to complete the foundational stages of the ML pipeline. Skipping these steps often leads to unreliable accuracy and poor feature performance:

Problem Framing: We must first determine if a machine learning model is the right solution for this business use case. If it is, we need to define whether the problem requires a Classification or Regression approach.

Exploratory Data Analysis (EDA) & Pre-processing: We must conduct EDA to understand data distributions and detect outliers. Additionally, thorough data cleaning—handling null values and preventing data leakage—is essential.

Conclusion: Without these preliminary steps, the features will not have the predictive power necessary to ensure model accuracy.