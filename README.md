# Experiment-6
# EDGE-DETECTION
### Developed by: HARISHBALA J
### Register Number: 212224223002
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

### Developed by: HARISHBALA J
### Register Number: 212224223002

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('hasna.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
<img width="706" height="470" alt="image" src="https://github.com/user-attachments/assets/465b58dc-b9ba-438f-ac3f-72872625babd" />
<img width="642" height="462" alt="image" src="https://github.com/user-attachments/assets/facd3137-1791-4f2c-8e27-655e003cb26c" />
<img width="628" height="455" alt="image" src="https://github.com/user-attachments/assets/25782b7e-d766-4e3b-9fe9-67944e7f3832" />
<img width="747" height="464" alt="image" src="https://github.com/user-attachments/assets/bf33cd1f-15c5-4799-89e6-ae7bd12b8a02" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
