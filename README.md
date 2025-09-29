 # Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Mahalakshmi R
# Register Number: 212223230116

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('img0.jpg')
color_image = cv2.imread('img1.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()      


import numpy as np
gray_image=cv2.imread('img0.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()


import numpy as np
color_image=cv2.imread('img1.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()


import cv2
gray_image = cv2.imread("img0.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:
### Input Grayscale Image and Color Image
<img width="601" height="574" alt="image" src="https://github.com/user-attachments/assets/6be7c0d4-d984-4379-82c9-939ed74d1091" />

<img width="694" height="445" alt="image" src="https://github.com/user-attachments/assets/7d5983bb-09a7-4bde-a095-034f25c1e51e" />

### Histogram of Grayscale Image and any channel of Color Image

<img width="859" height="582" alt="image" src="https://github.com/user-attachments/assets/ef718ae9-082b-4645-8f26-20f395f3db17" />

<img width="1005" height="638" alt="image" src="https://github.com/user-attachments/assets/2f93c197-4ef7-450c-91a8-636c51393346" />

<img width="993" height="431" alt="image" src="https://github.com/user-attachments/assets/405ae2e5-4ba1-434b-a5ac-70078d4e1d3c" />

<img width="1040" height="619" alt="image" src="https://github.com/user-attachments/assets/13821aa4-76ab-448b-8879-cce3430674ee" />


### Histogram Equalization of Grayscale Image.

<img width="599" height="564" alt="image" src="https://github.com/user-attachments/assets/d683d824-1935-47e3-8490-90b42d202801" />



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
