# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Create the Text using cv2.putText
### Step3:
Create the structuring element
### Step4:
Use Opening operation
### Step5:
Use Closing Operation
 
## Program:
Developed By: GIRITHICK ROHAN N
Reg.NO: 212223230063

# Import the necessary packages
``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((300, 600, 3), dtype="uint8")
```
# Create the Text using cv2.putText
```
text = "GIRITHICK ROHAN"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
# Use Opening operation
```
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
# Use Closing Operation
```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
## Output:

### Display the input Image

![img](https://raw.githubusercontent.com/Girithickrohan/OPENING--AND-CLOSING/refs/heads/main/1.png)

### Display the result of Opening

![img](https://raw.githubusercontent.com/Girithickrohan/OPENING--AND-CLOSING/refs/heads/main/2.png)

### Display the result of Closing

![img](https://raw.githubusercontent.com/Girithickrohan/OPENING--AND-CLOSING/refs/heads/main/3.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
