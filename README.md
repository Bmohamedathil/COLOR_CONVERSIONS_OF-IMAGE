# COLOR_CONVERSIONS_OF-IMAGE->
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
1.Load an image from your local directory and display it.
### Step2:
1.Draw a line from the top-left to the bottom-right of the image.

2.Draw a circle at the center of the image.

3.Draw a rectangle around a specific region of interest in the image.

4.Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.Convert the image from RGB to HSV and display it.

2.Convert the image from RGB to GRAY and display it.

3.Convert the image from RGB to YCrCb and display it.

4.Convert the HSV image back to RGB and display it.

### Step4:
1.Access and print the value of the pixel at coordinates (100, 100).

2.Modify the color of the pixel at (200, 200) to white.

### Step5:
1.Resize the original image to half its size and display it.
### Step6:
1.Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.Flip the original image horizontally and display it.

2.Flip the original image vertically and display it.

### Step8:
1.Save the final modified image to your local directory.


## Program:
### Developed By: MOHAMED ATHIL B
### Register Number: 212222230081

### i)Read and Display an Image
```
import cv2
img=cv2.imread('ajith.jpg',1)
cv2.imshow('Image Window', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/69215035-2899-4bfe-a80a-b6729bccb333)





### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res = cv2.line(image, (0, 0), (440,591), (200, 100, 205), 10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/60a2d339-b14f-49bb-9dc4-a61ababac76a)



(2) Draw a circle at the center of the image.
```
import matplotlib.pyplot as plt
img = cv2.imread("ajith.jpg")
img.shape
resimg=cv2.circle(img_resiz,(200,200),100,(200,0,0),10)
resimg_rgb =cv2.cvtColor(resimg, cv2.COLOR_BGR2RGB)
plt.imshow(resimg_rgb)
plt.show()

```
### Output
![image](https://github.com/user-attachments/assets/11c1a70f-3f78-456f-b0d1-881b054763c6)



(3) Draw a rectangle around a specific region of interest in the image.
```
import cv2
img = cv2.imread("ajith.jpg")
res_img=cv2.rectangle(img,(0,0),(400,400),(100,255,100),10)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/df10f9b7-a7e5-4659-8e32-e7d80334d704)



(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")

image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
res = cv2.putText(image,"AJITH", (5,150), font,1.5, (0, 0, 0),5)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/b7be1c9d-d824-441c-9216-9e2c530c2345)


### iii)Image Color Conversion
1) Convert the image from RGB to HSV and display it
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
hsv2 = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
plt.imshow(hsv2)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/564248cf-a96b-4363-9807-6969a2a8c6b6)


(2) Convert the image from RGB to GRAY and display it.
```
mg = cv2.imread('ajith.jpg',1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output

![Screenshot 2024-09-30 090117](https://github.com/user-attachments/assets/3360ef28-db96-4687-a8e9-6cedd609d058)



3) Convert the image from RGB to YCrCb and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
YCrCb1 = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
plt.imshow(YCrCb1)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/75a53c5b-a224-49e3-9ba7-ecc7160131c0)



(4) Convert the HSV image back to RGB and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
BGR = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(BGR)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/9dddbe3b-44fd-4d1f-a1d8-43573af1b5a5)


### iv)Access and Manipulate Image Pixels
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
image = cv2.resize(image,(400,400))
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
image[199, 199] = [255, 255, 255]
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/98411a2d-a6ff-4eaf-ae84-d351ffd5c962)

### v)Image Resizing
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
resized_img = cv2.resize(image, (900, 1000))
plt.imshow(resized_img)
plt.axis('off')
plt.show()
```
### Output
![image](https://github.com/user-attachments/assets/e2b708f5-afef-4dd9-9c82-11b4bfcc3699)



### vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
roi = image[50:50 + 425, 50:50 + 425]
plt.imshow(roi)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/39bd75a1-35f9-401e-be63-980e7b2b1349)


### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
image = cv2.resize(image,(400,400))
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res=cv2.rotate(image,cv2.ROTATE_180)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/110fe1ee-03f9-4762-93cb-afc8a5c8fb0f)


(2) Flip the original image vertically and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("ajith.jpg")
image = cv2.resize(image,(400,400))
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output

![image](https://github.com/user-attachments/assets/322d94e2-0651-46c4-96dc-51b9002bb1bf)


### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("ajith.jpg")
cv2.imwrite('ajith.jpg',img)
```
### Output

![image](https://github.com/user-attachments/assets/f3580ffc-df8e-4170-90c0-dfdfcee14ee7)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







