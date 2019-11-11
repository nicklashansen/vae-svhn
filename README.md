# VAE on SVHN dataset

In this notebook I train a VAE on the [Street View House Numbers](http://ufldl.stanford.edu/housenumbers/) dataset. I use the full dataset but with images rescaled to 16x16 (down from 32x32). The network is a VAE using a ResNet-like architecture for the encoder and decoder as well as linear layers learning the mean and variance of the pixel intensity for each color channel and for each pixel in the image. The prior has been chosen to be a standard normal Gaussian and the approximate posterior is a diagonal covariance Gaussian. Total network depth is 38 layers. The network can be trained in approximately 1 hour on a V100 GPU.

## How to run

If you download the dataset from [this link provided by UC Berkeley](https://drive.google.com/file/d/1D4mpm1mEJd1xVq_xANCD58pLIOeiny0L/view?usp=sharing) and place it in the same folder as the notebook, you should be able to run the code as is (assuming that you have installed the required pip packages).

## Results

Here's a few reconstructions and samples after training for 50 epochs.

![svhn](https://i.imgur.com/AKHf6Y1.png)
