# Computer_Vision_Autoencoders
Examin autoencoders on CIFAR10 and self-generated data

## How to
Clone the repository and examin two notebooks for different purposes:
- Training autoencoder on CIFAR10 images and use dimensionality reduction by **t-SNE on bottleneck activations** [Jupyter-Notebook](t_SNE_on_activations.ipynb)
- Training autoencoders on self-generated images of squares and circles and use to **convert circles to squares** [Jupyter-Notebook](Autoencoder_circle_squares_conversion.ipynb)

## Description
### CIFAR10 / t-SNE
An autoencoder is trained to reproduce CIFAR10 images with a bottleneck of 128 neurons. Later the activations of the bottleneck layer are visualized in 2D with t-SNE algorithm. 

As comparison for visualization with t-SNE, the MNIST dataset is visualized by t-SNE aswell. For both data representatives of small squared regions in the t-SNE plain are plotted simultaneously. Allowing to observe the change of images with coordinates in the t-SNE plain. Particularly the MNIST representation changes within the clusters quite graduarly, for example from upright written to crooked writings of the same number.

### Autoencoders on self-generated data
A class is provided to generate images of squares or circles. Moreover corresponding circles and squares can be constructed as data. This means, that images with circles and their counterparts with squares at the same location and the same size in pixel can be generated.
1. An autoencoder is trained on these images.
2. An autoencoder is trained on training data that holds circles and the corresponding (equal in size, color and size in pixels) squares.

The autoencoder bases on convolutional layer and holds only **9 neurons** in its bottleneck layer. Both tasks succeed after hyperparameter tuning, in task 2 circles from evaluation data are turned into squares.
