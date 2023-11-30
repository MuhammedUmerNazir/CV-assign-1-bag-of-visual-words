# Computer Vision Bag of Visual Words

### Abstract/Introduction
The bag of visual words (BoVW) is a popular method for image
classification and recognition that extracts features from images and
represents them as visual words. In this task we first extract the
features from the images then we generate a visual vocabulary as
known as Codebook Generation, lastly we train two classifiers, one
using Support Vector Machines and the other one using Random Forest. We work on two datasets in this task, Objects Dataset and
Flowers Dataset and perform these tasks for both these datasets.

The first data set that was provided to us was the Objects dataset containing
four different types of objects. This dataset was already split into training and
test data and only needed to be loaded into the code in order to get started.
The training set contained 14 images of all 4 categories namely accordion,
dollar bill, motorbike and soccer ball. The test set contained 2 images per
category (8 images in total).
![Training Images Objects](https://user-images.githubusercontent.com/58668040/224603962-4a7a2917-349a-4568-a018-cb4b766df0d8.png)

The second dataset was the Flowers dataset which contained 3670 images
of five different types of flowers namely Daisy (633 images), Dandelion (898
images), Roses (641 images), Sunflowers (699 images), Tulips (799 images). In
this dataset, a suitable quantity of images must be chosen for training and test
sets. I kept 3450 out of 3670 images inside the training set whereas 220 images
for the test set. The division of training and test set per class was as follows:
1. Daisy: 600 train images, 33 test images.
2. Dandelion: 850 train images, 48 test images.
3. Roses: 600 train images, 41 test images.
4. Sunflowers: 650 train images, 49 test images.
5. Tulips: 750 train images, 49 test images

Flowers Dataset
![Daisy](https://user-images.githubusercontent.com/58668040/224603944-a6550435-fae0-4333-8b6c-8dc5ce072166.png)

The Bag of Visual Words is applied on a dataset in the following sequence of
steps.
1) Feature Extraction: Local features, such as shapes or textures, are
extracted from the input images. In my assignment, this is achieved using
Scale-Invariant Feature Transform (SIFT) which is an algorithm used for
detecting and describing local features in images. It works by finding distinc-
tive points in an image and representing them as a set of invariant descriptors.
2) Clustering: The local features are grouped into a number of clusters, and
each cluster represents a visual word. I have made use of K-means clustering
which is used for grouping data points into K number of clusters based on
similarity. It works by iteratively assigning each data point to its closest
cluster center and updating the cluster centers based on the mean of the data
points assigned to them.

3) Building Histograms: A histogram is built for each image, by counting the
occurrences of the visual words in the image.
4) Classification: A classifier is trained on the histograms of the training
images, and used to predict the labels of new images. In this assignment, I have
used two classifiers namely the Support Vector Machine (SVM) and Random
Forest. The main libraries used for this assignment are OpenCV and SciKit
Learn

### Instructions to Run the Code

First copy the files Joblibs on your machine.
Then Import the mentioned libraries and dependencies in the code.
Then load the Joblibs mentioned in the codes to load the models.

### Instructions to Run Train and Test Scripts

The path for train and test sets mentioned in the code needs to be altered to match with where the Datasets are located in your machine in order for this code to work.

### Visual Results
The images below show how SIFT feature detector outputs the features and key points in the images which then constitude towards the formation of the codebook or the visual vocabulary. 
![Flower Keypoints](https://user-images.githubusercontent.com/58668040/224603938-33526197-8401-4330-91e8-3778cc4fa810.png)
![Keypoints Objects](https://user-images.githubusercontent.com/58668040/224603948-4b9237c5-6113-452a-9f63-ae672b60065f.png)
![Keypoints Objects Image](https://user-images.githubusercontent.com/58668040/224603955-1d32a2cc-e988-4c1e-a6f2-826188a3bfee.png)


### Quantitative Results 
#### Objects Dataset

![CV_RF_Classifier](https://user-images.githubusercontent.com/58668040/224603336-1a4bb2e2-1e0d-40b4-8d7c-31d2f272a7ba.png)
![CV_RM_CM](https://user-images.githubusercontent.com/58668040/224603341-5f155b02-11af-4bc2-b63e-58f22e89615b.png)
![CV_SVM_Classifier](https://user-images.githubusercontent.com/58668040/224603344-049af849-e8ca-4a51-9371-3e2d24817d4c.png)
![CV_SVM_CM](https://user-images.githubusercontent.com/58668040/224603346-a953c0ae-3d28-4ce0-990b-f050501db926.png)
#### Flowers Dataset
![Flower_RF_CR](https://user-images.githubusercontent.com/58668040/224603629-66f42aea-eeac-4099-a2fd-975f36884ff7.png)
![Flowers_SVM_CR](https://user-images.githubusercontent.com/58668040/224603631-fce5d328-bc88-4b63-a718-247f124adf6e.png)
