# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program

### Developed By:Sharangini T K
### Register No.: 212222230143
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Read the image
image = cv2.imread('cute.jpeg')
# Convert to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Display the original grayscale image
plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()
```
![WhatsApp Image 2024-10-15 at 6 42 25 PM](https://github.com/user-attachments/assets/945cf298-962a-4218-a148-787f77d4f348)

# Global thresholding
```
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

# Display the global thresholding result
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()
```
![WhatsApp Image 2024-10-15 at 6 42 25 PM (1)](https://github.com/user-attachments/assets/2f71f643-04b9-47ab-bbe1-4c46766433eb)

# Adaptive thresholding (Gaussian)
```
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY, 11, 2)
# Display the adaptive thresholding result
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()
```
![WhatsApp Image 2024-10-15 at 6 42 25 PM (2)](https://github.com/user-attachments/assets/10718e55-e0c2-4d31-8583-b1740fb184ce)

# Otsu's thresholding
```
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
# Display the Otsu thresholding result
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()
```
![WhatsApp Image 2024-10-15 at 6 42 25 PM (3)](https://github.com/user-attachments/assets/8508176e-6d3b-40df-b283-041e65a82eb3)

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
