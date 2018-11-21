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

* standard neural network such as R's work
* Auto Keras and Googles Auto ML

Our constraint is time in which we can spend fine tuning this - probably half a day here and there.

My thoughts are that this should go for the easiest to implement solutions that potentially have the best benefits for potential other projects (GLAM)

<hr>

## Convolutional Neural Networks ##

To start with we want to simply detect the storm in each time 

1. Time slice or 4D
  * 4D would be more complicated Activity Detection
  * Time Slice we can do a more traditional Method
2. Classification Task
  * Sliding window then piece together (0/1 array)
  * Segmentation find the whole storm - FNC (fully connected neural network) (UNET)

The best solution would be to do a FNC Segmentation Classification using pre built FCNs on Keras
then tweak. Things to consider:

* We have a lot of not storm so we might have to introduce loss weights to the loss function
  * this essentially penalises incorrect storms is it has to find a needle in a hay stack to its important if it misses a storm!

** Steps to Implement **

1. Generate a ground truth
  * binary map of 1/0 storm no storm for each hour
  * Perhaps look at one pressure level or all
  * box storm no storm
  * with metadata timestamp
  * corresponding "images" with timestamp
2. Once generated send a sample to R and she may suggest some FCNS and kenrnel size etc
  * Probably the best way would be share a Github repo if file sizes permit?
3. Test subsets on suggestions perhaps even on foe linux
5. Remember if the truth is a box the segment will be the actual storm so convert back to box to calculate the loss!
4. tweak/ fine tune
5. Implement on ARC
5. Train on both FC and CC subset
6. See how well it does - there are then some cool things we might be able to do stitching together showing the time evolution.
