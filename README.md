# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step 1:
Import the necessary packages.
<br>
## Step 2:
Create the Text using cv2.putText.
<br>
## Step 3:
Create the structuring element.
<br>
## Step 4:
Use Opening operation.
<br>
## Step 5:
Use Closing Operation.
<br>
## Step 6:
Print the output and end the program.
 <br>
## Program:

``` Python
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"K.M.Swetha",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')





```
## Output:

### Display the input Image
![image](https://github.com/swethamohanraj/OPENING--AND-CLOSING/assets/94228215/981f94c6-8ff6-4280-ad3b-20899c804512)


### Display the result of Opening
![image](https://github.com/swethamohanraj/OPENING--AND-CLOSING/assets/94228215/704c1df7-fffa-4075-9223-36f538aba0e1)


### Display the result of Closing
![image](https://github.com/swethamohanraj/OPENING--AND-CLOSING/assets/94228215/1fbaa7d2-411a-45ca-a8b2-cb9d6032cd64)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
