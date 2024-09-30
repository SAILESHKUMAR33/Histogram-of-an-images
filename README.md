# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: SAILESHKUMAR A
# Register Number: 212222230126
#CODE:

import cv2
import numpy as np
from matplotlib import pyplot as plt
image = cv2.imread('asil.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()









```
## Output:
### Input Grayscale Image and Color Image
 Grayscale Image :

![Screenshot 2024-09-30 155428](https://github.com/user-attachments/assets/1b2f5545-ffcf-493d-b347-453a2f6164af)

Color Image:
![SAVE_20240227_211357](https://github.com/user-attachments/assets/9b75e3ea-66d6-4b74-82b7-5703312aa03f)



### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2024-09-30 155507](https://github.com/user-attachments/assets/d1d9a02a-2a57-4f15-8cf7-e20a21e250ed)




### Histogram Equalization of Grayscale Image.

![Screenshot 2024-09-30 155523](https://github.com/user-attachments/assets/eacb5487-abae-4fd8-adfd-639907a60281)

![Screenshot 2024-09-30 155535](https://github.com/user-attachments/assets/441a2f15-948f-4968-a8c6-2edc958a944e)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
