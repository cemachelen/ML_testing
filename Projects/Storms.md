# Storm Tracking with Machine Learning #

This is a mini project that if takes off will move to the cemac repository. For now I leave this here as a skeleton plan for how you might go about something more exciting!

## Set Up ##

There are two options when working ARC3:

1. Container (Singularity is supported, but Docker image files can easily be converted into Singularity ones)
2. you can work straight on the machines and module load/pip install what you need.

Python is well-supported, with version >3.0 and most of the major machine learning libraries available (TensorFlow/Keras, Caffe + numpy, opencv, etc.).

**Step 1:** Experiment with standard tools, Singularity would make transfer of set up easier if we manage to make something of use. Especially if we try out auto Keras

<hr>

## Machine Learning Methods ##

* what sort of data do you have and how much (images? numbers?)
  * Module imagine output
  * Module numerical output

* what would you like to do to it (segment it, classify it, detect things in it?)
  * classify - storm or no Storm
  * potential subset strong storms

* what ground truth do you have already; what do you have to help train a model
  * We would have to use Julia's classification as "truth"

<hr>

# ML Options #

## Classifiers ##

* We have a whole suite of data. The "truth" classifiers storm only by precipitation.
* Storms have other features we know - wind speed, humidity, temperature

## Image recognition ##

* standard neural network such as R's work
* Auto Keras and Googles Auto ML

<hr>

Our constraint is time in which we can spend fine tuning this - probably half a day here and there.

My thoughts are that this should go for the easiest to implement solutions that potentially have the best benefits for potential other projects (GLAM)
* Auto Keras - If we learnt how to use then perhaps this could be a great easy option for future (Deep Learning)
* Something simple using perhaps scikit learn ? Niave Bayes, Kmeans ? Traditional
