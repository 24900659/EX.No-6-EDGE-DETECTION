# EX.No-6-EDGE-DETECTION
Edge-detection-opencv

Aim
To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

Software Required

Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib

⚙️ Algorithm
Step 1:
Import all the necessary modules for the program.

Step 2:
Load an image using cv2.imread().

Step 3:
Convert the image to grayscale.

Step 4:
Apply Sobel operator using OpenCV to detect edges.

Step 5:
Apply Prewitt operator using custom kernels.

Step 6:
Apply Roberts operator using custom kernels.

Step 7:
Apply Laplacian operator using OpenCV.

Step 8:
Apply Canny edge detector using OpenCV.

Step 9:
Display all edge-detected images for comparison.

Developed By

Name: MOHANA K.V.S.L

Register No: 212224240093

PROGRAM:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('monaa.jpeg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
Sobel edge detection
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)
sobel_combined = cv2.magnitude(sobel_x, sobel_y)

plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
laplace edge detection
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
canny edge detection
```
canny_edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
Output

<img width="371" height="507" alt="image" src="https://github.com/user-attachments/assets/102f853b-5737-433e-978e-6b8e05ba7d45" />

<img width="363" height="501" alt="image" src="https://github.com/user-attachments/assets/a6c6f75b-1162-4911-b768-9dcb1df2518c" />

<img width="392" height="505" alt="image" src="https://github.com/user-attachments/assets/fdb8050e-f5f6-475e-bcf3-4c86c373ab98" />

<img width="387" height="500" alt="image" src="https://github.com/user-attachments/assets/fd6f0560-3183-40a3-8f14-f87a9cf80726" />



Result
Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.

