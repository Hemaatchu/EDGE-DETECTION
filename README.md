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

### SOBEL EDGE DETECTOR
```
## Name: Hemavathy S
## Reg No: 212223230076
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('D:\\DIPT\\tiger.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

<img width="815" height="523" alt="image" src="https://github.com/user-attachments/assets/4b66e104-545a-4661-a74b-2ab06563a135" />

```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

<img width="902" height="513" alt="image" src="https://github.com/user-attachments/assets/88421e54-5a0e-4018-b1e2-b1155d39bdcb" />

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

<img width="771" height="531" alt="image" src="https://github.com/user-attachments/assets/7048b913-a8d8-48bf-b724-9cd903550866" />

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off') 
```

<img width="798" height="525" alt="image" src="https://github.com/user-attachments/assets/0cbc6910-535f-497f-9958-6d7c284505ce" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
