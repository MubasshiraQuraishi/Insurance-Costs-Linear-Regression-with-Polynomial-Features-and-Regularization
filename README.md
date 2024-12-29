### **Linear Regression Explanation**
Linear regression is a **supervised machine learning algorithm** where the target variable (dependent variable) depends on one or more independent variables (features). The goal is to predict the target variable using these features.

### **Assumptions of Linear Regression**
1. **Linear Relationship**
2. **No Multicollinearity**
3. **Homoscedasticity**
   
### **Formula of Linear Regression**
The basic formula for linear regression is:
\[
y = mx + c
\]
Where:
- \( y \) is the predicted value (target).
- \( m \) is the slope (the coefficient of the feature \( x \)).
- \( x \) is the feature (independent variable).
- \( c \) is the intercept (the value of \( y \) when \( x = 0 \)).

### **Gradient Descent (Explained Simply)**
- **Gradient Descent**: It's like walking downhill to find the lowest point (minimum error). The process starts with random guesses for the parameters (like the slope and intercept in linear regression). These parameters are updated gradually to minimize the error.
  
- **Cost Function**: This is a measure of how wrong your model's predictions are. For linear regression, it is commonly the Mean Squared Error (MSE). Gradient descent iteratively adjusts the parameters to reduce this error.
  
### **Metrics to Measure Performance**
- **MSE/RMSE/MAE**: Measure how wrong your guesses are (different ways to do it).
- **R²/Adjusted R²**: Show how good your line is at explaining the data.


### **Multicollinearity Check**
Since linear regression assumes **no multicollinearity** (i.e., the independent variables should not be highly correlated), I checked for multicollinearity using **Variance Inflation Factor (VIF)**. A VIF value of 1 indicates no correlation, and values greater than 10 suggest high multicollinearity, which can distort the model. However, since my values were all 1, there were no issues with multicollinearity.

### **Polynomial Features**
If a simple linear model doesn't provide a good fit, we can use **polynomial features** to create a higher-degree relationship between the features and the target. This adds additional features (e.g., squares, cubes of the original features), which can increase the model's accuracy. In my case, using polynomial features improved the performance.

### **Model Accuracy**
- **Baseline Linear Regression**: With the polynomial features, I achieved 82% accuracy on the training set and 86% accuracy on the test set.
  
- **Regularization**:
  - **Ridge Regression**: Regularizes by adding a penalty to the size of the coefficients (slope), preventing them from becoming too large.
  - **Lasso Regression**: Regularizes by adding a penalty that can shrink some coefficients to zero, effectively removing some features from the model.

I used **Lasso regularization**, which improved the model, achieving 82% accuracy on the training set and 87% accuracy on the test set.
