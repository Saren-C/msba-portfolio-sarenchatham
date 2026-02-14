# Individual Contribution

## What did you personally contribute to the most?
I contributed most heavily to the model development and interpretation process. This involved testing XGBoost under various conditions, specifically focusing on handling class imbalance using SMOTE versus cost-sensitive learning (weighted loss). We didn't end up using any of the models I created, but it was good the have them for comparison. I also worked on hyperparameter tuning to optimize performance. I managed the model interpretation using SHAP values and feature importance to identify the key drivers of churn. By analyzing the relationships between these top features, I was able to uncover data patterns that directly informed our customer clustering and final business recommendations.

## What is one decision or approach you personally advocated for and why?
I advocated for us to use PR-AUC as one of our evaluation metrics. Churners accounted for a small percentage of the data, and PR-AUC is a better metric for imbalanced data because it focuses on the minority class. I also advocated for keeping our customer segments to three clusters instead of four. Even though the math could have supported four, it felt too cluttered. By sticking to three and including features like Average GB Download, the reasons for customer churn became much clearer and easier to create recommendations for.

## Lessons Learned
The biggest thing I learned is that a high scoring model isn't useful if you can't turn it into a strategy. The most important thing is being able to connect the data insights with actionable business recommendations.

If I had more time, I would have conducted more extensive hyperparameter tuning to see if I could increase the performance of our model at all. I also would’ve liked to look even deeper into how all the features interact with each other. I only had time to look at relationships between the most important features but I would have liked to look at more to see if any hidden or surprising relationships emerged.


