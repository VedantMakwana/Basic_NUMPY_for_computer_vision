
# Basic Numpy for Computer vision
To represent an image as an array using the NumPy library in Python, we can utilize NumPy's array data structure. Here's an example of how to do it:




```bash
import numpy as np

# Grayscale image example
grayscale_image = np.array([
    [50, 60, 70],
    [100, 110, 120],
    [150, 160, 170],
    [200, 210, 220]
])

# Color image example
color_image = np.array([
    [[255, 0, 0], [0, 255, 0], [0, 0, 255]],
    [[255, 255, 0], [255, 0, 255], [0, 255, 255]],
    [[255, 255, 255], [0, 0, 0], [128, 128, 128]]
])

# Accessing pixel values
print(grayscale_image[0, 1])  # Output: 60
print(color_image[1, 2])      # Output: [0, 255, 255]

```
In the above example, we import the NumPy library and create NumPy arrays to represent the grayscale and color images. For the grayscale image, we use a two-dimensional NumPy array, and for the color image, we use a three-dimensional NumPy array.

We can access the pixel values of the images by indexing into the arrays. In this case, grayscale_image[0, 1] returns the pixel value at the first row and second column of the grayscale image, which is 60. Similarly, color_image[1, 2] returns the RGB values of the pixel at the second row and third column of the color image, which is [0, 255, 255].
