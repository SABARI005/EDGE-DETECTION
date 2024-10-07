# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

### Developed by: SABARI S
### Register no: 212222240085

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Load the image
```
image = cv2.imread('deadpool.png')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## Output:

![{781A6746-7B8B-4093-9335-FCB0F046F3F9}](https://github.com/user-attachments/assets/71bfe289-4b78-4c3c-9271-8cbc4f836b81)

### SOBEL EDGE DETECTOR
```
# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## Output:


![{520CDE76-3F3D-47B4-9DBD-D9389D3D2EF8}](https://github.com/user-attachments/assets/55b2440b-9d41-44df-90de-bb3519ce6013)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

```
## Output:

![{9F04FD2F-C9B8-49C0-86AC-C7E3BA8D95A4}](https://github.com/user-attachments/assets/7843d7e8-0830-44b7-a37c-d7b7f4aacd12)

### CANNY EDGE DETECTOR
```
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
![{FCE17E25-02BC-47F0-8378-470ECBD8F6D8}](https://github.com/user-attachments/assets/735c73ca-b0dd-4a0f-8bf6-1370e396671b)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
