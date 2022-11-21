## Convolutional Neural Network & Autoencoder
Libraries used: Tensorflow (Keras), NumPy, Matplotlib


### Purpose
To both create and test an autoencoder, using the autoencoder to train a convolutional neural network

### Autoencoder Overview
An autoencoder is an unsupervised network created to recreate a lower-dimensional solution to higher-dimensional data. Dimensionality reduction can be important as this allows the creation of images without unnecessary "noise."

In this project, I tested out the effect of changing the number of hidden units in the single "bottleneck" layer of the autoencoder. I accomplished this
by creating an autoencoder function. This function allowed for the graphing of network performance with matplotlib as well.

With this function, I ended up creating a sufficient autoencoder and a bad autoencoder, visualizing the results of each network along the way. Additionally, I commented on my journey in configuring the network's architecture to show my thought process in doing so.

This autoencoder would be used to create reduced-dimensionality training patterns for classification with a CNN later.

### Classifier
The second part of this project is to run the second half of the original MINST images through the autoencoder network and save the hidden layer activations for each pattern. These represent the lower-dimensional representations created by the autoencoder. These are the reduced training patterns for use in the classifier. This is done through matrix operations in NumPy.

After the reduced training patterns are produced, a multi-layered network, learning through backpropagation, is used to classify the images into one of ten clothing items. After tweaking the architecture of the network, the classifier was evaluated against test data.

### Convolutional Neural Network
Next, a separate solution to classifying the images was tested, a convolutional neural network. In the Jupyter Notebook, I walked through my thought process for configuring the network to improve performance. I began to see signs of overtraining and adjusted the architecture to the best of my ability. This simple CNN produced an accuracy of about 88% on test data.
