## Neive-Bayes
Neive bayes is extremely fast relative to other classification algorithms. It works on Bayes theorem of probability to predict the class of unknown data sets.

Bayes Theorem provides a way that we can calculate the probability of a piece of data belonging to a given class, given our prior knowledge. Bayes’ Theorem is stated as:

P(class|data) = (P(data|class) * P(class)) / P(data)

Where P(class|data) is the probability of class given the provided data.

**Steps**

1: Separate the data poins by label.

2: Calculate the mean, standard deviation of the each features in label wise

3: calculate class probabilities of each test data using Gaussian Probability theorem.

Gaussian conditional probability is given by:
![](https://miro.medium.com/max/1576/1*0If5Mey7FnW_RktMM5BkaQ.png)
