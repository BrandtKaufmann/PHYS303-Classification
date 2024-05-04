# PHYS303-Classification
98.73 Val Accuracy, .989 AUC using EfficientNetV2B0 

## Part I. Downloading the image data
https://www.microsoft.com/en-us/download/details.aspx?id=54765


## Part II. Preprocessing
* A) Make sure that each image has 3 channels (RGB). Sometimes you encounter images with 4
channels. In that case, it’s almost always the case that one of the channel is the transparency
channel. RGBA being one of the most common pattern for images that include transparency. In
the RGBA model, A (Alpha): Represents the transparency of the pixels. This channel controls the
transparency of the image. For example, for an 8-bit image, a value of 0 indicates full
transparency (completely clear) and a value of 255 indicates full opacity (completely solid).
There are also one or two images that are corrupted (0 KB), one of which has an name of “666”).
When you submit your homework, please include code to remove these images, as well as to
ensure that all images have only 3 channels.
* B) Normalize pixels as you saw in class. Sometimes they are rescale to 0 and 1, or –1 and 1, or 0
and 255. This can depend on the architecture you adopt (see next part).
* C) Make sure that all the images have the same size. If not, you may use resize() from
skimage (see the example of the image for the astronaut in one of the notebooks).

## Part III. Architecture and Training
You can:
1. Use a custom architecture of your own deign, either a CNN or a ResNet (or MLP)
2. Use TensorFlow or PyTorch
3. Use an “off-the-shelf” architecture (e.g., ResNet18)
* You can either use a pre-trained model, or
* Train “from scratch”
4. You may train as many models as you would like. But you may only do one of the following:
  * Submit one model, your best model, or
  * If you want to use multiple models, specify your “voting” scheme
5. Address all deprecation issues — that way you code will last longer!
For training, use an 8:2 split between the training and validation sets. You can try other ratios if
you’d like (between 7:3 - 9:1 are all reasonable).
You can experiment with different optimizers, different activation functions, learning rates, and
learning rate decay schedules.

## Part IV. Performance Metrics
You code should show and the loss vs. training epoch figure, the ROC curve, and the Precision-
Recall curve.

## Part V. Classification Challenge
On Monday, April 22, in class we will do a classification challenge. 
