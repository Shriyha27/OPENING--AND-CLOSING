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
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

``` Python
#NAME: V.SHRIYHA
#REG.NO: 212224230267

# Import necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
from google.colab.patches import cv2_imshow

# i) Create the text using cv2.putText
img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "V.SHRIYHA", (5, 200), font, 2, (255), 6, cv2.LINE_AA)

cv2_imshow(img2)

# ii) Create structuring elements
kernel1 = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))
kernel2 = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# iii) Use Opening operation (Erosion followed by Dilation)
img_open = cv2.morphologyEx(img2, cv2.MORPH_OPEN, kernel2)
cv2_imshow(img_open)

# iv) Use Closing operation (Dilation followed by Erosion)
img_close = cv2.morphologyEx(img2, cv2.MORPH_CLOSE, kernel1)
cv2_imshow(img_close)

```
## Output:

### Display the input Image
<img width="731" height="361" alt="image" src="https://github.com/user-attachments/assets/aecacb95-524a-4291-abea-3383b04cf29a" />

### Display the result of Opening
<img width="719" height="372" alt="image" src="https://github.com/user-attachments/assets/0c854b12-c33f-4a54-a082-0979adaf571d" />


### Display the result of Closing
<img width="637" height="374" alt="image" src="https://github.com/user-attachments/assets/62779614-13d1-4a39-b7bc-27f04dfb496c" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
