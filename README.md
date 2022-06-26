## EX NO:04
## DATE:25.4.22
# <p align="center">Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.
<br>
<br>
<br>
<br>
<br>
## Program:
```python
# Developed By: 212220230036
# Register Number: PRASHETHAA R
  
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('nat.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('flower.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('flower.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

<br>
<br>
<br>
<br>



```

## Output:
### Input Grayscale Image and Color Image
![Screenshot (246)](https://user-images.githubusercontent.com/75234942/164980430-57e3d63b-c282-418e-a69f-87a2ea91c983.png)
![Screenshot (247)](https://user-images.githubusercontent.com/75234942/164980438-698e8849-d42d-48fa-9b35-78bb992c1be6.png)
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
 br>
<br>
<br>
<br>
### Histogram of Grayscale Image and any channel of Color Image

![Screenshot (246)1](https://user-images.githubusercontent.com/75234942/164980445-21aae4ad-ee28-48f6-b067-fbb0f233402c.png)
![Screenshot (247)1](https://user-images.githubusercontent.com/75234942/164980449-badb4ef1-2bad-4aa9-94f1-c3f0599a1379.png)

### Histogram Equalization of Grayscale Image
![Screenshot (248)](https://user-images.githubusercontent.com/75234942/164980536-04a41a37-1207-42a1-9aa1-c84372e96d56.png)
![Screenshot (249)](https://user-images.githubusercontent.com/75234942/164980546-038b5452-8fcd-4dd8-92fd-8838e7b8b44d.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
