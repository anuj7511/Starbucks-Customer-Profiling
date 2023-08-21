## Project Motivation<a name="motivation"></a>

Understanding our customers is the key providing them a good service and sustain a profitable business. To understand them well, we need to pay attention on their purchase behaviour. One way we can collect and analyse their purchasing behaviour through an app, then identify their needs based on demographics.

The data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Periodically, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). However, some users might not receive any offer during certain weeks.
Using the data, I aim to :
- Gain understanding what types of customer characteristics and demographics are there.
- What offer should be sent to each customer ?
- How well can we predict customer response to offer ?

An unsupervised machine learning model with K-Means algorithm is used to cluster the customers. The number of clusters is chosen with 2 metrics - the higher Silhouette score and the lower Inertia / SSE value.

A supervised machine learning model with regression is used to predict the customer response rate to offer. The used metrics are mean squared error (MSE) and coefficent of determination (R^2)


## File Descriptions <a name="files"></a>

### Notebooks
There  are 3 notebooks available:
- part 1 about data understanding and cleaning process
- part 2 about EDA, feature preprocessing and unsupervised Machine Learning with KMeans.
- part 3 about supervised machine learning model to predict how well customer response to offer

Markdown cells were used to assist in walking through the thought process for individual steps.

### Helpers function
There is a `helpers.py` as utilities and also to extract features from the available data.
