# EX-6 EDGE-DETECTION
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
## PROGRAM:
```
DEVELOPED BY: JANARTHANAN V K
REGISTER NUMBER: 212222230051
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
<img src="https://github.com/Janarthanan2/DIP_EX06_EDGE-DETECTION/assets/119393515/1fe3a58a-55a5-4df9-bfc2-1c7d07b95d61" width=50%>

### SOBEL EDGE DETECTOR:
<img src="https://github.com/Janarthanan2/DIP_EX06_EDGE-DETECTION/assets/119393515/1ff1508c-2883-407a-b125-7a49b89686b0">
<img src="https://github.com/Janarthanan2/DIP_EX06_EDGE-DETECTION/assets/119393515/5b9de407-defe-4822-8e8a-577586e71f84">
<img src="https://github.com/Janarthanan2/DIP_EX06_EDGE-DETECTION/assets/119393515/a46da7d5-1c90-47fb-809c-4731946503c7">

### LAPLACIAN EDGE DETECTOR
<img src="https://github.com/Janarthanan2/DIP_EX06_EDGE-DETECTION/assets/119393515/1c2c80f0-b5fd-46c1-a1a8-b89971d8efda">

### CANNY EDGE DETECTOR
<img src="https://github.com/Janarthanan2/DIP_EX06_EDGE-DETECTION/assets/119393515/2c05b677-9bf7-4f80-9118-9342ef8f9b3e">

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
