# Basic_image_Manipulation
# # Program
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('Apollo.jpg')
height=720
width=1280
print(f"Width: {width}, Height: {height}")
plt.figure(figsize=(10, 10))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.show()
plt.axis('off')
cv2.imwrite('Apollo-11-Launch.png', image)
```
# OUTPUT

![image](https://github.com/user-attachments/assets/430528a2-0f54-49cd-9c9a-1f02800b9847)


# Program
```
img = cv2.imread('newzealand.jpg', cv2.IMREAD_COLOR)
print(img.shape)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])
plt.title("Original Image")
plt.show()
plt.axis('off')
```
# OUTPUT

![image](https://github.com/user-attachments/assets/29feb652-3fbd-4248-8979-f60430171e93)

# Program
```
x, y, a, b = 250, 250, 250, 250
cropped_img = img[y:y+b, x:x+a]
resized_img = cv2.resize(cropped_img,None, fx=2, fy=2)
flipped_img = cv2.flip(resized_img, 1)
plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1])
plt.title("Cropped, Resized, and Flipped Image")
plt.show()
```
# OUTPUT

![image](https://github.com/user-attachments/assets/2dc49152-eae8-4376-bf33-1c4cfb8fe922)

# Program
```
img = cv2.imread('emerald.jpg', cv2.IMREAD_COLOR)
gray_image = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
print("Grayscale Image Shape:", gray_image.shape)
plt.figure(figsize=(10, 10))
plt.imshow(gray_image)
plt.axis('off')
plt.title("Grayscale Image")
plt.show()
```
# OUTPUT
![image](https://github.com/user-attachments/assets/6990ebe2-cc5f-4e52-8479-699085eadec3)

# Program
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('apollo.jpg')
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
start=(700,700)
stop=(450,69)
color=(255,0,255)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
# OUTPUT

![image](https://github.com/user-attachments/assets/2f426fa9-7d0c-46e7-9d62-70f545b59fdb)

# Program
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('apollo.jpg')
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
position = (50, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)
thickness = 2
cv2.putText(img, text, position, font, font_scale, color, thickness)
start = (450, 69)      
stop = (700, 650)      
rect_color = (255, 0, 255)
rect_thickness = 10
cv2.rectangle(img, start, stop, rect_color, rect_thickness)
plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```
# OUTPUT

![image](https://github.com/user-attachments/assets/0e9f5d09-43d6-484f-b483-bf2b83d13425)

Basic_image_manipulaion
