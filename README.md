# COLOR_CONVERSIONS_OF-IMAGE
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
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### DEVOLOPED BY: NAVEEN.S
### REGISTER NUMBER: 212223240106


## Output:

### i)Read and Display an Image
```
import matplotlib.pyplot as plt
import cv2
img=cv2.imread('actor.jpg')
plt.imshow(img)
plt.show()
```
![image](https://github.com/user-attachments/assets/bb0b1dd6-f593-4d45-b012-6aecc625b736)


### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
res=cv2.line(img,(0,0),(600,400),(205,100,250),10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/28a9b0dc-1c8d-4588-8491-3a9e7a861903)




2) Draw a circle at the center of the image.
```
imc=cv2.imread('actor.jpg')
resc=cv2.circle(imc,(250,250),100,(250,195,280),15)
plt.imshow(resc)
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/437842e3-592f-4ef1-b8db-f8f73e3d14e5)





3.Draw a rectangle around a specific region of interest in the image.
```
imr=cv2.imread('actor.jpg')
start=(50,50)
stop=(300,300)
color=(250,250,200)
thick=15
resr=cv2.rectangle(imr,start,stop,color,thick)
plt.imshow(resr)
plt.show()
```
![image](https://github.com/user-attachments/assets/51bd38d9-e9a7-4a7b-9e89-013fccf595cd)



4. Add the text "OpenCV Drawing" at the top-left corner of the image.
```
imt = cv2.imread("actor.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
font_scale = 1
color = (150, 155, 255) 
thickness = 3
rest = cv2.putText(imt, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
plt.imshow(rest)
plt.show()

```
![image](https://github.com/user-attachments/assets/6f3c10b5-bd9c-4cbd-8390-956fb7357c9c)




### iii)Image Color Conversion
1. Convert the image from RGB to HSV and display it
```
image=cv2.imread("actor.jpg")
imhsv=cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
plt.imshow(imhsv)
plt.show()
```
![image](https://github.com/user-attachments/assets/c0936b9a-5127-425c-bd03-c89f5f1c6d6b)

2. Convert the image from RGB to GRAY and display it.

```
image1=cv2.imread("actor.jpg",0)
imgs=cv2.cvtColor(image1, 0)
plt.imshow(imgs)
plt.show()
```
![image](https://github.com/user-attachments/assets/0d475919-92d6-40cc-8a18-177d2708edb9)




3. Convert the image from RGB to YCrCb and display it.
```
imrgb=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(imrgb)
plt.show()
```
![image](https://github.com/user-attachments/assets/d828b533-663b-47ac-bdfb-69c55add79b0)



### iv)Access and Manipulate Image Pixels
1. Access and print the value of the pixel at coordinates (100, 100)
```
im2=cv2.imread('actor.jpg')
p=im2[100,100]

```
![image](https://github.com/user-attachments/assets/2c110e5e-d584-435f-9ed5-2717087ca395)


2. Modify the color of the pixel at (200, 200) to white.
```
imaw=cv2.imread("actor.jpg")
for i in range(100,250):
    for j in range(100,250):
        imaw[i,j]=225
plt.imshow(imaw,cmap="gray")
plt.show()
```
![image](https://github.com/user-attachments/assets/cbe58bde-9061-4c6e-b5d6-7020124e2a17)



### v)Image Resizing
Resize the original image to half its size and display it.
```
ime=cv2.imread('actor.jpg')
ime.shape
```
![image](https://github.com/user-attachments/assets/77d910b8-5470-4433-9b07-4d978e449d09)

```
image_resize=cv2.resize(ime,(150,150))
image_resize.shape
```



2. Flip the original image vertically and display it.
```
imageve = cv2.imread("actor.jpg")
resve=cv2.rotate(imageve,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(resve)
plt.show()
```
d2)
  ![image](https://github.com/user-attachments/assets/48bc9ad2-fbb3-4f06-a086-ac25fdc921ad)



### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
cv2.imwrite('Saved.jpg',resve)
```
![image](https://github.com/user-attachments/assets/11ba08ea-1e42-4312-bd70-3ab32130e989)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.

