# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

<br>


### Step2:
Create the text image using cv2.putText.

<br>

### Step3:
Then create the structuring image for dilation/erosion.

<br>

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

<br>

### Step5:
Plot the images using plt.imshow.

<br>

 
## Program:
```
Developed by : Vishranthi A
Reg No.: 212221230124
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
img=cv2.cvtColor(text_image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"Vishranthi A",(5,70),font,2,(0,0,255),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(img,kernel)
cv2.imshow("Eroded Image",image_erode)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate the image
image_dilate = cv2.dilate(img,kernel)
cv2.imshow("Dilated Image",image_dilate)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
<br>
<br>
<br>

![image](https://github.com/Vishranthi-arun/Implementation-of-Erosion-and-Dilation/assets/93427278/dea9298d-2e5b-41be-b5dc-17575350e726)

<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>

![image](https://github.com/Vishranthi-arun/Implementation-of-Erosion-and-Dilation/assets/93427278/46160727-2a49-4640-82b9-d88051d99868)

<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>

![image](https://github.com/Vishranthi-arun/Implementation-of-Erosion-and-Dilation/assets/93427278/2ca7ae93-58eb-4c08-9579-b34291007eb2)

<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
