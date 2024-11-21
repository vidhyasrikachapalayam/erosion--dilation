# EX 9 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
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
### Name:Vidhyasri
### Register No.:212222230170


# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

// Create a blank image
image = np.zeros((300, 600, 3), dtype="uint8")
```
# Create the Text using cv2.putText
```
text = "vidhyasri"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```


# Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```
# Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
# Convert images from BGR to RGB for Matplotlib
```
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
```
# Plot the original, eroded, and dilated images using Matplotlib
```
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()


```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/df2a4136-8756-42a9-870e-8216cf044042)


### Display the Eroded Image

![image](https://github.com/user-attachments/assets/cf8c7d45-138d-4ddb-ad3a-3fc1600d50bd)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/29488f2d-e0f5-41d1-904f-0ef946cbc8ee)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
