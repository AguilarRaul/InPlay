# Classification model predicting Ball In Play probability ⚾️

### Q1 In Play deployment data predictions

Plase refer to InPlay.ipynb notebook and results.csv file for modeling approach and results.

### Q2: Modeling approach reasoning

The solution process began with an exploratory analysis to identify the proportion of positive labels and selecting the appropriate metric to train the models, in addition to having a glimpse of the features' distributions and their correlations with the target variable. Subsequently, I standardized the features to mitigate the impact of varying magnitudes before proceeding with the training of both linear and non-linear models. Upon reviewing the results table from the modeling phase, it became apparent that both logistic regression and the light gradient boosting classifier exhibited similar performance. However, there was a concern about overfitting in the case of the light gradient boosting classifier (LGBM). To address this issue, I conducted hyperparameter optimization. Following this optimization and the plotting of precision-recall curves, it was evident that the LGBM's performance improved. Given the importance of interpretability in our problem, I ultimately chose the logistic regression model as the best option. It's worth noting that while tools like SHAP (SHapley Additive exPlanations) can aid in interpreting non-linear models, the coefficients of linear models offer a straightforward and direct interpretation, aligning with the interpretability requirement of Q3.

### Q3: How variables affect the batter’s ability to put the ball in play

Considering that all variables are independent. If the amount of movement the pitch had in the horizontal direction increases, there is a higher probability of the batter putting the ball in play. Whereas an increase in either the velocity of the pitch release, the spin rate or the amount of movement the pitch had in the vertical direction causes a lower probability of the batter putting the ball in play.

### Q4: Next steps

I would love to spend more time in experimenting with non-linear models and fine-tuning their performance, with the aim of identifying a superior performer in contrast to Logistic Regression, since the features in real life may not be not independent, and also trying to incorporate more data sources (for example context-dependent data). Furthermore, I would explore model interpretability techniques to provide actionable insights for the pitcher and the coaching staff, helping them optimize their pitching strategy based on these factors.
