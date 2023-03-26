# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 and save and image as filename.jpg

### Step2:

Use imread(filename, flags) to read the file.
### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
# Developed By:Sangeetha.K
# Register Number:212221230085

# IMAGE READING
```
import cv2
img=cv2.imread('baby.jpg')
cv2.imshow('image ice',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# i) Convert BGR and RGB to HSV and GRAY
```
#BGR_2_HSV
hsvimg=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGRhsv',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB_2_HSV
hsvimg1=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGBhsv',hsvimg1)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
gray=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('grayRGB',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
gray1=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('grayBGR',gray1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# ii)Convert HSV to RGB and BGR
```
#HSV TO RGB
rgb_img=cv2.cvtColor(hsvimg,cv2.COLOR_HSV2RGB)
cv2.imshow('hsv2rgb',rgb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgr_img=cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('hsv2bgr',bgr_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iii)Convert RGB and BGR to YCrCb
```
#RGB to YCrCb
YCrCb_img=cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR TO YCrCb
YCrCb_img1=cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# iv)Split and Merge RGB Image
```
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

```

# v) Split and merge HSV Image
```

#Split & merge hsv
hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()


```
## Output:
### Original Image
![image](https://user-images.githubusercontent.com/93992063/227767994-971b7497-b46f-43ed-8b70-e9eee81bf282.png)

### i) BGR and RGB to HSV and GRAY
<br>
![image](https://user-images.githubusercontent.com/93992063/227768130-edfa9837-221d-4e9c-a5fb-18d13f316af2.png)

<br>
![image](https://user-images.githubusercontent.com/93992063/227768303-36210733-050f-46d0-8e28-583911b95f58.png)

![image](https://user-images.githubusercontent.com/93992063/227768475-ca21dd5a-8a18-477b-a0f4-31a7d1ec4459.png)
![image](https://user-images.githubusercontent.com/93992063/227768528-5a0e5b05-ba78-40bd-8a89-8e229697755a.png)


### ii) HSV to RGB and BGR
<br>
![image](https://user-images.githubusercontent.com/93992063/227769324-ee887192-bf7d-4043-882e-942dc3ca22ae.png)

<br>
![Screenshot 2023-03-26 154955](https://user-images.githubusercontent.com/93992063/227769391-30cf162a-ca59-4178-850d-0dd5672ed32f.png)

### iii) RGB and BGR to YCrCb
<br>
![image](https://user-images.githubusercontent.com/93992063/227769583-576b3942-32e6-4a88-adb2-04a9d075953d.png)

<br>
![image](https://user-images.githubusercontent.com/93992063/227769651-e208ae2f-a23d-4656-8f00-57b162d42a0d.png)

### iv) Split and merge RGB Image
<br>
![Screenshot (176)](https://user-images.githubusercontent.com/93992063/227770171-13355091-e33b-49d0-b1f6-bf6c0b0a9477.png)
<br>

### v) Split and merge HSV Image
<br>
![Screenshot (177)](https://user-images.githubusercontent.com/93992063/227770413-7aae0dd3-aa5c-41df-b75c-9cee739ba2a6.png)

<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
