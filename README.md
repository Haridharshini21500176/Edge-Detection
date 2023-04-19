# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required packages for further process.

### Step2:
<br>
Read the image and convert the bgr image to gray scale image.

### Step3:
<br>
Use any filters for smoothing the image to reduse the noise.

### Step4:
<br>
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
<br>
Display the filtered image using plot and imshow.
 
## Program:
```
DEVELOPED BY: HARIDHARSHINI.S
REG NO : 212221230033
```

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt


# Load the image, Convert to grayscale and remove noise
image = cv2.imread("flower.jpeg")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

# SOBEL EDGE DETECTOR

#SOBEL X:
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

#SOBEL Y:
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()


# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()


# CANNY EDGE DETECTOR
canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
![EX 7 A](https://user-images.githubusercontent.com/94168395/233007539-c2dd3397-c9fe-4892-bce7-367649398865.png)

![EX 7 B](https://user-images.githubusercontent.com/94168395/233009711-350572cb-1963-43c4-9f08-eb10d5fb539e.png)


### LAPLACIAN EDGE DETECTOR
![EX 7 C](https://user-images.githubusercontent.com/94168395/233008832-1b972f82-0a30-434b-9723-a8eb76c4cab3.png)



### CANNY EDGE DETECTOR

![EX 7 D](https://user-images.githubusercontent.com/94168395/233009647-64a7cae8-cf96-4daf-b142-ea534aad5399.png)




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
