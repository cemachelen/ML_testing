# Machine Learning #

Large data sets - find the useful information

* Python
* Stats
* Git

# supervised learning
--> show examples with know correct answers

# can be used for classifications
supervised
* matching tagged photos
* matching preference

unsupervised
- faud detection
- clustering

# Features and labels

scatter plots - clear patterns or not

# Decision surface
- clearly separates classes to allow classificiation of new point
- can be linear

# Naive BAYES

- find a decision surfaces

* SK LEARN (sci kit learn)

- fist look at gaussian niave bayes
- documentation is realy good
- test example code
- decide on classifier and create then fit features and lables
- able to predict class

* Must train and test on 2 different types of data
* must not over fit, use 10% data as test set

# BAYES RULE #

Probabilistic inference

Quiz:
prior probability of cancer is 1%, and a test has sensitivity and specitivity of 90% : therefore the chance is .9/10.9 = 8 % chance

Bayes rule:

There is a prior probability and posterior probability
posterior probability:

Prior:  P(c) = 0.01          P(noC)= .99
        P(pos|c) = 0.9       P(pos no C) = .1
        P(neg no c) = 0.9

joint: P(C pos) = P(c) * P(Pos|c) = 0.01* 0.9 = 0.009
       P(no C pos) = P(noC) * P(pos no C) = 0.99 * 0.1 = 0.099

Normalise = 0.108 (P pos)

posterior: P(c Pos)/ P (pos) = 0.009/0.108 = 8.3%
          P (no c pos) / P (neg) = 0.099/0.108

Seems complicated but can use bayes diagram

Used a lot in text learning using Naive BAYES

Called Niave because it's simple a probability assigned to a labels
it doesn't care of any context e.g. looking at word frequency alone not the order

Choosing an alogrithm:

Naive Bayse:
doens't recognise phrase and relations
easy to implement
