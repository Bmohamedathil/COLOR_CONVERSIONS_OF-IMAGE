## Developed By : MOHAMED ATHIL B
## Register No : 212222230081
## Exp No : 01

#  COLOR_CONVERSIONS_OF-IMAGE

## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:BALAJI J
### Register Number: 212221243001




### i) Read and display the image
```
import cv2
image=cv2.imread('vn.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('window',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output:

![306840043-461a3195-31ca-4774-93b6-b644001f14d3](https://github.com/user-attachments/assets/7839e6d7-690a-419b-84c9-1d33a0d4f233)

### ii)Write the image
```
import cv2
image=cv2.imread('vn.jpg',0)
image=cv2.resize(image,(400,300))
cv2.imwrite('new1.png',image)
```
## output:

![306840803-5eae6982-d795-4697-bc1a-6d38bf0b1e39](https://github.com/user-attachments/assets/6e022e05-de1e-4691-b5a6-b97ef8866952)


### iii)Shape of the Image
```
import cv2
image=cv2.imread('vn.jpg',1)
print(image.shape)
```
## output:

![306841192-900b715a-9043-4cf1-8aba-95c2bd02c339](https://github.com/user-attachments/assets/d94687fa-7002-43fb-a6d2-ba60566e45aa)



### iv)Access rows and columns
```
import random
import cv2
image=cv2.imread('vn.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)] 
cv2.imshow('WINDOW2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output

![306840995-399d4529-1d2a-44d6-ad7e-76b9aed483b6](https://github.com/user-attachments/assets/0635c1d8-085c-4ee3-86e4-c46683fd8e0c)



### v)Cut and paste portion of image
```
import cv2
image=cv2.imread('vn.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('WINDOW3',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output:

![306841319-d610ce3f-34b6-4043-bba0-933152216d1e](https://github.com/user-attachments/assets/1b047f12-39d2-4b97-9050-272e264a3735)




### vi) BGR and RGB to HSV and GRAY
``````
import cv2
img = cv2.imread('vn.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
``````
## output

![306842172-f8065f80-69d0-477f-9acb-4ea72b0de4a8](https://github.com/user-attachments/assets/906bfa37-d3d4-4b00-8119-e6e6a2d4a353)




### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('vn.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output

![306842856-69b6555f-3f87-4e3b-ba0a-439950caf5f5](https://github.com/user-attachments/assets/86d951e1-0bcf-44bf-97ed-ac7ec2e1e48e)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('vn.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output:

![306843961-049f2621-5752-40a8-87f7-881e9e5e22da](https://github.com/user-attachments/assets/8db1bb47-fa58-4b74-97e4-8123188a4c87)


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('vn.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output:



![306856358-14a25ccd-7480-4e9c-ac4d-ed0176cfdcb5](https://github.com/user-attachments/assets/88d36394-2051-400a-8a02-e52f7209e038)


### x) Split and merge HSV Image

```

import cv2
img = cv2.imread("vn.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
````
## output:

![306856928-cbc62796-f40c-4a62-8ef4-61088894c10f](https://github.com/user-attachments/assets/4760c485-088a-4a75-a3fb-fb41c4a18fe4)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







