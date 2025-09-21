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
<img width="413" height="540" alt="image" src="https://github.com/user-attachments/assets/85188378-6fb6-4059-990f-5dfbd768a905" />


### ii)Using Weighted Averaging Filter
<img width="377" height="500" alt="image" src="https://github.com/user-attachments/assets/0788fbb9-6b12-4a3f-8e82-49a9cda3ac46" />


### iii)Using Gaussian Filter
<img width="380" height="489" alt="image" src="https://github.com/user-attachments/assets/3ef24cab-e779-47fa-b043-77b47c2b84da" />


### iv) Using Median Filter
<img width="373" height="500" alt="image" src="https://github.com/user-attachments/assets/b6e1f993-30b9-429a-bbc0-c07223f209d6" />


### 2. Sharpening Filters
</br>

### i) Using Laplacian Kernal
<img width="371" height="498" alt="image" src="https://github.com/user-attachments/assets/75c81189-f722-4c6f-a234-674bd4b4bd38" />


### ii) Using Laplacian Operator
<img width="377" height="491" alt="image" src="https://github.com/user-attachments/assets/96f74a9b-90ab-4390-847e-2be0f9356925" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
