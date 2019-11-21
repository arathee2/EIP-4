# score
print(score)
> 0.9908

# definitions

1. Convolution: In simple langauge, it scans a channel (a black and white image, for example) using a kernel. Mathematically, it computes the hadamard product between the kernel and the image portion that it looks at and takes the sum of the values of the hadamard product. This process repeats until the kernel scans (and makes these computations on) the entire image going from left-to-right and top-to-bottom (like scanning a table row by row).

2. Filters/Kernels: A way to extract or filter out meaningful features from a channel. An example of such features edges.

3. Epochs: Number of runs over the training data.

4. 1x1 Convolution: Scanning the image (left-to-right and top-to-bottom) pixel by pixel to extracts features that are representative of the image for example. A 1x1 convolution simply multiplies the weight of the kernel and does this for each pixel in the image which becomes the feature map.

5. 3x3 Convolution: Scanning the image (left-to-right and top-to-bottom) with a window of size 3x3 that extracts features that are representative of the image. A 3x3 convolution computes a hadamard product between the portion of the image being looked at and the filter. Then, the result is calculated by taking the sum of all the values of this hadamard product. This is one entry in the feature map. All such possible entries are calculated by scanning the entire channel to give the full feature map for a particular kernel.

6. Feature Maps: Features that are extracted after applying a kernel to a channel.

7. Activation Function: A function applied to the feature map to make the neural network non-linear and more complex and more powerful. Popular such functions are relu, tanh, and sigmoid.

8. Receptive Field: The portion of image that's being looked at at a given time.