## Opening-and-Closing
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step 1:
Import the necessary packages.
## Step 2:
Create the Text using cv2.putText.
## Step 3:
Create the structuring element.
## Step 4:
Use Opening operation.
## Step 5:
Use Closing Operation.
## Step 6:
Print the output and end the program.
## Program:
```
Developed By:S.ABHISHEK
Register No:212221230002
```
## Import the necessary packages
```
import numpy as np
import matplotlib.pyplot as plt
import cv2
```
## Create the Text using cv2.putText
```
text_image = np.zeros((100,660),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"S.ABHISHEK",(130,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')
```
## Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_ELLIPSE,(5,11))
```
## Use Opening operation
```
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')
```
## Use Closing Operation
```
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')
```
## Output:

## Display the input Image
![image](https://github.com/S-ABHISHEK-1905/Opening-and-Closing/assets/66360846/38b2d1cd-25b8-4ee3-ac00-1f7f68e15072)

## Display the result of Opening
![image](https://github.com/S-ABHISHEK-1905/Opening-and-Closing/assets/66360846/96970fb4-449e-4a7f-a439-a1b863c10a10)


## Display the result of Closing
![image](https://github.com/S-ABHISHEK-1905/Opening-and-Closing/assets/66360846/76d8d9d0-843d-4b64-b714-98497ecba447)

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
