# JKU_AIVizProject_Fashion-MNIST_The-Night-riders
We will investigate how increasing blur and reducing how corruption of images like lower or higher brightness or blur affect CNN’s predictions and confidence.
# Fashion-MNIST Classification Under Image Corruption

## Team

**The Night riders**

- Mohamed Abouelnasr — K12453145
- Hassan Gasser — K12455990
- Youssef Hamad — K12453150
- Ahmed Bakkar — K12438432

## Task

This project investigates how image corruption affects a pretrained convolutional neural network’s classification performance on Fashion-MNIST.

We examine Gaussian blur, darkening, and brightening at several severity levels. The same images are evaluated across all conditions so that individual predictions can be compared before and after corruption.

Our main questions are:

- How does accuracy change as corruption increases?
- Which clothing categories are most affected?
- Which classes are frequently confused?
- How confident is the model when its predictions are incorrect?

## Model

We use the pretrained CNN from
[tsilva/fashionmnist-classifier-cnn](https://huggingface.co/tsilva/fashionmnist-classifier-cnn).

- Architecture — CNN with channel sizes of 64, 128, and 256.
- Input — grayscale images with shape `1 × 28 × 28`.
- Output — scores for the 10 Fashion-MNIST classes.
- Preprocessing — scale pixels to `[0, 1]`, then normalize using mean `0.2860` and standard deviation `0.3530`.
- Model revision — `8b068e4063f2b03ea91651b0fa5877550616d6ae`.

The model is evaluated with its pretrained weights in evaluation mode. We do not train or fine-tune it.

## Dataset

We use the official Fashion-MNIST test split, loaded through `torchvision.datasets.FashionMNIST`.

- Test images — 10,000.
- Image size — `28 × 28` pixels.
- Format — grayscale.
- Classes — T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, and Ankle boot.
- Images per class — 1,000.

The corruption conditions are generated locally from the standard test images.

Dataset reference:
[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)
