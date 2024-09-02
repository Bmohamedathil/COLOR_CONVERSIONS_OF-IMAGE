# COLOR_CONVERSIONS_OF-IMAGE
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
### Developed By: MOHAMED ATHIL B
### Register Number: 212222230081


## Output:

### i) Read and display the image
```py
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:


![Screenshot 2024-02-22 092247](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/0eb621aa-2159-478d-a410-602ddb5e8251)

### ii)Write the image
```py
    import cv2
    image=cv2.imread('images.jpg',0)
    cv2.imwrite('natural.jpg',image)
```
## Output:

![write the image](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/9d717855-bb9d-41e6-916f-ac3205453f25)

### iii)Shape of the Image
```py
    import cv2
    image=cv2.imread('images.jpg',1)
    print(image.shape)
```
## Output:
![shape the image](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/46902cb3-9d2f-4729-98a7-b9e04fc95ca2)

### iv)Access rows and columns
```py
    import random
    import cv2
    image=cv2.imread('images.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('natural',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![access row and column](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/701c00d5-76d0-4a10-a74f-0ba58420a05a)



### v)Cut and paste portion of image
```py
   import cv2
   image=cv2.imread('images.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('natural',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output:
![cut and paste](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/2d007fda-b32b-4d5f-a042-e1f685651395)


### vi) BGR and RGB to HSV and GRAY
```py
import cv2
img = cv2.imread('images.jpg',1)
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
```
## Output:
![Screenshot 2024-02-22 093231](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/4bd1f54d-36e3-4278-afc6-1f60481e10e0)
![Screenshot 2024-02-22 093107](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/0f5e1f37-6217-4248-bdc1-810937b1a6a3)
![Screenshot 2024-02-22 093131](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/fd2452ac-baed-4ed9-8be3-c9045450ee59)
![Screenshot 2024-02-22 093145](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/a7e6d7e5-5e1f-4ec2-b794-01536c0e1a22)

![Screenshot 2024-02-22 093248](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/a58b623e-bf2d-46be-be6d-1c0d8e0911a0)

### vii) HSV to RGB and BGR
```py
import cv2
img = cv2.imread('images.jpg')
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
## Output:
![Screenshot 2024-02-22 093423](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/cfe68694-7e42-42f6-80f4-74527dcd997c)
![Screenshot 2024-02-22 093432](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/b113c1bd-c1ae-4206-b6c5-3bcf106255f5)
![Screenshot 2024-02-22 093440](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/94cf556b-5ce2-4c7e-94e3-7977fc944ad0)




### viii) RGB and BGR to YCrCb
```py
import cv2
img = cv2.imread('images.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-22 093752](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/d54056a6-12fa-4d52-b7fe-9880b7062b73)
![Screenshot 2024-02-22 093759](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/51f1c2dd-8728-4787-a73e-b179843ef075)
![Screenshot 2024-02-22 093811](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/a329b99d-058c-4588-b48d-a904500c7937)





### ix) Split and merge RGB Image
```py
import cv2
img = cv2.imread('images.jpg',1)
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
## Output:
![Screenshot 2024-02-22 094211](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/e1fac2e4-dc15-45f3-98b5-81c65311f33e)
![Screenshot 2024-02-22 094218](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/77a67c0d-8c8e-412a-b7be-5adfb8d8fc17)
![Screenshot 2024-02-22 094225](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/551cf5f6-4ea8-46aa-8e5c-5d60898a73e9)

![Screenshot 2024-02-22 094232](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/0195593d-990e-4ec5-8a59-16d3973df9e0)





### x) Split and merge HSV Image
```py
import cv2
img = cv2.imread("images.jpg",1)
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
```
## Output:
![Screenshot 2024-02-22 094042](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/06d3fe79-5611-494f-be36-7cf48571e65f)
![Screenshot 2024-02-22 094049](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/f2465292-5dc6-4cef-bd2e-f3afa674dddc)
![Screenshot 2024-02-22 094056](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/7d5f6dd9-d3a9-4864-9033-973284ce34ae)
![Screenshot 2024-02-22 094104](https://github.com/AdhithyaMR/COLOR_CONVERSIONS_OF-IMAGE/assets/118834761/608846e6-397f-4ee4-aaa8-16f83f53c916)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
