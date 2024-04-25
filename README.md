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


### Step5:
End the program.
 
## Program:
### DEVELOPED BY: D.B.V. SAI GANESH
### REGISTER NO: 212223240025
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'RRR',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis('off')


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")



# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")




```
## Output:

### Display the input Image
![image](https://github.com/saiganesh2006/OPENING--AND-CLOSING/assets/145742342/722c819e-217d-4395-9f52-4ee06cefaa29)


### Display the result of Opening
![image](https://github.com/saiganesh2006/OPENING--AND-CLOSING/assets/145742342/8f67af61-5bd7-424a-8acd-1fc7a4ab2c96)


### Display the result of Closing
![image](https://github.com/saiganesh2006/OPENING--AND-CLOSING/assets/145742342/2e243c00-e3a3-40b6-9c0c-04e184d052d0)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
