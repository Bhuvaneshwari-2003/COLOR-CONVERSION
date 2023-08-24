# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
## Step1:
 Import cv2 and save an image as scolor.jpeg.

## Step2:
 Use imread to read and display the image.

## Step3:
 Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

## Step4:
 Split and merge the image using cv2.split and cv2.merge commands.

## Step5:
 End the program and view the output image windows.

## Program:
```
# Developed By:bhuvaneshwari.s
# Register Number:212221240010
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('aa.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()
# i) Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# ii)Convert HSV to RGB and BGR
#HSV TO RGB
rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2.destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()



# iv)Split and Merge RGB Image
# SPLIT AND MERGE RGB IMAGE

blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
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
Original image:
![image](https://github.com/Bhuvaneshwari-2003/COLOR-CONVERSION/assets/94828604/9e87e072-8153-4fe1-8440-6e0b4c7754f4)
i) BGR and RGB to HSV and GRAY
i) BGR TO HSV
![image](https://github.com/Bhuvaneshwari-2003/COLOR-CONVERSION/assets/94828604/94bc53b9-82bf-43bf-9ab7-d0f2b4d1758c)
ii) BGR TO GRAY 
![image](https://github.com/Bhuvaneshwari-2003/COLOR-CONVERSION/assets/94828604/779a9f4d-4210-4e5e-b212-ac1970a62521)
iii) RGB TO HSV 
![image](https://github.com/Bhuvaneshwari-2003/COLOR-CONVERSION/assets/94828604/e136b695-a312-4ca7-a5cd-9587a44ec3cb)
iv)RGB TO GRAY
![image](https://github.com/Bhuvaneshwari-2003/COLOR-CONVERSION/assets/94828604/512688db-7893-4df1-9db5-e70f393716d9)
ii) HSV to RGB and BGR
i) HSV TO RGB
![image](https://github.com/Bhuvaneshwari-2003/COLOR-CONVERSION/assets/94828604/4d978429-6592-4d6e-ab1f-ad57d216e73f)
## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
