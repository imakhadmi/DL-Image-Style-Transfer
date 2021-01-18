[//]: # (Image References)

[image1]: ./notebook_ims/vgg19_convlayers.png "CNN Layers"
[image2]: ./images/paris-starry_night.png "Sample Output 1"
[image3]: ./images/paris-starry_night_comparison.png "Sample Output Comparison 1"
[image4]: ./images/dc_capitol-new_york.png "Sample Output 2"
[image5]: ./images/dc_capitol-new_york_comparison.png "Sample Output Comparison 2"
[image6]: ./images/seattle-the_scream.png "Sample Output 3"
[image7]: ./images/seattle-the_scream_comparison.png "Sample Output Comparison 3"

## Image Style Transfer using CNNs Implementation in PyTorch

This repository contains code in the main Jupyter Notebook `style_transfer_notebook` that shows an implementation of the Image Style Transfer method that is outlined in the paper, Image Style Transfer Using Convolutional Neural Networks, by Gatys et al. in PyTorch using the ImageNet pre-trained VGG19 model.

![CNN Layers][image1]

### Project Structure

1. Load in VGG19 model (features, which are the convolutional and pooling layers of the model) and freeze model parameters
2. Load in content and style images
3. Map VGG layers to be used for the content and style features
4. Calculate the gram matrix of a given tensor (the tensor being the output of a given convolutional layer)
5. Applying weight values for individual style layers, overall content weight (alpha), and overall style weight (beta)
6. Calculate losses (Content Loss, Style Loss, and Total Loss)
7. Run a training loop with a decided number of steps to update the target image only
8. Display the target image

Further detailed information on each step of the project can be found in the following notebook file.
	
	```
		style_transfer_notebook.ipynb
	```

### Sample Style Transfer Images

![Sample Output 1][image2]

![Sample Output Comparison 1][image3]

![Sample Output 2][image4]

![Sample Output Comparison 2][image5]

![Sample Output 3][image6]

![Sample Output Comparison 3][image7]

### Packages Required to Run Project

	```
		io
		matplotlib
		numpy
		PIL
		torch
		torchvision
	```