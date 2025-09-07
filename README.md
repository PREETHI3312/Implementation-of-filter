# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7




## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>

Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By : PREETHI A K
### Register Number: 212223230156
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nature.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters
</br>

### i) Using Averaging Filter
<img width="419" height="335" alt="image" src="https://github.com/user-attachments/assets/3ec67779-4a52-4501-9692-e3452e09c741" />


### ii)Using Weighted Averaging Filter
<img width="633" height="502" alt="image" src="https://github.com/user-attachments/assets/0e21bba0-821c-489c-acb6-7b0429b9cec3" />


### iii)Using Gaussian Filter
<img width="631" height="506" alt="image" src="https://github.com/user-attachments/assets/6159af9d-223a-45c3-947a-c6d700fe1ae1" />


### iv) Using Median Filter
<img width="633" height="497" alt="image" src="https://github.com/user-attachments/assets/703feb5f-2f00-47d3-ae03-2f35252026cd" />


### 2. Sharpening Filters
</br>

### i) Using Laplacian Kernal
<img width="636" height="499" alt="image" src="https://github.com/user-attachments/assets/b2c3ee1a-41f8-450c-a554-e352b4471d44" />


### ii) Using Laplacian Operator
<img width="629" height="495" alt="image" src="https://github.com/user-attachments/assets/39f9e710-3573-4ea3-bff9-e1c77cd4ff7c" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
