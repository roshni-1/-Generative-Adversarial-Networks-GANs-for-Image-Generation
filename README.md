# GANs for Image Generation

This project demonstrates how to implement Generative Adversarial Networks (GANs) using the MNIST dataset. GANs are a class of machine learning frameworks designed by Ian Goodfellow and his colleagues in 2014. The goal is to generate new data samples that resemble the training data.

## Project Overview

The project consists of training a GAN to generate handwritten digit images similar to those in the MNIST dataset. The GAN architecture involves two neural networks, a generator, and a discriminator, which are trained simultaneously.

- **Generator**: Takes random noise as input and generates images.
- **Discriminator**: Takes an image as input and outputs a probability indicating whether the image is real or generated.

The goal of the generator is to produce images that are indistinguishable from real images, while the discriminator aims to correctly classify images as real or generated.

## Dataset

The MNIST dataset, a collection of 70,000 handwritten digit images (60,000 training and 10,000 test samples), is used in this project. Each image is a 28x28 grayscale image.

## Architecture

### Generator

The generator model takes a 100-dimensional noise vector as input and generates 28x28x1 images. It consists of:

- Dense layers
- LeakyReLU activations
- BatchNormalization layers
- Conv2DTranspose layers for upsampling

### Discriminator

The discriminator model takes a 28x28x1 image as input and outputs a single scalar value (probability of the image being real). It consists of:

- Conv2D layers
- LeakyReLU activations
- Dropout layers
- Dense layers

### Combined Model

The combined model stacks the generator and discriminator models. The discriminator is set to non-trainable when training the generator.

## Installation

To run this project, you need to have Python and the following libraries installed:

- numpy
- matplotlib
- tensorflow
- keras

You can install the required libraries using pip:

```bash
pip install numpy matplotlib tensorflow keras



