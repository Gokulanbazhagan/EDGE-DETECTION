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

## PROGRAM :
### DEVELOPED BY : GOKULARAMANAN K
### REGISTER NO : 212222230040
### Convert image to grayscale and remove noise
```P
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("ani.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```p
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y AXIS :**
```p
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY AXIS :**
```p
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```p
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```p
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR


### SOBEL X AXIS :

![Screenshot 2024-04-02 114316](https://github.com/Gokul-008/EDGE-DETECTION/assets/121165996/b5762cf9-cf2e-4330-950d-7cb7989f6d11)





### SOBEL Y AXIS :

![Screenshot 2024-04-02 114347](https://github.com/Gokul-008/EDGE-DETECTION/assets/121165996/d0997687-3f6d-485c-894b-4c191e2a54d7)




### SOBEL XY AXIS :


![Screenshot 2024-04-02 114408](https://github.com/Gokul-008/EDGE-DETECTION/assets/121165996/3e3335bf-eff6-4ed9-8d10-92f7dc5d8ffe)



### LAPLACIAN EDGE DETECTOR :

![Screenshot 2024-04-02 114423](https://github.com/Gokul-008/EDGE-DETECTION/assets/121165996/1aaf77d8-d316-448c-a6d1-dd3455df24e5)



### CANNY EDGE DETECTOR :
![Screenshot 2024-04-02 114440](https://github.com/Gokul-008/EDGE-DETECTION/assets/121165996/0e16e82e-edf1-4e22-b9eb-84234326268c)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
