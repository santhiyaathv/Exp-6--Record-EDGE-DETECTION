# -EX-6-Record-EDGE-DETECTION
# Name: SANTHIYA B
# Reg No: 212224230247
# Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1: Import all the necessary modules for the program.

Step2: Load a image using imread() from cv2 module.

Step3: Convert the image to grayscale

Step4: Using Sobel operator from cv2,detect the edges of the image.

Step5: Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM :

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```

# OUTPUT :


## ORIGINAL IMAGE :
<img width="355" height="507" alt="image" src="https://github.com/user-attachments/assets/1b48a9b8-c520-4d0d-88eb-65b05c05916d" />


## SOBEL EDGE DETECTOR:
<img width="381" height="515" alt="image" src="https://github.com/user-attachments/assets/72536360-ba90-4a9e-90fa-3e07ba2edd10" />


## LAPLACIAN EDGE DETECTOR:

<img width="392" height="505" alt="image" src="https://github.com/user-attachments/assets/e03df886-0039-476e-af85-4d52fbf772dc" />


## CANNY EDGE DETECTOR:
<img width="372" height="510" alt="image" src="https://github.com/user-attachments/assets/9ffdcc56-0435-403a-8af0-7155aa963201" />



# RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

