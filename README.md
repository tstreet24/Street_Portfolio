# Tanner Street's Portfolio

## Project 1: Optimal K-means and K-medoids Clustering
* Final project for Course 15.095: Machine Learning Under a Modern Optimization Lens at MIT
### Contributors
* Zack Horton
### Tools
* Julia, JuMP
### Data
* Abalone from UC Irvine Machine Learning Repository (4177 observations, 9 features, mostly continuous)
* Similarity Prediction from UC Irvine Machine Learning Repository (100 observations, 17 features, mostly categorical)
### Preprocessing
* Min-max normalization
* Standardization
### Situation
* Clustering is typically performed using heuristic algorithms, so optimality is not guaranteed and results vary based on random initializations.
### Task
* Formulate optimization models to address the shortcomings of heuristics while also remaining scalable and time efficient.
### Actions
* Use mixed-integer modeling to perform k-means and k-medoids clustering.
* Compare the optimization models to heuristic algorithms using metrics such as within-cluster sum of squares and silhouette scores.
* Evaluate the models on a diverse range of scenarios to find generalizable results by varying characteristics such as dataset, number of observations, number of clusters, usage of warm starts, etc.
### Results
* K-means and k-medoids clustering can be developed into optimization models using mixed-integer techniques. The models struggle to converge or improve the warm start solution as dataset size increases and when euclidean distance is used. 

## Project 2: ARMA-GARCH Modeling for Financial Forecasting
* Final project for Course 15.072: Advanced Analytics Edge at MIT
### Tools
* R, Python
### Data
* Daily closing prices of the PIMCO Active Bond Exchange-Traded-Fund (with ticker BOND) between November 2018 and November 2023
* BOND is an ETF encompassing a portfolio of bonds
* Data collected from yfinance python package

### Preprocessing
* Log transformation to stabilize variance
* Dummy variables for seasonality

### Situation
* Forecasting the prices of financial instruments is a powerful technique in a variety of scenarios, such as portfolio optimization, risk mitigation, etc. However, forecasting is challenging for many reasons, mostly due to the inherently unpredictable nature of markets and the autocorrelated structure of time-series.
  
### Task
* Use a combination of regression, ARMA, and GARCH models to forecast the daily closing price of BOND up to 14 days in advance.

### Actions
* Fit regression model using time and seasonal dummy variable to capture trend and seasonality. Fit ARMA model on regression model's residuals to capture autocorrelation. Fit GARCH model on regression model's residuals to capture heteroeskadicity.
* Generate point predictions by summing regression and ARMA forecasts. Generate prediction intervals by summing point prediction and GARCH forecast (multiplied by desired Z-score).
* Generate thousands of models by varying parameters from each component.
* Evaluate models using metrics such as the Box Test, the White Test, root mean square error, mean directional accuracy, etc.

### Results
* Over 80% of the models captured autocorrelation and heteroeskadicity up to the 14th lag, indicating that ARMA-GARCH models are effective at characterizing the complex structure of time-series.
* Different evaluation criteria should be emphasized for different objectives. For example, for risk mitigation, models with the best prediction interval coverage probability should be considered best. 
  
## Project 3: Green Epichlorohydrin Plant Production
* Final project for Course 15.093: Optimization Methods at MIT
### Tools
* Julia, JuMP
### Data


### Preprocessing

### Situation
* Clustering is typically performed using heuristic algorithms, so optimality is not guaranteed and results vary based on random initializations.

### Task

### Actions

### Results

