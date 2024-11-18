# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

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
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.

### Developed By: SANJEEVI J
### Register Number: 212222110040


## Program & Output:

### i)Read and Display an Image
Load an image from your local directory and display it.
```
import cv2 
image=cv2.imread('boat.jpg',1)
image =cv2.resize(image, (400, 300))
cv2.imshow('WINDOW',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![1](https://github.com/user-attachments/assets/a50e2abd-2c2f-42a0-82eb-039e40bc5201)

### ii)Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("boat.jpg")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![2](https://github.com/user-attachments/assets/bfe26cb0-7cd8-4e02-bdc2-168603621d23)

(2) Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("boat.jpg")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![3](https://github.com/user-attachments/assets/6e39d4d9-7be0-4a71-93c5-337f84f47066)

(3) Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("boat.jpg")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![4](https://github.com/user-attachments/assets/f3541c3a-309b-44e6-bcab-4ce5952f6e6d)

(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("boat.jpg")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![5](https://github.com/user-attachments/assets/9c25500e-e149-4100-ac7e-83567cfc725a)

### iii)Image Color Conversion

(1) Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('boat.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![6](https://github.com/user-attachments/assets/b2a0a396-4f40-4399-9f01-f19646f0bb83)

(2) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('boat.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![7](https://github.com/user-attachments/assets/c33d3005-765f-44a5-af52-ebe62b025664)

(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('boat.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![8](https://github.com/user-attachments/assets/c0be67b0-ac26-4b3f-befc-d221c7239e60)

(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('boat.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![9](https://github.com/user-attachments/assets/c4d7cee4-c945-4398-9368-8afd85efe93c)

### iv)Access and Manipulate Image Pixels

(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```

![10](https://github.com/user-attachments/assets/f70eb357-3baa-4dcd-b7a2-be6632d8ccc7)

(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('boat.jpg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![11](https://github.com/user-attachments/assets/a72d4b54-6d63-4f51-a26d-cb1c873df7ff)

### v)Image Resizing
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![12](https://github.com/user-attachments/assets/3f604663-e4ad-4260-85ed-7f48046110c5)

### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('boat.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![13](https://github.com/user-attachments/assets/5947177e-3169-4611-a4d2-580602b083cb)

### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("boat.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![14](https://github.com/user-attachments/assets/84093752-27ad-44bd-8c41-c5d17a3421a6)

(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("boat.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![15](https://github.com/user-attachments/assets/21702815-47d0-4f33-a393-dfd74c96470f)

### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("boat.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('boat_pic.jpg',img)
```

![16](https://github.com/user-attachments/assets/37a39c04-9a88-4ce0-ad31-2bdb40193c8e)






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







