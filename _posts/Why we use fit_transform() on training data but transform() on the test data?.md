<!---
layout: post
title: "Why we use fit_transform() on training data but transform() on the test data?"
categories: Scikit-Learn
author:
- Anis Taluqdar
meta: "Springfield"
--->
<p align="center"> 
<img src="https://i.stack.imgur.com/QEPAU.png" width="600">
</p>


If you are somehow curious why StandardScaler uses fit_transform() for training and transform() for testing data then you are in the right place. 

Let’s first know what is fit_transform() and transform()

## fit_transform()
Fit to data, then transform it

fit_transform() used for scaling training data and learning the scaling  parameter from train data. So, the model learns the mean and variance of training data and scaling it.

## transform()
Perform standardization by centering and scaling

transform() used for scaling test data and it uses the same parameter of training data. It does not learn mean and variance from this model of test data. transform() uses the same parameter from fit_transform().


### Why don't we use the same fit_transform for both?

As fit_transform() scaling learns the parameter of data and scales it. We want the same scale for both training and testing data. We also want to make unknown the test data from our model so that we don’t scale by this data.


## Example:

{% highlight python %}
from sklearn.preprocessing import StandardScaler

# Create a StandardScaler instance
scaler = StandardScaler()

# Split the data into training and test sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Fit the StandardScaler to the training data and transform it
X_train_scaled = scaler.fit_transform(X_train)

# Transform the test data using the StandardScaler that was fit to the training data
X_test_scaled = scaler.transform(X_test)

# Now you can use the transformed data to fit a model
model.fit(X_train_scaled, y_train)

# And evaluate the model on the transformed test data
model.score(X_test_scaled, y_test)
{% endhighlight %}
