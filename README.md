# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required


### Step2:
Convert the input image to gray , to get more details and for laplcian operator, we have to convert input 
image to bgr format

### Step3:
Apply smoothing to reduce noise, here we are using gaussian blur

### Step4:
Perform the edge detector operation


### Step5:
Show to detected image

 
## Program:
```
Developed By: Nithishkumar P
Register No: 212221230070
```

``` Python
# Import the packages
import cv2

# Load the image, Convert to grayscale and remove noise
i=cv2.imread('build.jpg',-1)
gray=cv2.cvtColor(i,cv2.COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)


# SOBEL EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
sobel_x=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
cv2.imshow('sobel_x',sobel_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_y=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
cv2.imshow('sobel_y',sobel_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_xy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('sobel_xy',sobel_xy)
cv2.waitKey(0)
cv2.destroyAllWindows()


# LAPLACIAN EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
rgb_image = cv2.cvtColor(i,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(rgb_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()


# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(img, 120, 150)
cv2.imshow('canny',canny_edges)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/d579e907-fa2c-4899-a8f0-362e3fb99d05)

![image](https://github.com/user-attachments/assets/acc4700c-cb4a-43c8-b8b1-154fd66293be)

![image](https://github.com/user-attachments/assets/f8cf8e7f-3f2a-44da-b1e3-e6b3a2fc7ab2)




### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/fd965475-9e2a-43c3-888e-319bff0433ea)



### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/b444f3a9-df84-4301-9175-b8d0149da7f4)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
