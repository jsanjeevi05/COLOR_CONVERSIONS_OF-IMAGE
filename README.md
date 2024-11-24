# COLOR CONVERSIONS OF IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing.

vi) Image Cropping.

vii) Image Flipping.

viii)	Write and Save the Modified Image.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.<br>
o	Draw a circle at the center of the image.<br>
o	Draw a rectangle around a specific region of interest in the image.<br>
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.<br>
o	Convert the image from RGB to GRAY and display it.<br>
o	Convert the image from RGB to YCrCb and display it.<br>
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).<br>
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.

### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.<br>
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


## Program:
```py
#Developed By: SANJEEVI J
#Register Number: 212222110040

#1.Read and Display an Image:
import cv2
image = cv2.imread('img.jpg')
cv2.imshow('Loaded Image', image)
cv2.waitKey(0)
cv2.destroyAllWindows()

#2a.Draw a line from the top-left to the bottom-right of the image
start=(0,0)
end=(1370,780)
color = (255, 0, 0)
thickness = 5 
diagonal= cv2.line(image, start, end, color, thickness)
cv2.imshow('Diagonal Line', diagonal)
cv2.waitKey(0)
cv2.destroyAllWindows()

#2b.Draw a circle at the center of the image
center = (480, 270)
radius = 100
color = (0, 255, 0)
thickness = 5
circle=cv2.circle(image, center, radius, color, thickness)
cv2.imshow('Center Circle', circle)
cv2.waitKey(0)
cv2.destroyAllWindows()

#2c.Draw a rectangle around a specific region of interest in the image
start=(5,5)
end=(1365,780)
color = (0, 255, 0)
thickness = 5 
rectangle=cv2.rectangle(image, start, end, color, thickness)
cv2.imshow('rectangle',rectangle)
cv2.waitKey(0)
cv2.destroyAllWindows()


#2d.Add the text "OpenCV Drawing" at the top-left corner of the image
text = "OpenCV"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 2
color = (255, 255, 255)
thickness = 3
opencv=cv2.putText(opencv, text, position, font, font_scale, color, thickness)
cv2.imshow('Image with Text', opencv)
cv2.waitKey(0)
cv2.destroyAllWindows()

#3a.RGB to HSV Conversion
hsv=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('HSV Image',hsv)
cv2.waitKey(0)

#3b.RGB to Grayscale Conversion
grey=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('HSV Image',grey)
cv2.waitKey(0)

#3c.RGB to YCrCb
ycrcb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow('ycrcb Image',ycrcb)
cv2.waitKey(0)

#3d.HSV to RGB
rgb=cv2.cvtColor(hsv,cv2.COLOR_HSV2RGB)
cv2.imshow('RGB Image',rgb)
cv2.waitKey(0)

#4a. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

#4b. Modify the color of the pixel at (200, 200) to white
image[200, 200] = [255, 255, 255]
cv2.imshow('pixel',image)
cv2.waitKey(0)

#5. Resize the image by half
height, width = image.shape[:2]
new_dimensions = (width // 2, height // 2)
resized_image = cv2.resize(image, new_dimensions, interpolation=cv2.INTER_AREA)
cv2.imshow('resized image',resized_image)
cv2.waitKey(0)

#6. Image Cropping
x, y, w, h = 50, 50, 100, 100
roi = image[y:y+h, x:x+w]
cv2.imshow('Cropped ROI', roi)
cv2.waitKey(0)

#7a. Image Flipping (Horizontal)
flipped_horizontally = cv2.flip(image, 1)
cv2.imshow('Original Image', image)
cv2.imshow('Horizontally Flipped Image', flipped_horizontally)
cv2.waitKey(0)

#7b. Image Flipping (Vertical)
flipped_vertically = cv2.flip(image, 0)
cv2.imshow('Original Image', image)
cv2.imshow('Vertically Flipped Image', flipped_vertically)
cv2.waitKey(0)

#8. Write and Save the modified image
cv2.imwrite('modified image',flipped_vertically)
```
## Output:


![image](https://github.com/user-attachments/assets/5aed25a6-8c38-4e67-ac47-8706361d926b)
![image](https://github.com/user-attachments/assets/9979731d-4fbb-49b6-b153-72fdf9952095)
![image](https://github.com/user-attachments/assets/6c31d60f-2e93-47dd-b17d-84676041cacd)
![image](https://github.com/user-attachments/assets/5768a1a7-d11f-4d14-8e4a-b5fdaa57677b)
![image](https://github.com/user-attachments/assets/5f6eed6c-1645-4229-bc6b-6b35201be9d2)
![image](https://github.com/user-attachments/assets/8550e088-8ae3-49b3-a501-29dbebd901bd)
![image](https://github.com/user-attachments/assets/ce6fdddd-5c8d-4967-b30b-8ed183d6d127)
![image](https://github.com/user-attachments/assets/6137e43e-7cb2-43f8-b11c-e5c4cfd8eecf)
![image](https://github.com/user-attachments/assets/c85ca9fa-3f98-4833-9294-d58c5e193cb1)
![image](https://github.com/user-attachments/assets/830ee006-96fe-4ff1-a932-f4aef3daafa8)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
