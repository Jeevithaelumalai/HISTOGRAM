# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

## Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

## Step3:
Display the histograms with their respective images.

## Step4:
Equalize the grayscale image.

## Step5:
Display the grayscale image.

## Program:
# Developed By:JEEVITHA
# Register Number:212222230054
```
import cv2
import matplotlib.pyplot as plt
```
# Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cha.jpeg")
color_image = cv2.imread("ch.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("cha.jpeg")
Color_image = cv2.imread("ch.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Write the code to perform histogram equalization of the image. 
```
import cv2
gray_image = cv2.imread("cha.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output:
### Input Grayscale Image and Color Image
![WhatsApp Image 2023-09-13 at 16 02 41](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/c0722be4-be2c-4350-a1c9-57ca5b9339e2)
![WhatsApp Image 2023-09-13 at 16 03 02](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/61722ef9-2036-41c8-beda-9dc93baa2e2f)


### Histogram of Grayscale Image and any channel of Color Image
![WhatsApp Image 2023-09-13 at 16 03 25](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/3bad76d7-f7d1-44bf-896a-9edae7cf9c1a)
![WhatsApp Image 2023-09-13 at 16 03 43](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/74c6b170-e3da-4a56-a6b2-294ccf02e733)
![WhatsApp Image 2023-09-13 at 16 04 03](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/b9484f5f-8bbb-4b13-b154-e51e2f3baede)
![WhatsApp Image 2023-09-13 at 16 04 50](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/9b9f887d-753e-42f3-9937-9e7c6eac061d)


### Histogram Equalization of Grayscale Image

![WhatsApp Image 2023-09-13 at 16 05 09](https://github.com/Jeevithaelumalai/HISTOGRAM/assets/118708245/8b98da19-8ec5-4312-b03d-15b17e0eaca2)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
