# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Read the Image:

Load the input color image from a specified path.
### Step-2:Convert to Grayscale:

Transform the color image into a grayscale format for easier processing.
### Step-3:Edge Detection:

Apply an edge detection technique to identify the prominent edges in the grayscale image.
### Step-4:Create Structuring Element:

Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.
### Step-6:Morphological Operations:

Perform morphological operations:<br>
Opening: Remove small objects from the edges to clean up the image.<br>
Closing: Fill small holes in the detected edges to enhance the structure.
### Step-7:Display Results:

Show the original grayscale image, along with the results of the opening and closing operations for visual comparison.

 
## Program:
```python
Developed By: NARAMALA KUMARTEJA
Reference Number :212223230132
``` 

# Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("Fish.jpg")  

kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")

plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```
# Create the Text using cv2.putText
```python
image = cv2.imread("Fish.jpg")
```
# Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
# Use Opening operation
```python
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
# Use Closing Operation
```python
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/cf6d3689-7229-4d58-bb1c-aeed5bc02ce3)

### Display the result of Opening
![image](https://github.com/user-attachments/assets/c5068dc4-8ec7-4317-86c6-969b57688117)

### Display the result of Closing
![image](https://github.com/user-attachments/assets/e6246f86-bf3b-4c35-81b0-d09c92d65d48)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
