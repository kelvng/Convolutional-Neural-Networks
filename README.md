# Learn Convolutional Neural Networks For Image Classification

## Introduction
Convolutional Neural Networks (CNN) is one of the most popular and most influential deep learning models in the Computer Vision community. CNN is used in many problems such as image recognition, video analysis, MRI images, or for articles in the field of natural language processing, and most of them solve these problems well. <br/> <br/> CNN also has a long history. The original architecture of the CNN model was introduced by a Japanese computer scientist in 1980. Then, in 1998, Yan LeCun first trained the CNN model with the backpropagation algorithm for the handwriting recognition problem. . However, it wasn't until 2012, when Ukrainian computer scientist Alex Krizhevsky (filed by Geoffrey Hinton) built a CNN (AlexNet) model and used a GPU to speed up training deep nets to reach the top. 1 in the ImageNet annual Computer Vision competition with top 5 classification error reduced by more than 10% compared to previous traditional models, created a strong wave of using deep CNN with the help of GPUs to solve. more and more problems in Computer Vision.

## Image Classification 
In this blog post, I introduce the specific architecture of the CNN model for the image classification problem. Image classification is the most important problem in Computer Vision. We already have a lot of research to solve this problem by extracting very common features like SIFT, HOG and then giving it to computer learning, but these methods are not really effective. But on the contrary, for humans, we have great instincts to classify objects in our surroundings in an easy way.
The input to the problem is a photo. An image is represented by a matrix of values. The classification model will have to predict the image layer from this pixel matrix, for example if the image is a cat, dog, or bird. 

<div class="img-div" markdown="0">
    <img src="/images/cnn_input.png" />
</div>

To represent a 256x256 pixel image in a computer, we need a matrix that will have a 256 × 256 dimension diameter, and depending on whether the image is color or gray, this matrix will have the corresponding channel number, for example with an image. 256x256 RGB color, we will have a 256x256x3 matrix to represent this image.

## The link between CNN and vision
CNN is closely linked with biology, namely the visual cortex, which processes information related to images from receptors located in the human eye. In 1962, two American neuroscientists Hubel and Wiesel explored how to organize brain cells to process visual information, and these organizations took on the task. In this ![video] (https://www.youtube.com/watch?v=Cw5PKV9Rj3o), you can hear the sound representing which cells the brain responds to images, angles, directions. of lines that appear in the video in a certain order. This means that each neuron is set up in response to certain fixed characteristics of that neuron. 
<div class="img-div" markdown="0">
    <img src="/images/cnn_visual_cortex.jpg" />
</div>


# Dataset
You can download the processed dataset at [here] (https://drive.google.com/open?id=1ABhwNb5ioRzUEV9iLDpVSEIV_76yofNm).
