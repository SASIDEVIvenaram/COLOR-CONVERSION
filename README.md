# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.
## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2.
### Step2:
Read the image file.
### Step3:
Store the converted color in a variable.
### Step4:
Display the color converted image windows.
### Step5:
Destory and close the windows
## Program:
```
Developed By: SASIDEVI V
Register Number: 212222230136
```
# i) Convert BGR and RGB to HSV and GRAY

```
import cv2
image= cv2.imread('fly.jpg')
cv2.imshow('ORIGINAL IMAGE',image)
hsv_image = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)

cv2.imshow('BGR2HSV',hsv_image)
hsvImage1=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)

cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
Output:


![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/5f350f4e-5034-40a3-94ae-f98d8a9fd079)

![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/18b7ab37-27d6-489e-9bb8-98ebf1e2c541)

![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/95f2ab63-dae6-424d-8b71-bbcf7cfcaba6)

# ii)Convert HSV to RGB and BGR
```

import cv2
image=cv2.imread('fly.jpg')
image=cv2.resize(image,(300,200))

image=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',image)

RGB = cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
Output:

![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/db7a79d3-e5d1-494d-88f3-0d3af6ba636b)

# iii)Convert RGB and BGR to YCrCb
```
import cv2
image=cv2.imread('fly.jpg')
image=cv2.resize(image,(300,200))
cv2.imshow('Original RGB Image',image)

YCrCb1 = cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
Output:
![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/937626a5-b06a-4d35-b3b1-6c6c4fe6636f)

# iv)Split and Merge RGB Image
```
import cv2
image=cv2.imread('fly.jpg',1)
image=cv2.resize(image,(300,200))

R=image[:,:,2]
G=image[:,:,1]
B=image[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged=cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

Output:
![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/c071657a-c73b-4f26-9e85-00d89a0723c9)

# v) Split and merge HSV Image

```
import cv2
image=cv2.imread("fly.jpg",1)
image= cv2.resize(image,(300,200))
image=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(image)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
Output:
![image](https://github.com/SASIDEVIvenaram/COLOR-CONVERSION/assets/118707332/1569e3ef-a682-4c54-b8db-8cb7e2636d95)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
