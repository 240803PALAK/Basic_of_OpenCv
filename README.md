# Basic_of_OpenCv
It include the code which can draw different types of shape using OpenCV. It also contain code to blur the image , apply filter on image .


    import cv2 as cv
    import numpy as np
    
    blank=np.zeros((500,500,3),dtype='uint8')
    cv.imshow("Black",blank)
    
    # paint
    blank[200:300,300:400]=0,255,0
    cv.imshow("Green",blank)
    
    cv.rectangle(blank,(0,0),(250,250),(0,255,0),thickness=-1)
    cv.imshow("Rectangle",blank)
    
    cv.circle(blank,(blank.shape[1]//2,blank.shape[0]//2),40,(0,0,255),thickness=-1)
    cv.imshow("Circle",blank)
    
    # text on image
    cv.putText(blank,"Hello",(255,255),cv.FONT_HERSHEY_TRIPLEX,1.0,(0,0,255),2)
    cv.imshow("Text",blank)
    
    cv.waitKey(0)
    
    
    
    # Converting to grayscale
    import cv2 as cv
    
    img=cv.imread('peacock.jpg')
    gray=cv.cvtColor(img,cv.COLOR_BGR2GRAY)
    cv.imshow("Gray",gray)
    cv.waitKey(0)
    
    
    
    # Bluring
    import cv2 as cv
    
    img=cv.imread('peacock.jpg')
    blur=cv.GaussianBlur(img,(3,3),cv.BORDER_DEFAULT)
    cv.imshow("Blur",blur)
    
    cv.waitKey(0)
    
    
    
    # Edge Cascade
    import cv2 as cv
    
    img=cv.imread('peacock.jpg')
    canny=cv.Canny(img,125,175)
    cv.imshow("Canny Edges",canny)
    
    cv.waitKey(0)
    
    
    
    # Eroding
    import cv2 as cv
    
    eroded=cv.erode(canny,(3,3),iterations=1)
    cv.imshow("Eroded",eroded)
    
    cv.waitKey(0)
    
    
    # Resize
    import cv2 as cv
    
    img=cv.imread('peacock.jpg')
    resized=cv.resize(img,(500,500),interpolation=cv.INTER_CUBIC)
    cv.imshow("Resized",resized)
    
    cv.waitKey(0)
    
    
    
    # Croping
    import cv2 as cv
    
    img=cv.imread('peacock.jpg')
    cropped=img[50:200,200:400]
    cv.imshow("Cropped",cropped)
    
    cv.waitKey(0)
    
    
    
    # Flipping
    import cv2 as cv
    
    img=cv.imread('peacock.jpg')
    flip=cv.flip(img,-1)
    cv.imshow('Flip',flip)
    
    cv.waitKey(0)
