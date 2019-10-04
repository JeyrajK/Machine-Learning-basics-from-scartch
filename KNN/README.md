## K-Nearest Neighbors

K nearest neighbors or KNN Algorithm is a simple algorithm which uses the entire dataset in its training phase. Whenever a prediction is required for an unseen data instance, it searches through the entire training dataset for k-most similar instances and the data with the most similar instance is finally returned as the prediction. 

Most similar items is found by calculating the distance between 2 data points ia a space.

The similarity measure is dependent on the type of data. For real-valued data, the Euclidean distance can be used. Other other types of data such as categorical or binary data, Hamming distance can be used.

In the case of regression problems, the average of the predicted attribute may be returned. In the case of classification, the most prevalent class may be returned.

** k in kNN algorithm represents the number of nearest neighbor points which are voting for the new test data’s class.**
![](KNN-Algorithm.png)

### Steps:
1. Find distances between new item and all other items
2. Pick k shorter distances
3. Pick the most common class in these k distances
4. That class is where we will classify the new item

The kNN algorithm is belongs to the family of instance-based, competitive learning and lazy learning algorithms.

Instance-based algorithms are those algorithms that model the problem using data instances (or rows) in order to make predictive decisions. The kNN algorithm is an extreme form of instance-based methods because all training observations are retained as part of the model.

It is a competitive learning algorithm, because it internally uses competition between model elements (data instances) in order to make a predictive decision.

Lazy learning refers to the fact that the algorithm does not build a model until the time that a prediction is required.

### References :
https://machinelearningmastery.com/tutorial-to-implement-k-nearest-neighbors-in-python-from-scratch/

https://www.geeksforgeeks.org/implementation-k-nearest-neighbors/


