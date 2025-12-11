# Customer Churn Prediction 
by Ethan Huffman 12\11\2025
# Business Problem
### SyriaTel has been losing customers, and replacing them costs more than keeping the ones they already have. The company needs a way to spot which customers are most likely to leave so the retention team can reach out early. The goal of this project is to build a model that predicts churn and focuses on recall, since missing a customer who leaves is more costly than contacting someone who ends up staying.
# Data Understanding
### The dataset comes from Kaggle and includes customer account details, calling behavior, and service usage. I explored the data to see how many customers churn, what features are available, and whether anything needed cleaning. The churn rate was imbalanced, so understanding this early helped guide the modeling choices later.
# Data Preparation 
### I cleaned the data by converting the churn column into numbers and removing ID-style columns that don’t help with prediction. Then I split the data into training, validation, and test sets. I used a pipeline to handle missing values, scale numeric features, and encode categorical ones so the models could learn from the data more reliably.
# Modeling
### I started with a logistic regression model as a baseline to understand simple patterns and see how well a basic model performs. After that, I trained a decision tree to capture more complex relationships in the data. Finally, I tuned the tree using GridSearch to improve recall and reduce mistakes on churners. The tuned tree became the final model because it identified the most true churners without letting too many false alarms slip through.
# Evaluation 
### I tested the final model on a separate holdout set to make sure the results were fair and unbiased. Since the main goal was recall, I focused on how many churners the model successfully caught. The final model performed the best by catching most churners while still keeping incorrect predictions low. This balance matters because missing a churner can cost the company money.
# Deployment
### I used the final model to create a ranked list of customers who are most likely to churn so the retention team can contact them first. I also looked at which features were most important, such as customer service calls and total charges, which can guide teams on changes to improve the customer experience. Finally, I identified high-value customers who are also at risk, giving the marketing team a target group for special offers.
