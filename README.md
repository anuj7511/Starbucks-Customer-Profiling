## Project Motivation<a name="motivation"></a>

Understanding our customers is the key to sustain a profitable business. To understand them well and identify their needs based on demographics, we need to pay attention on their purchase behaviour by collecting and analysing their purchasing behaviour through an app.

The data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Periodically, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). However, some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the CHALLENGE to solve with this data set.

Using the data, I aim to :
- Gain understanding what types of customer characteristics and demographics are there.
- What offer should be sent to each customer ?
- How well can we predict customer response to offer ?

An unsupervised machine learning model with K-Means algorithm is used to cluster the customers. 

A supervised machine learning model with regression is used to predict the customer response rate to offer. 

## Problem Statement
Your task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.

You'll be given transactional data showing user purchases made on the app including the timestamp of purchase and the amount of money spent on a purchase. This transactional data also has a record for each offer that a user receives as well as a record for when a user actually views the offer. There are also records for when a user completes an offer.

Keep in mind as well that someone using the app might make a purchase through the app without having received an offer or seen an offer.

## Project Metrics :

### Unsupervised Machine Learning Model
The number of clusters in K-Means algorithm is choosed with 2 metrics :
1. The [Silhouttee score](https://en.wikipedia.org/wiki/Silhouette_(clustering))
```
The silhouette value is a measure of how similar an object is to its own cluster (cohesion) compared to other clusters (separation). The silhouette ranges from −1 to +1, where a high value indicates that the object is well matched to its own cluster and poorly matched to neighboring clusters.
```

2. The Inertia / [Sum Square Error (SSE)](https://en.wikipedia.org/wiki/Residual_sum_of_squares) value, can be recognized as a measure of how internally coherent clusters are. We seek to minimize the value.

### Supervised Machine Learning Model
The regression metrics are :
1. [Mean Squared Error (MSE)](https://en.wikipedia.org/wiki/Mean_squared_error):
2. [Coefficient of Determination (R^2)](https://en.wikipedia.org/wiki/Coefficient_of_determination)

## File Descriptions <a name="files"></a>

### Notebooks
There  are 3 notebooks available:
- part 1 about data understanding and cleaning process
- part 2 about EDA, feature preprocessing and unsupervised Machine Learning with KMeans.
- part 3 about supervised machine learning model to predict how well customer response to offer

Markdown cells were used to assist in walking through the thought process for individual steps.

### Helpers function
There is a `helpers.py` as utilities and also to extract features from the available data.
