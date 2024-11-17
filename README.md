# Implementation-of-Erosion-and-Dilation->
## Aim:
To implement Erosion and Dilation using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
Developed By : M Sanjay
Reg No : 212222240090
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
image = np.zeros((300, 600, 3), dtype="uint8")
text = "M Sanjay"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
### Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```
### Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2024-11-17 161305](https://github.com/user-attachments/assets/6d5cb2ae-ce45-4703-bc72-c0356b4a3e09)


### Display the Eroded Image
![Screenshot 2024-11-17 161311](https://github.com/user-attachments/assets/bad1d163-170e-4002-89fb-82e31897a485)



### Display the Dilated Image
![Screenshot 2024-11-17 161316](https://github.com/user-attachments/assets/6cb09cba-94e4-4087-a64e-e9ad1f011ddd)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
