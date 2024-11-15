# EX 1
# COLOR_CONVERSIONS_OF-IMAGE
## DATE:
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
### Developed By: DEEPAK RAJ S
### Register Number: 212222240023


## Output:

### i)Read and Display an Image

```
import cv2
# Read the image
image = cv2.imread('loki1.jpeg')
# Display the image in a window
cv2.imshow('Image Window', image)
# Wait indefinitely for a key press
cv2.waitKey(0)
# Destroy all windows created by OpenCV
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/9a7ec3fe-b0e6-42db-9f81-d65db97edb31)
<br>
<br>

### ii)Draw Shapes and Add Text

```
import cv2

img = cv2.imread("loki1.jpeg")
start=(0,0)
stop=(500,329)
color=(100,255,100)
thickness=10
res_img=cv2.circle(img,(330,225),150,(255,0,0),10)
res_img=cv2.rectangle(img,start,stop,color,thickness)
text = "OpenCV Drawing"
org = (10, 30)  # top-left corner of the text string
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
text_color = (255, 255, 255)  # White color
thickness = 2
res_img = cv2.line(img,(100,200),(900,100),(200,100,205),10)
res_img= cv2.putText(res_img, text, org, font, font_scale, text_color, thickness, cv2.LINE_AA)

# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/f9163c6c-061c-423e-9ed1-d21bee89b2d1)
![image](https://github.com/user-attachments/assets/8d443cea-3021-40e2-8a5d-15fd006a8313)
![image](https://github.com/user-attachments/assets/c0cbcdc0-6787-4a67-ab6f-ab2f2afb3086)



<br>
<br>

### iii)Image Color Conversion

```
# Read the image
image = cv2.imread("loki1.jpeg")

# Convert to HSV color space
img_hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
# Convert to grayscale
img = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)


# Display the HSV image
cv2.imshow('Image Window (HSV)', img_hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Convert the image from RGB to YCrCb and display it
ycrcb_image = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb Image', ycrcb_image)
cv2.waitKey(0)

# Convert the HSV image back to RGB and display it
hsv_to_rgb_image = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to RGB Image', hsv_to_rgb_image)
cv2.waitKey(0)
```
### Convert the image from RGB to HSV and display it:
![image](https://github.com/user-attachments/assets/3362fb1a-5d88-438a-b339-440a109a9d18)


### Convert the image from RGB to GRAY and display it:
![image](https://github.com/user-attachments/assets/b828adfd-d6a7-4d65-bcc5-1214e52bd994)

### Convert the image from RGB to YCrCb and display it:
![image](https://github.com/user-attachments/assets/293193ea-232e-4b9f-ab3d-23828a6245b8)

### Convert the HSV image back to RGB and display it:
![image](https://github.com/user-attachments/assets/00e3c8ef-64d4-41b0-ab2f-b3a98f9888f3)

<br>
<br>

### iv)Access and Manipulate Image Pixels

```
# Step 4: Access and Manipulate Image Pixels
# Access and print the value of the pixel at coordinates (100, 100)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# Modify the color of the pixel at (200, 200) to white
image[200, 200] = [255, 255, 255]
print(f"Modified pixel value at (200, 200): {image[200, 200]}")
```
![image](https://github.com/user-attachments/assets/66bf0b1a-3b5a-4da3-a159-90b507f5eeed)
<br>
<br>

### v)Image Resizing
```
# Image Resizing
# Resize the original image to half its size and display it
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('Resized Image', resized_image)
cv2.waitKey(0)
```
![image](https://github.com/user-attachments/assets/cdb7f2a8-6345-434d-bb0b-51573bd3ff97)

<br>
<br>

### vi)Image Cropping:

```
# Image Cropping
# Crop a region of interest (100x100 pixels starting at (50, 50)) and display it
roi = image[50:150, 50:150]
cv2.imshow('Cropped ROI Image', roi)
cv2.waitKey(0)
```
![image](https://github.com/user-attachments/assets/a46bd24e-a71d-4593-ac88-81439a5eafdc)

<br>
<br>

### vii)Image Flipping

```
# Flip the original image horizontally and display it
flipped_horizontally = cv2.flip(image, 1)
cv2.imshow('Horizontally Flipped Image', flipped_horizontally)
cv2.waitKey(0)

# Flip the original image vertically and display it
flipped_vertically = cv2.flip(image, 0)
cv2.imshow('Vertically Flipped Image', flipped_vertically)
cv2.waitKey(0)
```

### Flip the original image horizontally and display it:
![image](https://github.com/user-attachments/assets/8aa5495b-447f-48f0-b135-930329634339)

### Flip the original image vertically and display it:
![image](https://github.com/user-attachments/assets/d3644900-6792-4d50-a092-e8e7bee3db69)

<br>
<br>

### viii)Write and Save the Modified Image

```
# Step 8: Write and Save the Modified Image
output_path = 'output.jpg'
cv2.imwrite(output_path, image_with_text)
print(f"Modified image saved as {output_path}")
```
![image](https://github.com/user-attachments/assets/d6ad0554-365a-4c30-a515-8967af1101f1)
<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







