# Speech-Emotion-Recognition

We have a dataset that consists of speeches of 24 professional voice actors(12 male, 12 female) that are recorded with different emotions. 60 trails were taken per each actor. Each audio file is named in a format

We need to classify this data into 8 classes. 00 = neutral 01 = calm 02 = happy 03 = sad 04 = angry 05 = fearful 06 = disgust 07 = surprised

We do the classification in 4 steps.

Feature Extraction:- We load the audio data using librosa library.This library converts the continuous audio data to a discrete numpy array. And then we extract the MFCC features from the loaded numpy array using librosa.

Preprocessing the data: We may get different length arrays from each audio data.So we need to make sure that the length of all the arrays is same. So we take the maximum length of all the arrays and pad every array with zeros at the end. We split the data into two sets.One is training and the other is test set(90% training and 10% test) using scikit-learn library

Creating a model: Network archictecture can be of any type like simple,deep,convolutional. We are going to use convolutional neural network using keras.So we initialise a keras sequential model and then add layers to it.

Fitting the model: Now we are going to train the data set using the model we created. After training the set we test it by predicting the classes of the test set.

We achieved the accuracy of upto 63% which is quite good considering the vagueness of sound data in general.

<p align="center">
  <img src="./model.png" width="350" title="hover text">
<!--   <img src="your_relative_path_here_number_2_large_name" width="350" alt="accessibility text"> -->
</p>
