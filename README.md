# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use any filters for smoothing the image to reduse the noise.

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
## Program:
1. Import the packages
```
import cv2
import matplotlib.pyplot as plt
```

2. Load the image, Convert to grayscale and remove noise
```
img = cv2.imread("sp2.jpg")
plt.imshow(img)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```

3. SOBEL EDGE DETECTOR
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.imshow(sobelx)
plt.title("SOBEL_X")
plt.xticks([])
plt.yticks([])
plt.show()

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.imshow(sobely)
plt.title("SOBEL_Y")
plt.xticks([])
plt.yticks([])
plt.show()

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize =(8,8))
plt.imshow(sobelxy)
plt.title("SOBEL_XY")
plt.xticks([])
plt.yticks([])
plt.show()
```


4. LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.imshow(laplacian)
plt.title('LAPLACIAN')
plt.axis("off")
plt.show()
```


5. CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(new_image,120,150)
plt.figure(figsize=(8,8))
plt.imshow(canny_edges)
plt.title('CANNY_EDGES')
plt.axis("off")
plt.show()
```
## Output:
### GRAY SCALE
<img width="340" alt="image" src="https://user-images.githubusercontent.com/93427376/232233342-193097cc-70f8-4858-8926-4c548e74f4a6.png">


### SOBEL EDGE DETECTOR
<img width="356" alt="image" src="https://user-images.githubusercontent.com/93427376/232233431-44cb693b-074c-4793-9177-3ffcb6a7c2c0.png">

<img width="366" alt="image" src="https://user-images.githubusercontent.com/93427376/232233450-962e7a60-6407-41d6-a57b-6a1cc8ef0c4f.png">

<img width="359" alt="image" src="https://user-images.githubusercontent.com/93427376/232233535-9fdccdd3-9782-4755-87ec-ec8aaaf531dc.png">


### LAPLACIAN EDGE DETECTOR
<img width="369" alt="image" src="https://user-images.githubusercontent.com/93427376/232233605-54e39b8e-ba81-4115-9f64-0784681b2097.png">


### CANNY EDGE DETECTOR
<img width="364" alt="image" src="https://user-images.githubusercontent.com/93427376/232233673-4cc032f6-efb4-4060-a40c-3acca1245106.png">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
