# Diabetic retinopathy detection using deep CNN
Implementation for the Kaggle competition http://www.kaggle.com/c/diabetic-retinopathy-detection

The various data pre-processing techniques were per- formed using ImageMagick (a command line tool for image processing) and OpenCV.
CNN training performed using NVIDIA GeForce GTX 780 series GPU of RAM 3GB. 

# Overview

1. The train dataset consists of 35,126 images of resolution 512x512. Training on these images on all three color channels demand high memory requirements. Due to this limitation, images have been converted to single channel (green channel) which retained the maximum information. 

2. Dataset augmented using image transformations such as shear, flop, transverse and transpose to prevent over-fitting. 

2. Histogram equalization applied to enhance contrast of the image. 

3. Min-Max normalization implemented to reduce the effect of inherent background noise on the learning. 

4. Class balancing employed to prevent over-fitting of a particular class (Class 0). 

5. Implements an ensemble of 3 different 28 layer deep CNNs each differing in the number of hidden units or filters. 

6. Zero padding utilized to preserve the spatial size of input and output volumes. 

7. Activation function for convolution and hidden layers is Leaky Rectifier. 

8. Obtains a quadratic kappa score of 0.3996. 
