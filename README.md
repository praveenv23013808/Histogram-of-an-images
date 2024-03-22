# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Read the gray and color image using imread()

## Step2:
Print the image using imshow().

## Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## Step5:
The Histogram of gray scale image and color image is shown.

## Program:
# Developed By: praveen v
# Register Number: 212222233004
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat1.jpg")
color_image = cv2.imread("cat2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
import numpy as np
import cv2
Gray_image = cv2.imread("cat1.jpg")
Color_image = cv2.imread("cat2.jpg")
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
```
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```
import cv2
gray_image = cv2.imread("cat1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/praveenv23013808/Histogram-of-an-images/assets/145824728/98d5654d-61b1-408c-8cf3-ca57a5afcd7c)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/praveenv23013808/Histogram-of-an-images/assets/145824728/08671aec-c02d-401d-90f3-b9dd04fb0263)
![image](https://github.com/praveenv23013808/Histogram-of-an-images/assets/145824728/fc2dc84c-bf0d-46f4-9102-ac0b9b2670fa)




### Histogram Equalization of Grayscale Image.

![image](https://github.com/praveenv23013808/Histogram-of-an-images/assets/145824728/9b5203cf-5b50-43e4-b244-d383ff795c73)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
