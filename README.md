# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
</br>
Import the required modules.
</br> 

### Step2:
</br>
Convert the image from BGR to RGB.
</br> 

### Step3:
</br>
Apply the required filters for the image separately.
</br> 

### Step4:
</br>
 Plot the original and filtered image by using matplotlib.pyplot
</br> 

### Step5:
</br>
End the program.
</br> 

## Program:
### Developed By   : Sai Eswar Kandukuri
### Register Number: 212221240020
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)

kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")

```
ii) Using Weighted Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")

```
iii) Using Gaussian Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")

```

iv) Using Median Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")

```
ii) Using Laplacian Operator
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")

```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
<img width="600" alt="1" src="https://user-images.githubusercontent.com/93427011/168228510-54a62973-243e-48f9-b7eb-7ff4dde7f6ea.png">
</br>


ii) Using Weighted Averaging Filter
</br>
<img width="600" alt="2" src="https://user-images.githubusercontent.com/93427011/168228525-96f6226a-efc6-4b14-8021-e6d6d64fa2f0.png">
</br>

iii) Using Gaussian Filter
</br>
<img width="600" alt="3" src="https://user-images.githubusercontent.com/93427011/168228536-b353ffaa-1522-4b18-911e-dc11df6af806.png">
</br>

iv) Using Median Filter
</br>
<img width="600" alt="4" src="https://user-images.githubusercontent.com/93427011/168228557-6979373c-cf94-4bc8-af5e-8a17033dd5a4.png">
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
<img width="600" alt="5" src="https://user-images.githubusercontent.com/93427011/168228573-85fcd6f7-456c-4244-99b3-8029ac0eb7d8.png">
</br>


ii) Using Laplacian Operator
</br>
<img width="600" alt="6" src="https://user-images.githubusercontent.com/93427011/168228587-cfdd1466-1233-44ba-9dd4-a394b8c9a435.png">
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
