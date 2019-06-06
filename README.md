# Generative Adversarial Network (GAN) - PyTorch implementation

## There are two components in GAN:

### 1. Generative - Take random noise signal as input and output the image

### 2. Discriminator - It assess the image created by Generator and provides the feedback.

Both trained/learn together as discriminator has ground truth images or real world images to compare.


## How to train GAN

### Two Steps

#### Step 1. Training a Discriminator
                1.1 Input random noise signal to Generator and output the image
                1.2 Input the generated image to Discriminator
                1.3 Discriminator output the probabilities 
                1.4 Then calculate error based on ground truth images and back propagate the error to discriminator and update                     the weights

![alt text](https://github.com/dilipajm/gan/blob/master/images/training-discriminator.png)


#### Step 2. Training a Generator
                2.1 Input same image from generator to Discriminator (which is already trained earlier)
                2.2 Get discriminator probabilities
                2.3 Back propagate the errors to Generator & update the weights

![alt text](https://github.com/dilipajm/gan/blob/master/images/training-generator.png)
