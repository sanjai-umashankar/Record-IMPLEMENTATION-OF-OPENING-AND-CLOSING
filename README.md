# OPENING--AND-CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages

## Step2:
Create the Text using cv2.putText

## Step3:
Create the structuring element

## Step4:
Use Opening operation

## Step5:
Use Closing Operation

 
## Program Developed By:
- **Name:** SANJAI U 
- **Register Number:**  212224240145
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'NIRMAL', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

kernel = np.ones((3, 3), np.uint8)

opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

original_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opened_rgb = cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB)
closed_rgb = cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(12,5))

plt.subplot(1,3,1)
plt.imshow(original_rgb)
plt.title("Input Image with Text")
plt.axis('off')

plt.subplot(1,3,2)
plt.imshow(opened_rgb)
plt.title("Opening Operation")
plt.axis('off')

plt.subplot(1,3,3)
plt.imshow(closed_rgb)
plt.title("Closing Operation")
plt.axis('off')

plt.show()

```


## Output:

### Display the input Image

<img width="677" height="543" alt="image" src="https://github.com/user-attachments/assets/126574a5-3911-4756-962f-a33e96d7e8ae" />

### Display the result of Opening

<img width="676" height="546" alt="image" src="https://github.com/user-attachments/assets/d2c6635e-22b4-4da1-8a6c-2be6b6641833" />

### Display the result of Closing

<img width="692" height="567" alt="image" src="https://github.com/user-attachments/assets/f6224911-19b2-47b3-81f2-3255c623e3df" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
