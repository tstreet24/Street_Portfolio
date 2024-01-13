# Tanner Street's Portfolio
## Introduction
Hello! My name is Tanner Street, and I am currently a Master of Business Analytics student at MIT aspiring to be a data scientist or machine learning engineer. This portfolio contains three projects that I am especially proud of and reflect a variety of relevant skills. Each project header is hyperlinked to that project's repository, in case you are interested in seeing the code or more in-depth information. You can contact me via [LinkedIn](https://www.linkedin.com/in/tannerstreet/) or email at street24@mit.edu. 

## [Project 1: Optimal K-means and K-medoids Clustering](https://github.com/zack-horton/ML-Project)
### Overview
* Final project for Course 15.095: Machine Learning Under a Modern Optimization Lens at MIT
* This project is particularly interesting to me since it pertains to the intersection of machine learning and optimization. Indeed, the MBAn curriculum at MIT has convinced me of the power and importance of optimization, so my partner and I wanted to explore new avenues for this intersection. 

### Contributors
* [Zack Horton](https://github.com/zack-horton)
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
![alt text](https://github.com/tstreet24/Street_Portfolio/blob/27789bca24cb18553f72e8ed7b71fc64499ff2e1/images/project1-img1.png)

## [Project 2: ARMA-GARCH Modeling for Financial Forecasting](https://github.com/Theo-Dawson/A_EDGE)
### Overview
* Final project for Course 15.072: Advanced Analytics Edge at MIT
* I took a time-series course in my undergraduate degree and really enjoyed it. I wanted to further explore the field with this project by learning about GARCH and using ARMA in unique ways.

### Contributors
* [Zack Horton](https://github.com/zack-horton), [Emily Hahn](https://github.com/Ech232), [Theo Dawson](https://github.com/Theo-Dawson)
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
* Over 80% of the models capture autocorrelation and heteroeskadicity up to the 14th lag, indicating that ARMA-GARCH models are effective at characterizing the complex structure of time-series.
* Different evaluation criteria should be emphasized for different objectives. For example, for risk mitigation, models with the best prediction interval coverage probability should be considered best.
![alt_text](https://github.com/tstreet24/Street_Portfolio/blob/27789bca24cb18553f72e8ed7b71fc64499ff2e1/images/project2-img1.png)
  
## [Project 3: Green Epichlorohydrin Plant Production](https://github.com/zack-horton/Opt-Project)
### Overview
* Final project for Course 15.093: Optimization Methods at MIT
* I majored in chemical engineering for my undergradate degree. I still really like the field, so I wanted to do a project pertaining to the intersection of chemical engineering and analytics. The inspiration for this project comes from my senior design project, in which my team comprehensively designed a green ECH plant. However, the senior design project did not incorporate any optimization, leading to this project. 
  
* ### Contributors
* [Zack Horton](https://github.com/zack-horton)
### Tools
* Julia, JuMP
### Data
* Physical and chemical property data, such as molecular weights and stoichiometric coefficients, from PubChem
* Synthetized data for everything else (separator costs, reactor costs, etc.) based on real-world example

### Situation
* Epichlorohydrin (ECH) is a key intermediate in the production of epoxy resins, which are used in a large variety of products such as adhesives, electronics, and protective coatings. ECH has historically been produced using petroleum-derived byproducts, but recent research has demonstrated that ECH can also be produced using a glycerol-derived pathway, which is much more environmentally friendly. 

### Task
* Develop and optimize a chemical plant to produce and sell ECH produced via the glycerol-derived pathway.

### Actions
* Develop a realistic chemical plant outline that contains all of the necessary process units
* Generate synthetic, interesting data for each process unit in the plant (suppliers, separators, reactors, customers, and wastewater treatment) 
* Formulate constraints to account for chemical engineering principles such as conservation of mass, separator recoveries, reaction conversions, etc.
* Add interesting constraints that reflect issues faced by chemical engineers in real world, such as organic composition constraints in wastewater and varying purity requirements unique to each customer.
![alt_text](https://github.com/tstreet24/Street_Portfolio/blob/27789bca24cb18553f72e8ed7b71fc64499ff2e1/images/project3-img1.png) 

### Results
* The plant is financially successful, achieving a profit of 7.5M USD. The sales revenue is 20.2M, and the total operating cost is 12.7M USD.
* ~8K metric tons of material are sent to wastewater, resulting in total waste costs of nearly 900K USD. This is certainly an area of improvement for the plant. As a cost-savings measure, some of the unreacted reactants and byproducts from the second set of separators could be recycled back to the reactor to increase yield and reduce waste costs.
* The optimal solution does not suggest using most of the available capital. Scaling up the plant to utilize more of the available capital would thus require greater efficiency or external factors to change.
* The solution uses a mixture of low-cost and high-cost equipment.
![alt_text](https://github.com/tstreet24/Street_Portfolio/blob/27789bca24cb18553f72e8ed7b71fc64499ff2e1/images/project3-img2.png)

