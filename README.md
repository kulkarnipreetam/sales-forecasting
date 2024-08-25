# Forecasting sales 
The goal of this kaggle project/competition is to develop a machine learning model to predict the sales of 33 product families across 54 stores for the period from August 16 to 30, 2017. The training dataset comprises 3 million transactions spanning from January 1, 2013 to August 15, 2017. In addition to this data, supplementary information on holidays and oil prices during this period is also provided.

### Exploratory data analysis 
- Recognized product families that experience a significant annual sales spike around the New Year
- Detected periods with maximum sales variation to understand seasonality, using periodogram analysis
- Utilized autocorrelation and partial autocorrelation plots to identify relevant lags for improving the forecasting model
### Modeling
Multivariate linear regression, neural network, and XGBoost models were trained on the dataset. For the multivariate regression model, we incorporated trend and seasonal features generated through a deterministic process, along with holiday and New Year indicators. This model was fitted for each combination of the 54 stores and 33 product families, resulting in a total of 1,782 models.

In contrast, the neural network and XGBoost models utilized a different set of features: week number, daily oil prices, day of the week, holiday indicator, New Year indicator, product family, number of products on promotion within each product family, and store number.

The models were trained using data from January 1, 2016, to August 15, 2017.
### Result
All three models delivered strong performance, each with an R² score of around 91%. Introducing lag features could further enhance accuracy.

## Important Notice

The code in this repository is proprietary and protected by copyright law. Unauthorized copying, distribution, or use of this code is strictly prohibited. By accessing this repository, you agree to the following terms:

- **Do Not Copy:** You are not permitted to copy any part of this code for any purpose.
- **Do Not Distribute:** You are not permitted to distribute this code, in whole or in part, to any third party.
- **Do Not Use:** You are not permitted to use this code, in whole or in part, for any purpose without explicit permission from the owner.

If you have any questions or require permission, please contact the repository owner.

Thank you for your cooperation.
