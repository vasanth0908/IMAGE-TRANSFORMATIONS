# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output.

### Step5:
End the program.
## Program:
### Developed By: vasanth s
### Register Number: 212222110052
### i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
```

### ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
```
### iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1, 0, 0],
                [0.5, 1, 0],
                [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis
plt.show()
```
### iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
### v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
```
### vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
cropped_img=input_image[100:300, 100:300]
plt.imshow(cropped_img)
```
## Output:
### i)Image Translation
![image](https://github.com/vasanth0908/IMAGE-TRANSFORMATIONS/assets/122000018/27ef2249-a9ee-4427-8416-d85ad7c39e19)


### ii) Image Scaling
![image](https://github.com/vasanth0908/IMAGE-TRANSFORMATIONS/assets/122000018/bed0d1fd-0845-4d12-b1ab-1987779a62d4)



### iii)Image shearing
![image](https://github.com/vasanth0908/IMAGE-TRANSFORMATIONS/assets/122000018/d65c80e5-fb4b-4871-a306-951fdc67a17a)



### iv)Image Reflection
![image](https://github.com/vasanth0908/IMAGE-TRANSFORMATIONS/assets/122000018/38d4386c-9bab-4169-bc29-b5ce0342c107)




### v)Image Rotation
![image](https://github.com/vasanth0908/IMAGE-TRANSFORMATIONS/assets/122000018/6932a506-ce1d-490b-8420-82ea1d630dfb)




### vi)Image Cropping
![image](https://github.com/vasanth0908/IMAGE-TRANSFORMATIONS/assets/122000018/204414c6-1dd8-4a0d-8f62-878c70603a45)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
