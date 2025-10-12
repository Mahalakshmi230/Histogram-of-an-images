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

### Developed By: Mahalakshmi R
### Register Number: 212223230116

```
import cv2
from matplotlib import pyplot as plt
#Load the color image
image = cv2.imread('eagle.jpeg')
#Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

```
## Output:
### Input Grayscale Image and Color Image
<img width="510" height="365" alt="Screenshot 2025-10-12 230748" src="https://github.com/user-attachments/assets/2be14674-3717-4586-b727-e8d0593cefed" />

### Histogram of Grayscale Image
<img width="613" height="449" alt="Screenshot 2025-10-12 230801" src="https://github.com/user-attachments/assets/990857c2-e99d-4eb8-8b60-a5e45e5bbeb0" />

### Histogram Equalization of Grayscale Image
<img width="541" height="378" alt="Screenshot 2025-10-12 230808" src="https://github.com/user-attachments/assets/9743d393-f302-435b-bb28-51cf302dcc13" />

### Equalized Histogram
<img width="704" height="445" alt="Screenshot 2025-10-12 230814" src="https://github.com/user-attachments/assets/ada8efa5-f579-43ca-8e9b-12bcfa1eb9df" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
