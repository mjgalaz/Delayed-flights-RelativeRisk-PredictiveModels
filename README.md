# USA Domestic Flights Analysis Project (January 2023)
This project focuses on the analysis of domestic flight data in the United States during January 2023. Through exploratory data analysis and predictive modeling, we aim to identify the causes of flight delays and propose improvements for the United States Department of Transportation (DOT).
Conducted in pairs, this project capitalized on the combined expertise of each team member, fostering effective ollaboration and the integration of diverse skill sets.

### Project Summary
The project addresses the following aspects:

- Client: The client for this project is the United States Department of Transportation (DOT).
- Objective: To predict the causes of flight delays and find improvement opportunities through predictive models based on historical data.
- Scope: The analysis focuses on flight data from the contiguous 48 states of the United States, excluding day 11 due to issues with the Air Mission Notification System.

### Methodology
1. Exploratory Data Analysis: 
We used SQL for data handling, including identifying relevant variables and excluding states that affect overall data metrics.
We analyzed correlations between variables, revealing a strong relationship between departure delays (DEP_DELAY) and arrival delays (ARR_DELAY) of flights, with a correlation coefficient of 0.97. Visualizing this relationship in a scatter plot, it became evident that departure delay is a significant predictor of arrival delays, **directing our focus towards predicting departure delays.**

2. Predictive Modeling:
We built a manual prediction model by categorizing departure delay predictor variables and assigning a score to each flight based on relative risk.
We evaluated the model's effectiveness through a confusion matrix in Google Colab using Python.
 In this phase, we utilized various predictive models to analyze flight delay data:
    - Manual Model: We defined predictive categorical variables for delays, calculated relative risk, and assigned scores to flights to define the new variable "NUEVOS RETRASOS" by Pareto cutoff (top 20% of scores defined as Potential Delayed Flights). This allowed us to compare it with the original "RETRASOS" variable.
    - Logistic Regression: We developed logistic regression models using OneHotEncoder to handle categorical predictor variables. For logistic regression, we balanced class samples (many on-time flights, few delayed in the sample) using techniques such as class_weight, SMOTE, Undersampling, and Oversampling.
    - Random Forest Model: We explored Random Forest models using TargetEncoder and Frequency Encoding.
    - Tree Models: Lastly, we applied tree models with balanced samples using SMOTE and class_weigh

3. Results Presentation: In addition to the analysis and modeling, findings were communicated through the creation of a  report and an dashboard in Power BI.

### Conclutions

- The utilization of class_weight in the tree models resulted in a significant improvement in performance, with the latter achieving a 34.9% increase in F1 Score compared to the initial manual model.
- Despite the improved F1 Score, it's important to note that there is still room for improvement in the metrics.
- One potential avenue for further improvement could be the definition of new predictor variables and reassembling models to account for these variables.
- These conclusions highlight both the successes achieved in improving model performance and the ongoing opportunities for refinement and enhancement in future iterations of the analysis.


### Dashboard
![](https://raw.githubusercontent.com/mjgalaz/Delayed-flights-RelativeRisk-PredictiveModels/main/dashboard.png)

