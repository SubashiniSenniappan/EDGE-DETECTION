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
DEVELOPED BY: SUBASHINI
REGISTER NUMBER: 212222240106
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("$$$.jpg",0)
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
### ORIGINAL IMAGE:

![$$$](https://github.com/user-attachments/assets/210e5dd4-b606-4d62-bccb-f39c528d9bcd)


### SOBEL EDGE DETECTOR

![download (5)](https://github.com/user-attachments/assets/dfd8396b-91fc-489e-bfb5-a732c7002840)


![download](https://github.com/user-attachments/assets/e053685e-8eaf-46fc-8e4f-14cf5dc24b02)

![download (1)](https://github.com/user-attachments/assets/794f0683-638e-4f31-ad52-022afd862c4f)

### LAPLACIAN EDGE DETECTOR


![download (2)](https://github.com/user-attachments/assets/262f4c08-10c5-48d5-9835-ff051e35d866)



### CANNY EDGE DETECTOR


![download (3)](https://github.com/user-attachments/assets/9e5eca97-a902-413b-a7f8-cff4252e158f)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
