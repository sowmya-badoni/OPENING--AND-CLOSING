# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:

### NAME: Ashwina K N
### REG.No:212223230025

# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ASTROPHYSICIST',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![Screenshot 2024-04-28 210830](https://github.com/AbishekAnand15/OPENING--AND-CLOSING/assets/118706942/bd1fcc39-a81b-4157-ba3c-d32587844c84)
### Display the result of Opening
![Screenshot 2024-04-28 210842](https://github.com/AbishekAnand15/OPENING--AND-CLOSING/assets/118706942/f235cd1b-a05b-4f5e-b629-f9968f3ff97d)
### Display the result of Closing
![Screenshot 2024-04-28 210849](https://github.com/AbishekAnand15/OPENING--AND-CLOSING/assets/118706942/7915dd60-a8aa-49c9-8039-14131c30a89e)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
