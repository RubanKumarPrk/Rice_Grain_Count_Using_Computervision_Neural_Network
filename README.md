# Rice_Grain_Count_Using_Computervision_Neural_Network


Step 1: Creating a Training Set 
================================

	In This Module we are creating a training dataset of the images to use for the prediction we use

	- importing black image as background to display the contour of each grain
	- creating a directories of broken rice grain training set and full rice grain training set
	- storing the shape of background image that is to be used to resize the training images to fit the background.
	- creating lists to store the training images of respective classes
	- importing all the images of broken grains, resizing them to the size of background image
	- importing all the images of broken grains, resizing them to the size of background image
	- Creating a Function to preprocess the image
	- finding the contours of the broken rice grains and storing them in a list
	- finding the contours of the full rice grains and storing them in a list
	- method to increase the size of contours to print on the background image	
	- putting the contours of the broken rice grain filled in white on the black background and saving it in the given address.
	- putting the contours of the full rice grain filled in white on the black background and saving it in the given address .

Step 2 : Training Model
========================

	- importing all the dependancies
	- setting the image size for the neural network
	- address to the directory of training data for their respective classes
	- iterating through both the folders and adding the images to the training data list
	- shuffling the data so the model can learn better
	- break the dataset and store the features in X_train and labels in y_train
	- converting the data into numpy array
	- normalising the pixel values
	- creating the CNN model for classiying
	- first CNN layer with 32 layers and feature extractor of size 3x3
	- second CNN layer with 32 layers and feature extractor of size 3x3
	- third CNN layer with 64 layers and feature extractor of size 3x3
	- Flattening to get 1D array of features and defining the hidden layer with 64 neurons
	- activation function that returns the probability of a data lying in either classes
	- training the model over the training dataset
	- saving the CNN classifier model

Step 3 : Testing Model
=======================

	- importing all the dependencies
	- importing the output csv file, the background image, and the saved model
	- address to the tesing data and reading the test images one by one
	- converting the test image to grayscale
	- getting the contours and storring it in a list
	- method to scale the contour coordinates to the desired size
	- painting the contours on to the black background and saving the images in the given directory's address
	- counting the number of data that has probability of being broken grain greater than that of being a full grain
	- the count is the number of broken grains in the image
	- adding the values to the op dataframe and saving it to the final csv file
