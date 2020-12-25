## Problem Statement:
Lets say you want to develop a cool feature in the smart-TV that can recognize five different gestures performed by the user which will help users control the TV without using a remote.
The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:
Thumbs up:  Increase the volume
Thumbs down: Decrease the volume
Left swipe: 'Jump' backwards 10 seconds
Right swipe: 'Jump' forward 10 seconds  
Stop: Pause the movie

Dataset:
The training data consists of a few hundred videos categorized into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use. Each video is a sequence of 30 frames (or images). 
The dataset has been divided into train and val. The dataset has been uploaded to https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL 

## Approach:
We have defined a generator function that is able to successfully input a batch of videos to the model. 
In the generator, we preprocessed the images as we have images of 2 different dimensions as well as created a batch of video frames. We have experimented with `img_idx`, `y`,`z`, image resizing, normalization, batch size in order to obtain a high accuracy.
We experimented with different values of Batch size, and found the maximum working value to be 80. Increasing batch size further, resulted in a ResourceExhaustedError. So we have chosen batch size of 80 as our final value.
We have tried multiple models based on 3D Convolution, CNN + LSTM and Transfer Learning models.

The performance and model details can be found in a tabular form in the doc. fiel attached.
