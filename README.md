# Semantic Segmentation - Advaced Deep Learning

## Inroduction
The goal is to create a fully convolutional neural network (FCN) based on the VGG-16 image classifier architecture to identify drivable road area from a car dahcam image. The KITTI data set is used for training and testing.

### Neural Net
An already trained neural network (VGG-16) is converted to a fully convolutional neural network.
- The final fully connected layer is dropped
- a 1x1 convolution with depth=num_classes is added
- skip connections are introduced
- upsampling layers are added (transpose convolutions) till the spatial size matches the size of the input images

![architecture](./media_readme/3-Figure3-1.png)

### Hyperparameters
The hyperparameters used for traing are:
- learning_rate: 0.0005
- dropout: 0.5
- batch_size: 5
- epochs: 60

The Adam optimizer and cross-entropy as loss function is used.

### Results

#### Segmentation after 2 Epochs
![segmentation_2](./media_readme/segmentation_after_epoch_2.png)

#### Segmentation after 10 Epochs
![segmentation_10](./media_readme/segmentation_after_epoch_10.png)

#### Segmentation after 20 Epochs
![segmentation_20](./media_readme/segmentation_after_epoch_20.png)

#### Segmentation after 30 Epochs
![segmentation_30](./media_readme/segmentation_after_epoch_30.png)

#### Segmentation after 40 Epochs
![segmentation_40](./media_readme/segmentation_after_epoch_40.png)

#### Segmentation after 50 Epochs
![segmentation_50](./media_readme/segmentation_after_epoch_50.png)

#### Segmentation after 60 Epochs
![segmentation_60](./media_readme/segmentation_after_epoch_60.png)

---
## *The following is the original Udacity README for this project*

### Introduction
In this project, you'll label the pixels of a road in images using a Fully Convolutional Network (FCN).

### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
**Note** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.

### Submission
1. Ensure you've passed all the unit tests.
2. Ensure you pass all points on [the rubric](https://review.udacity.com/#!/rubrics/989/view).
3. Submit the following in a zip file.
 - `helper.py`
 - `main.py`
 - `project_tests.py`
 - Newest inference images from `runs` folder  (**all images from the most recent run**)
 
 ## How to write a README
A well written README file can enhance your project and portfolio.  Develop your abilities to create professional README files by completing [this free course](https://www.udacity.com/course/writing-readmes--ud777).
