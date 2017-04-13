Demo Video @ [https://youtu.be/syIXeapmQnE](https://youtu.be/syIXeapmQnE)  
# Zhaorui's work for course project  
An implementation of markerless augmentment reality, based on openCV3.0 bindings for python3.  

Ideas come from book: Mastering OpenCV [https://github.com/MasteringOpenCV/code](https://github.com/MasteringOpenCV/code)   
copyright by Packt Publishing 2012  

## Dependencies
- openCV 3.0+
- python 3.4+
- numpy
- matplotlib

## To run  
Ensure to have openCV3 for python in environment  
```
python3 main.py {static, capture} {sift, orb}
```

## Results
Test Result 1             |  Test Result 2             |  Test Result 3
:-------------------------:|:-------------------------:|:-------------------------:
![](https://github.com/TeppieC/markerless-ar-python/blob/master/testResults/result1.png "Test result 1")  |  ![](https://github.com/TeppieC/markerless-ar-python/blob/master/testResults/result2.png "Test result 2")  |  ![](https://github.com/TeppieC/markerless-ar-python/blob/master/testResults/result3.png "Test result 3")

## Trouble Shooting  
```  
OpenCV Error: Bad argument (image is empty or has incorrect depth (!=CV_8U)) in detectAndCompute, file /Users/zhaorui/opencv_contrib/modules/xfeatures2d/src/sift.cpp, line 770  
Traceback (most recent call last):  
  File "main.py", line 195, in <module>  
    app.main()  
  File "main.py", line 92, in main  
    self.roi = ROI(cropImage, self.alg)  
  File "/Users/zhaorui/414/opencv-ar-project/ROI.py", line 23, in __init__  
    self.keypoints, self.descriptors = sift.detectAndCompute(self.image, None)  
cv2.error: /Users/zhaorui/opencv_contrib/modules/xfeatures2d/src/sift.cpp:770: error: (-5) image is empty or has incorrect depth (!=CV_8U) in function detectAndCompute   
```
Sol: Retry the program. Be sure to drag out a rectangle using your mouse.
