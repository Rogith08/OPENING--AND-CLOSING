# EXP NO: 10 - OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

``` Python
#NAME: ROGITH. K
#REG.NO: 212223110042

import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'ROGITH.K', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

```
## Output:

### Display the input Image
<img width="463" height="495" alt="Screenshot 2025-11-10 114729" src="https://github.com/user-attachments/assets/4eeb3fa3-dce2-4000-88aa-4bb949251000" />


### Display the result of Opening
<img width="460" height="493" alt="Screenshot 2025-11-10 114739" src="https://github.com/user-attachments/assets/c0b987a0-9d84-4245-bd08-763bf366f7a9" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
