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
### Developed By : P.Senthil arunachalam
### Register Number:212224240147
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Tiger.jpg")
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
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show(
```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```Python

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")

plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
<img width="935" height="330" alt="average" src="https://github.com/user-attachments/assets/7684fd5f-1e3b-4694-8ac8-f065354e0eb5" />
</br>


ii)Using Weighted Averaging Filter
</br>
<img width="483" height="316" alt="weighted avg" src="https://github.com/user-attachments/assets/28913205-d3f1-493b-80a4-3d90da20a96b" />


</br>

iii)Using Gaussian Filter
</br>
<img width="450" height="304" alt="guassian_blur" src="https://github.com/user-attachments/assets/2667a55c-5103-4bfb-8a67-13b13b2ff145" />

</br>

iv) Using Median Filter
</br>
<img width="486" height="320" alt="median_blur" src="https://github.com/user-attachments/assets/5614aa68-0608-47e6-bdd9-6cb496843b13" />

</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
<img width="482" height="328" alt="Laplacian Kernal" src="https://github.com/user-attachments/assets/39a0b333-9ec5-40ab-abe0-13ca02726817" />

</br>

ii) Using Laplacian Operator
</br>
<img width="434" height="304" alt="Laplacian Operator" src="https://github.com/user-attachments/assets/3b98f8ca-f902-46ca-ade4-ae5afb444a47" />

</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
