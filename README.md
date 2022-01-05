
# **Adaptation to new classes using 2-step method**

Group Member: Chenchen Tang, Haojia Nie

This work explores the method using unsupervised to train classification network to detect K+N classes. Given K classes with labels, we use them to train a supervised convolutional neural network. Our goal for this step is to minimize the loss and produce relatively high accuracy for the detection of the K classes. Then we use the trained network and input it with (K+N) classes, which N classes unseen by the network. In this step, we exclude the top dense layers of the trained network and only collect the middle layer features produced by the network. Then we use those features to perform K-means clustering and the classification yield by the clustering would be our prediction result.

Besides from that, we've also tried a new way of preprocess the dataset. Instead of using the original image and and apply transformations. We create artificial sample image by randomly choose X images from the same class and combine them together. It helps the network to learn more features and yield a better accuracy for the K+N class detection. 

The main goal of the project is to produce a way of classification that is able to adapt to new classes. We have demonstrated that using the features of the trained network for clustering performs better than regular K-means using original images. It has been shown that it has the better capability for the classification of unseen classes.
