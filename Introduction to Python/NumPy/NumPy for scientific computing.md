**Project: Image manipulation with NumPy**

In this project, you will use NumPy to manipulate digital images. You will load an image into a NumPy array, perform various operations on the array, and save the modified image back to disk. Here are the steps you can follow:
- Choose an image to work with. You can use any image file format supported by the Python Imaging Library (PIL), such as JPEG, PNG, or BMP.
- Load the image into a NumPy array using the PIL.Image.open() function. This will create a NumPy array that represents the pixels of the image.
- Perform various operations on the array to modify the image. For example, you can:
    - Convert the image to grayscale by averaging the RGB values of each pixel.
    - Resize the image by scaling the array using the numpy.resize() or numpy.repeat() functions.
    - Apply a filter to the image, such as a Gaussian blur or edge detection.
- Save the modified image back to disk using the PIL.Image.fromarray() function.
- Display the original and modified images side-by-side for comparison using the matplotlib.pyplot.imshow() function.

Resources and links:
- NumPy documentation: [https://numpy.org/doc/stable/](https://numpy.org/doc/stable/)
- Python Imaging Library (PIL) documentation: [https://pillow.readthedocs.io/en/stable/](https://pillow.readthedocs.io/en/stable/)
- Matplotlib documentation: [https://matplotlib.org/stable/contents.html](https://matplotlib.org/stable/contents.html)
- Sample code for image manipulation with NumPy: [https://www.geeksforgeeks.org/image-manipulation-using-numpy-python/](https://www.geeksforgeeks.org/image-manipulation-using-numpy-python/)

**Sample code**

```Python
import numpy as np
from PIL import Image
import matplotlib.pyplot as plt
from scipy.ndimage import gaussian_filter
# Load the image using the PIL library
image = Image.open('path to image.jpg')
# Convert the image to a NumPy array
image_array = np.array(image)
# Convert the image to grayscale by averaging the RGB values of each pixel
gray_image_array = np.mean(image_array, axis=2, keepdims=True)
new_height = 100
new_width = 80
# Resize the image using the numpy.resize() function
resized_image_array = np.resize(gray_image_array, (new_height, new_width, 1))
resized_image_array = resized_image_array.reshape(new_height, new_width)
# Apply a Gaussian blur filter to the image using the scipy.ndimage.gaussian_filter() function
blurred_image_array = gaussian_filter(gray_image_array, sigma=(5, 5, 0))
# Convert the NumPy array back to an image using the PIL.Image.fromarray() function

modified_image = Image.fromarray((blurred_image_array[0]*255).astype(np.uint8))

# Save the modified image to disk using the PIL.Image.save() function
modified_image.save('path to save image.jpg')
# Create a subplot with two images: the original image and the modified image
fig, axs = plt.subplots(1, 2, figsize=(10, 5))
axs[0].imshow(image_array)
axs[0].set_title('Original Image')
axs[1].imshow(blurred_image_array)
axs[1].set_title('Modified Image')
plt.show()
# Load the image to make it gray scale

# Convert the image to a NumPy array
img_array = np.array(image)

# Convert the RGB values to grayscale using numpy.dot()
gray_array = np.dot(img_array[...,:3], [0.5, 0.5, 0.5])

# Convert the grayscale array back to an image
gray_image = Image.fromarray(gray_array.astype('uint8'))

# Save the grayscale image
gray_image.save('pathe to save gray image.jpg')
# Create a subplot with two images: the original image and the modified image
fig, axs = plt.subplots(1, 2, figsize=(10, 5))
axs[0].imshow(image_array)
axs[0].set_title('Original Image')
axs[1].imshow(gray_image)
axs[1].set_title('gray Image')
plt.show()
```
