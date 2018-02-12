---
title: OpenCV 基础总结
date: 2018-02-09 10:05:51
categories: 计算机视觉
tags:
    - OpenCV
description: OpenCV C++基础总结, 主要是一些矩阵操作。
---
## 图像读取、保存、显示
### 1) 读取
using namespace cv;

Mat img = imread("/path/to/image/img.jpg", CV_LOAD_IMAGE_UNCHANGED);

CV_LOAD_IMAGE_UNCHANGED = -1 // IMREAD_UNCHANGED

CV_LOAD_IMAGE_GRAYSCALE = 0  // IMREAD_GRAYSCALE

CV_LOAD_IMAGE_COLOR = 1      // IMREAD_COLOR

CV_LOAD_IMAGE_ANYDEPTH = 2   // IMREAD_ANYDEPTH

CV_LOAD_IMAGE_ANYCOLOR = 4   // IMREAD_ANYCOLOR

### 2) 保存
bool imwrite( const string& filename, InputArray img, const vector<int>& params=vector<int>() );

参数分别是：含后缀图像名，图像矩阵，图像保存参数如压缩等级等。

### 3) 显示
void namedWindow( const string& winname, int flags=WINDOW_AUTOSIZE );

命名窗口，其中参数WINDOW_AUTOSIZE表示自适应成图像大小，且不可手动调整大小。WINDOW_NORMAL则可以自由调整窗口大小。

void moveWindow(const String &winname, int x, int y); // 水平, 竖直方向

移动指定窗口的位置。

void imshow(const string& winname, InputArray mat);

显示图像mat到特定窗口。

destroyWindow(); // destroyAllWindows();

关闭窗口释放内存。

## Mat矩阵的选取、加减乘除


## Mat的统计API

##
