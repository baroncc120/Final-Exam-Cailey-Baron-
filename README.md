# Final-Exam-Cailey-Baron-

For this final exam, we were tasked with choosing our own data set, and then making a dashboard and completing analysis on 5 different variables across at least 3 kinds of statistical models. This assignment requires completing the full data analysis process: data preprocessing, creating and interpreting visualizations, and predictive modeling. The goal is to move from raw data to meaningful insights by cleaning the data, exploring important relationships, and building models that can generate predictions from patterns.

For this project, I selected a publicly available dataset of worldwide UFO sightings containing over 88,000 observations. The data include both categorical and numerical variables such as reported location, event date, description, latitude/longitude, time of day, and reported duration of the sighting. Because the dataset required several cleaning steps including handling missing values, recoding variables, and merging geographic information to create useful maps, it satisfies the requirements for data cleaning and also provides us with interesting information that otherwise would not have been known.

![alt text](<https://github.com/baroncc120/Final-Exam-Cailey-Baron-/blob/main/ufo_dashboard.png>)

In this analysis, I focus on predicting the duration of UFO sightings using predictors like year, season, latitude, longitude, and time of day. Through dashboards and performance comparisons across multiple statistical models, I investigate whether these factors help us to explain how long UFO sightings last. This project also evaluates which predictive methods perform best and what these predictions tell us about UFO reports.

The question that I aim to answer through this project is as follows: Can we predict how long a UFO sighting lasts based on when and where it happens?

![alt text](<https://github.com/baroncc120/Final-Exam-Cailey-Baron-/blob/main/analysis_dashboard.png>)

Across all five predictive models, the Random Forest model with 400 trees (RF4) performed the best overall. It produced the highest R2, capturing more variation in UFO sighting duration than other approaches while also maintaining competitive RMSE and MAE values in comparison. This suggests that relationships between the predictors and duration are nonlinear, so multiple decision trees helps detect the patterns that linear regression or a single decision tree wouldn't be able to.

Even the best model still explains a very small portion of the variance in duration_seconds. The low R2 across all models indicates that spatial and temporal variables alone are not strong predictors of how long a UFO sighting lasts. The duration of a report likely reflects human memory instead of structured geographic or temporal patterns.

The analysis shows that predicting how long a UFO sighting lasts is highly uncertain using only the available spatial and temporal information. Still, the Random Forest model demonstrates that there are faint patterns that can be detected, suggesting that some external variables influence sighting duration.

Future work that incorporates features like the sighting’s visual description, movement, or even sentiment within the report may lead to more reliable model performance. These predictions should be thought of as pattern detection, not precise data.

Here are some brief explanations behind why I chose to run the models that I did. 

Linear Regression (All Predictors)
Baseline model to assess whether UFO sighting duration can be explained as a combination of geographic and numerical variables. It offers high interpretability and allows comparison of predictor influences.

Linear Regression (Subset)
Tests whether a simpler specification can achieve similar accuracy and improve the model. This also fulfills the requirement of training a model that does not use all predictors.

Regression Tree (rpart)
A tree-based model allows nonlinear relationships and interaction effects across predictors. This model is included to satisfy the requirement for a tree-based method and provides visual interpretability into how different variables split duration outcomes.

Random Forest (200 & 400 Trees)
Random forest generally improves prediction accuracy and stability over a single tree. By testing two forest sizes (200 and 400 trees), I evaluated how increasing the number of trees influences model performance. Random forests capture complex variable interactions, making them strong options for the final model.
