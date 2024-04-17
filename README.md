# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.
 
## Program:
```
DEVELOPED BY: SANJAY T
REGISTER NO: 212222110039
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'SANJAY', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
### Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
### Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image

![image](https://github.com/sanjaythiyagarajan/OPENING--AND-CLOSING/assets/119409242/a6ea28ba-7a66-4a44-af14-e3820d3c4284)


### Display the result of Opening

![image](https://github.com/sanjaythiyagarajan/OPENING--AND-CLOSING/assets/119409242/fe1b0e17-215d-4671-a959-f92442c7e0c8)



### Display the result of Closing

![image](https://github.com/sanjaythiyagarajan/OPENING--AND-CLOSING/assets/119409242/722a12ef-5577-4d2c-a95f-26a3ba8f1392)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
