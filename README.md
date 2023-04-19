# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

Step1
Import the necessary modules.

Step2
Perform smoothing operation on a image.

Step3
Perform sharpening on a image.

Step4
Display all the images with their respective filters.

## Program:
### Developed By   :YASHASWI MITTA
### Register Number:212221230062

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()






```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```

iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()







```
ii) Using Laplacian Operator
```Python

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()



```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter


![dip 6-1](https://user-images.githubusercontent.com/94619247/233021895-412427da-f5f1-4f37-a84c-74036bf52684.jpg)

ii) Using Weighted Averaging Filter


![dip 6-2](https://user-images.githubusercontent.com/94619247/233022002-6ce88fa9-0dab-4aba-9dc8-dd5f7dceffe8.jpg)

iii) Using Gaussian Filter


![dip 6-3](https://user-images.githubusercontent.com/94619247/233022057-780b2757-115f-41a3-83bf-ed44d7874049.jpg)


iv) Using Median Filter


![dip 6-4](https://user-images.githubusercontent.com/94619247/233022133-35bf5a41-bf7c-4448-b0af-f4d7732bbaa8.jpg)


### 2. Sharpening Filters


i) Using Laplacian Kernal


![dip 6-5](https://user-images.githubusercontent.com/94619247/233022197-89875327-043f-4ca6-bf56-a5420d537937.jpg)


ii) Using Laplacian Operator


![dip 6-6](https://user-images.githubusercontent.com/94619247/233023866-d668c7fa-4ed3-4d9d-a286-d2bfe0c5b7b7.jpg)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domaIn.
