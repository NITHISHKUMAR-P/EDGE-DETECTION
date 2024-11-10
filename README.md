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
i=cv2.imread('land.jpeg',-1)
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
![Screenshot (835)](https://github.com/JEEVAABI/EDGEDETECTION/assets/93427098/bc95f9aa-0e48-4b9b-9797-ef37aff32e6b)
![Screenshot (834)](https://github.com/JEEVAABI/EDGEDETECTION/assets/93427098/dce2a796-9ef1-4b82-bf93-7d7c748d1f9f)
![Screenshot (833)](https://github.com/JEEVAABI/EDGEDETECTION/assets/93427098/05b6d66f-eb1d-4c4b-9a79-c07e63e60a99)



### LAPLACIAN EDGE DETECTOR
![Screenshot (836)](https://github.com/JEEVAABI/EDGEDETECTION/assets/93427098/5b9479a2-264a-4cd8-be92-72ddd3b07667)



### CANNY EDGE DETECTOR
![Screenshot (837)](https://github.com/JEEVAABI/EDGEDETECTION/assets/93427098/3b5142d1-910c-4248-8aa4-8f36bd5439c1)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
