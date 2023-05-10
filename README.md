# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:
```
Developed by : Marella Dharanesh
Registeration Number:212222240062
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Gowri",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')



```
## Output:

### Display the input Image


![download](https://github.com/MarellaDharanesh/Implementation-of-Erosion-and-Dilation/assets/118707669/2b776353-d4cd-48e2-8b83-0d8f58da33eb)

### Display the Eroded Image

![download](https://github.com/MarellaDharanesh/Implementation-of-Erosion-and-Dilation/assets/118707669/ab955322-6f42-4be0-961c-337858069c12)



### Display the Dilated Image
![download](https://github.com/MarellaDharanesh/Implementation-of-Erosion-and-Dilation/assets/118707669/fd1ce3f4-e324-43dd-bd86-a0598ecf637f)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
