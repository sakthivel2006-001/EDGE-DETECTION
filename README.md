# EX 6: EDGE-DETECTION
# NAME : SAKTHIVEL S
# REG NO : 212223220090
# Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
Step1:
Import all the necessary modules for the program.

Step2:
Load a image using imread() from cv2 module.

Step3:
Convert the image to grayscale

Step4:
Using Sobel operator from cv2,detect the edges of the image.

Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

# Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

<img width="266" height="411" alt="download" src="https://github.com/user-attachments/assets/1c9d5a33-86a6-4731-a085-4e5384a46f88" />
```
 SOBEL EDGE DETECTOR 
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="266" height="411" alt="download" src="https://github.com/user-attachments/assets/8a45bdd4-b35a-46a4-a80e-e0b4cfdfff2c" />
```
LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="266" height="411" alt="download" src="https://github.com/user-attachments/assets/34714a6d-e5bc-489e-a7ec-ba2366055793" />
```
CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
<img width="266" height="411" alt="download" src="https://github.com/user-attachments/assets/ead0f0b4-d4f7-4898-a4dc-58e10a405136" />


## Output:

# ORIGINAL IMAGE
<img width="632" height="461" alt="image" src="https://github.com/user-attachments/assets/cb1aa65d-8a5e-4256-b227-063f1b147793" />

### SOBEL EDGE DETECTOR

<img width="640" height="476" alt="image" src="https://github.com/user-attachments/assets/79b3cef7-9581-4450-82c9-7f5eabca6607" />

### LAPLACIAN EDGE DETECTOR
<img width="631" height="469" alt="image" src="https://github.com/user-attachments/assets/dfc5af15-9a16-43b7-951b-777efe6507d0" />

### CANNY EDGE DETECTOR
<img width="648" height="458" alt="image" src="https://github.com/user-attachments/assets/7ca65485-f4bd-420e-87a9-aac0cddd7c10" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
