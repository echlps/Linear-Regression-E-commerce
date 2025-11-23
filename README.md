# Linear-Regression-E-commerce

This project explores an e-commerce dataset in order to understand **which behaviours drive customers to spend more** and builds a **linear regression model** to predict customer value. In this analysis I compared the impact of mobile app usage, website usage, and customer membership length on annual revenue.
---
## Dataset
[Kaggle](https://www.kaggle.com/datasets/kolawale/focusing-on-mobile-app-or-website/data): *Focusing on Mobile App or Website?*
The dataset consists of behavior metrics such as: 
* Avg. Session Length
* Time on App
* Time on Website
* Length of Membership
* Yearly Amount Spent (target)

## Project objectives
- Perform **exploratory data analysis (EDA)**
- Visualize relationships between features
- Build a **linear regression model**
- Evaluate model performance
- Determine which user behaviors most influence customer spending
- Provide **business insights**

## Exploratory Data Analysis
Key steps in EDA:
- Pairplot to visualize all feature relationships
- Jointplots (scatter + regression line)  
- Distribution of residuals  
- Q–Q plot to check normality


### **Main EDA Findings**
- **Length of Membership** has the strongest correlation with yearly spending  
- **Time on App** has a moderate positive correlation  
- **Time on Website** shows almost no relationship  
- Feature distributions are clean with no major outliers

## Model and Coefficients
* A linear regression model was trained using scikit-learn. The model coefficients help identify feature influence.

| Feature                | Coefficient |
|------------------------|-------------|
| Avg. Session Length    | 25.72       |
| Time on App            | 38.60       |
| Time on Website        | 0.46        |
| Length of Membership   | 61.67       |

Interpretation:
* Length of Membership has the strongest positive impact on yearly spending.
* Time on App also contributes positively.
* Avg.Session Length has a moderate effect.
* Time on Website has almost no influence on spending.

### Model Evaluation
Metrics:
* **MAE:** ≈ 8.4
* **RMSE:** ≈ 10.2
* Model's predictions are typically within **8-10$** range of the true yearly spending


### Visual evaluation
* Residual Histogram:
  ![Residual Histogram](https://github.com/echlps/Linear-Regression-E-commerce/blob/main/Reg/images/imagesresiduals.png?raw=true)
  * Shows the distribution of model errors. The residuals are centered around zero and form a roughly normal distribution, indicating that the model’s errors are random and not biased.
* Q-Q Plot:             
  ![Q-Q Plot](https://github.com/echlps/Linear-Regression-E-commerce/blob/main/Reg/images/Q-Q_Plot.png?raw=true)   
  * Compares the residual distribution to a perfect normal distribution. Points follow the line closely, confirming that the residuals are approximately normal.
 * Predictions vs Actual values plot:
  ![Predicted Vs Actuial](https://github.com/echlps/Linear-Regression-E-commerce/blob/main/Reg/images/PredictedVsActualPlot.png?raw=true)
    * Plots predicted values against true values. Points fall close to the diagonal line, showing that the model makes accurate predictions with no strong patterns in the errors.

### Conclusions and insights 
* Membership Length has the strongest impact on spending
* App usage correlates positively with revenue
* Website usage has little predictive value
* The model performs strongly and generalizes well

Focus on improving the mobile app experience.
Invest in customer retention strategies (longer membership = more revenue).
Website improvements have low expected financial return.
