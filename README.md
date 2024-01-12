# Tanner Street's Portfolio

## Project 1: Optimal K-means and K-medoids Clustering
* Final project for Course 15.095: Machine Learning Under a Modern Optimization Lens at MIT
### Tools
* Julia, JuMP
### Data
* Abalone from UC Irvine Machine Learning Repository
* Similarity Prediction from UC Irvine Machine Learning Repository
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
