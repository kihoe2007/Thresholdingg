## EXP-8-THRESHOLDING
# Aim

To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

Software Required
Anaconda - Python 3.7
OpenCV
# Algorithm
# Step1:
Load the necessary packages

# Step2:
Read the Image and convert to grayscale

# Step3:
Use Global thresholding to segment the image.

# Step4:
Use Adaptive thresholding to segment the image.

# Step5:
Use Otsu's method to segment the image and display the results.

 # Program
## kishore S M 
## 212224230131
```python
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt




# Read the Image and convert to grayscale

# Step 2: Read the image and convert to grayscale
image = cv2.imread('kishore.tif')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale


# Use Global thresholding to segment the image
# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')



# Use Adaptive thresholding to segment the image


# Step 3: Use Global Thresholding to segment the image
# Apply global thresholding with a threshold value of 127
# Step 4: Use Adaptive Thresholding to segment the image
# Apply adaptive thresholding using Gaussian method
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

# Use Otsu's method to segment the image 

# Step 3: Use Global Thresholding to segment the image
# Apply global thresholding with a threshold value of 127
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)


# Display the results





```

### Original Image



<br>
<br>
<br><img width="705" height="297" alt="image" src="https://github.com/user-attachments/assets/f5f3a7e9-57a1-4367-9eff-fce3c6252a09" />

<br>
<br>

### Global Thresholding
<br>
<br><img width="856" height="717" alt="image" src="https://github.com/user-attachments/assets/de40b41c-a1e8-4f54-94a8-f088dd35f131" />

<br>
<br>
<br>

### Adaptive Thresholding
<br>
<br><img width="856" height="717" alt="image" src="https://github.com/user-attachments/assets/0691ce1a-1804-4f12-81a6-fe177426fd6b" />

<br>
<br>
<br>

### Optimum Global Thesholding using Otsu's Method
<br>
<br>
<br><img width="856" height="717" alt="image" src="https://github.com/user-attachments/assets/3e26e4e1-870a-4120-8db9-d023891dfc08" />

<br>
<br>


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
