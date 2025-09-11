# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

# Developed By: Farhana H
# Register Number: 212223230057

# Input Grayscale Image
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('image.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

```
# Histogram of Grayscale Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
# Equalization
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
# Equalized Histogram
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## Output:
### Input Grayscale Image and Color Image

<img width="816" height="572" alt="Screenshot 2025-09-11 221709" src="https://github.com/user-attachments/assets/c3a503f7-755f-4e79-83ef-868e02e18772" />



### Histogram of Grayscale Image and any channel of Color Image

<img width="881" height="602" alt="Screenshot 2025-09-11 221716" src="https://github.com/user-attachments/assets/447c9ebf-fba2-4b68-8ca3-41300f4402f5" />


### Histogram Equalization of Grayscale Image.

<img width="788" height="569" alt="Screenshot 2025-09-11 221722" src="https://github.com/user-attachments/assets/47a44ce7-4edb-431a-9dbe-b7794c88d190" />

# Equalized Histogram.
<img width="921" height="585" alt="Screenshot 2025-09-11 221727" src="https://github.com/user-attachments/assets/9568664f-61a1-4056-9308-8a33de9e3e94" />


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
