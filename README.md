# Image Classification Using Convolutional Neural Network
This project classifies images from the Cifar10 dataset using Convolutional Meural Network (CNN). The CNN model consists of several layers:

1. Input Layer:

Input shape: (32, 32, 3) which corresponds to an image of height 32, width 32, and 3 channels (RGB).

2. Convolutional Layers:
   First Conv2D layer:
   * 50 filters, each with a kernel size of (3, 3).
   * ReLU activation function.
   * Stride of (1, 1) which means the filter slides one pixel at a time.
   * Padding is set to 'same', which means the input image is padded with zeros so that the output has the same height and width.
   Second Conv2D layer:
   * 75 filters, each with a kernel size of (3, 3).
   * ReLU activation function.
   * Stride of (1, 1).
   * Padding is 'same'.
   Third Conv2D layer:
   * 100 filters, each with a kernel size of (3, 3).
   * ReLU activation function.
   * No padding specified, so it defaults to 'valid', which means no padding is added.
   Fourth Conv2D layer:
   * 125 filters, each with a kernel size of (3, 3).
   * ReLU activation function.
   * No padding.
     
3. Pooling Layer:
   MaxPooling2D layer:
   * Pool size of (2, 2), reducing the spatial dimensions by half. Helps in downsampling and reducing the number of parameters.
    
4. Dropout Layer:
   Dropout layer with a rate of 0.25, which randomly drops 25% of the input units during training, helping to prevent overfitting.

5. Flattening Layer:
   Flattens the input from a 2D matrix into a 1D vector, preparing it for input into the fully connected layers.

6. Fully Connected (Dense) Layers:
   First Dense layer:
   * 125 units with ReLU activation.
   * It is a fully connected layer, connecting every input neuron to every output neuron in the previous layer.
   Second Dense layer:
   * 10 units with softmax activation.
   * Outputs the probability distribution over the 10 classes.
