# FaceAverage
人脸合成加68点计算
## 效果展示
![error](https://github.com/xjkj123/FaceAverage/blob/master/doc/show.png)
## 引用库
```python
import os
import cv2
import numpy as np
import math
import sys
import dlib
import tqdm
````

## 为何做此项目
  偶然间发现了学校教务系统的API有漏洞,手头多出上千张一寸照不知如何处理,遂想到如此项目
  
##
  核心代码来自average-face-opencv-c-python-tutorial，在人脸特征68点识别上调用的dlib的方法，以及需要训练好的shape_predictor_68_face_landmarks.dat,训练文件未在代码内贴出,使用时请网络下载此文件放进源码根目录即可
  
# 文件说明
  face68point.py 计算脸部68个特征点
  
  faceAverage.py 脸部合成
  
  /rawimage/存放照片以及特征点文件,已给出22张实例图片
  
# 使用说明
  只需启动faceAverage.py,并把图片放入/rawimage中
  
```python
if __name__ == '__main__' :
  face68point.point68('rawimage/') #图片路径
  average('rawimage/','.bmp') #图片路径+格式
```
  
# 以上操作即可自动计算脸部特征和合成了
