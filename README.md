## Project Motivation<a name="motivation"></a>

Understanding our customers is the key to sustain a profitable business. To understand them well and identify their needs based on demographics, we need to pay attention on their purchase behaviour by collecting and analysing their purchasing behaviour through an app.

The data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Periodically, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). However, some users might not receive any offer during certain weeks.
Using the data, I aim to :
- Gain understanding what types of customer characteristics and demographics are there.
- What offer should be sent to each customer ?
- How well can we predict customer response to offer ?

An unsupervised machine learning model with K-Means algorithm is used to cluster the customers. 

A supervised machine learning model with regression is used to predict the customer response rate to offer. 

## Project Metrics :

### Unsupervised Machine Learning Model
An unsupervised machine learning model with K-Means is used to cluster the customers.

The number of clusters is choosed with 2 metrics :
1. The [Silhouttee score](https://en.wikipedia.org/wiki/Silhouette_(clustering))
```
The silhouette value is a measure of how similar an object is to its own cluster (cohesion) compared to other clusters (separation). The silhouette ranges from −1 to +1, where a high value indicates that the object is well matched to its own cluster and poorly matched to neighboring clusters.
```

2. The Inertia / Sum Square Error (SSE) value, can be recognized as a measure of how internally coherent clusters are. We seek to minimize the value.

### Supervised Machine Learning Model
A Supervised Machine learning using regression algorithm is used to predict customers offer completed rate.
The regression metrics are :
1. Mean Squared Error (MSE):
2. Coefficient of Determination (R^2)

## File Descriptions <a name="files"></a>

### Notebooks
There  are 3 notebooks available:
- part 1 about data understanding and cleaning process
- part 2 about EDA, feature preprocessing and unsupervised Machine Learning with KMeans.
- part 3 about supervised machine learning model to predict how well customer response to offer

Markdown cells were used to assist in walking through the thought process for individual steps.

### Helpers function
There is a `helpers.py` as utilities and also to extract features from the available data.
