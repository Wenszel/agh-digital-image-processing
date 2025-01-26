<h1 align="center"> Digital Image Processing - AGH Course 2024/2025 </h1>

<p align="center">
  <img src="/readme-images/mandril.png" />
</p>

## Lab 1 - Intro to OpenCV
Basic operations on images: reading, displaying with different color models 
</br> 

[Notebook](01_intro.ipynb)

## Lab 2 - Pixel-wise operations
- LUT operations - look-up table is a table that maps each pixel value to a new value 
- Logical operations on images 
- Arithmetic operations on images 
</br> 
This image shows the result of adding two images together:

![SumExample](/readme-images/sum-example.png)

[Notebook](02_point.ipynb)

## Lab 3 - Histogram
- Normalization  - method to scale the pixel values to the full possible range (0-255)
- Histogram equalization - method to improve the contrast of an image by stretching the histogram to fill the entire intensity range
- CLAHE - a variant of histogram equalization that limits the contrast amplification in the local areas of the image. In other words, it enhances the contrast without making noise or small details too bright in certain areas
</br> 

This image shows the result of applying histogram equalization on an image to improve the contrast:
![HistogramExample](/readme-images/equalization-example.png)

[Notebook](03_histogram.ipynb)

## Lab 4 - Threadsholding
Thresholding is a method to segment an image into two parts: the foreground and the background. The threshold value is a value that separates the two parts.

- Based on a histogram - algorithm found the best threshold value based on the shape of the histogram
- Otsu - is a method that automatically determines the best threshold value to separate an image into two classes: foreground and background. In other words, it finds the value that minimizes the combined variance of these two classes, making the image as distinct as possible between the two regions.
- Adaptive - method that calculates the threshold value for each pixel based on the local neighborhood of the pixel
</br> 
This image shows the result of applying thresholding on an image to segment the foreground and background:

![ThresholdingExample](/readme-images/thresholding-example.png)

[Notebook](04_thresholding.ipynb)

## Lab 5 - Image interpolation, Resolution
Interpolation is a method to increase the resolution of an image by adding new pixels, between the existing ones.
Examples of interpolation methods:
- Nearest neighbour - assigns the value of the nearest pixel to the new pixel
- Bilinear - method that calculates the value of the new pixel based on the weighted average of the four nearest pixels
- Bicubic - method that calculates the value of the new pixel based on the weighted average of the sixteen nearest pixels
</br>

[Notebook](05_resolution.ipynb)

## Lab 6 - Image filtering
Image filtering is used to remove noise, blur the image, or detect edges. It is done by applying a convolution operation on the image with a kernel. The kernel is a small matrix that is applied to each pixel of the image. 
Examples of filters:
- Low-pass filters: gaussian, median, averaging
- High-pass filters: laplacian, sobel, prewitt, roberts
</br> 
This image shows the result of applying a median filter on an image to remove noise:

![MedianFilterExample](/readme-images/median-filter-example.png)

[Notebook](06_context.ipynb)

## Lab 7 - Mathematical morphology
Mathematical morphology is a method to process images based on the shape of the objects in the image. It is used to remove noise, detect edges, or segment objects in the image.
- Erosion - method that shrinks the objects in the image by removing the pixels on the object's boundary
- Dilation - method that expands the objects in the image by adding pixels to the object's boundary
- Opening - method that removes small objects in the image by applying erosion followed by dilation
- Closing - method that removes small holes in the objects in the image by applying dilation followed by erosion
- Hit-or-miss - method that detects objects in the image based on the shape of the object
- Morphological reconstruction - method that removes small objects in the image by applying dilation followed by erosion
</br> 

This image shows the result of applying erosion and dilation on an image to remove noise:
![Example](/readme-images/erosion-dilation-example.png)

[Notebook](10_morphology.ipynb)