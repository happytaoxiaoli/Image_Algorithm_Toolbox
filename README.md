# Image_Algorithm_Toolbox　 ![Language](https://img.shields.io/badge/language-Python3-orange.svg) ![AD](https://img.shields.io/badge/东半球最好的-图像算法工具箱-ff69b4.svg) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE.md) 


-----------------


| **`Linux CPU`** | **`Linux GPU`** | **`Mac OS CPU`** | **`Windows CPU`** | **`Windows GPU`** | 
|-----------------|---------------------|------------------|-------------------|---------------|
| ![Travis](https://img.shields.io/travis/rust-lang/rust/master.svg) | ![Travis](https://img.shields.io/travis/rust-lang/rust/master.svg) | ![Travis](https://img.shields.io/travis/rust-lang/rust/master.svg) | ![Travis](https://img.shields.io/travis/rust-lang/rust/master.svg) | ![Travis](https://img.shields.io/travis/rust-lang/rust/master.svg) |


**Update 23-10-2017: It's an image algorithm toolbox entirely written by myself.**

MIT license. Contributions welcome.

**Note :**

Each sub-tool independent of each other, can be used alone.<br>
各子工具之间互相独立，可单独使用。

## Overview

    Image_Algorithm_Toolbox/      root dir  根目录
	     |
	     |
	     +-- Distributing_Tool/   image distributing tool  图片数据分发工具
	     |         |
	     |         +-- distributing.py         main program  主程序
	     |         |
	     |         +-- src/         	   pics to be distributed (need build by yourself)  存放待分发的图片集(需自己新建)
	     |         |
	     |         +-- dst/                    pics be distributed (automatically build by program)  存放已分发的图片集(程序自动新建)	     
	     |
	     |
	     +-- Enhancing_Tool/      image enhancing tool  图片数据增强工具
	     |         |
	     |         +-- sync_enhancing.py       main program  主程序
	     |         |
	     |         +-- src/         	   pics to be enhanced (need build by yourself)  存放待增强的图片集(需自己新建)
	     |         |
	     |         +-- dst/                    pics be enhanced (automatically build by program)  存放已增强的图片集(程序自动新建)
	     |
	     |
	     +-- Formatting_Tool/     format conversion tool  格式转换工具
	     |         |
	     |         +-- format_conversion.py    main program  主程序
	     |         |
	     |         +-- src/         	   pics to be formatted (need build by yourself)  存放待格式转换的文件(需自己新建)
	     |         |
	     |         +-- dst/                    pics be formatted (automatically build by program)  存放同名的已转换文件(程序自动新建)
	     |
	     |
	     +-- Labeling_Tool/       labeling tool  图片标记工具
	     |         |
	     |         +-- labeling.py             main program  主程序
	     |         |
	     |         +-- src/         	   pics to be marked (need build by yourself)  存放待标注的图片(需自己新建)
	     |         |
	     |         +-- dst/                    pics be marked (automatically build by program)  存放同名的已标注文件(程序自动新建)
	     |
	     |
	     +-- Resizing_Tool/       resizing tool  图片缩放工具
	     |         |
	     |         +-- pic_resizing.py         main program 1  主程序1(只缩放图片)
	     |         |
	     |         +-- sync_resizing.py        main program 2  主程序2(同步缩放图片和标记文件)
	     |         |
	     |         +-- src/         	   pics to be resized (need build by yourself)  存放待缩放的数据集(需自己新建)
	     |         |
	     |         +-- dst/                    pics be resized (automatically build by program)  存放同名的已缩放(程序自动新建)	    数据集 
	     |
	     |
	     +-- README.md            manual of project  说明手册
	     |
	     |
	     +-- LICENSE.md           license of project  许可证
	     |
	     |
	     +-- requirements.txt     environment required for this program  环境要求

## Usage


### image distributing tool  图片数据分发工具

1. ```cd Distributing_Tool/```；
2. Build ```src/``` folder and copy dataset into it；
3. Run ```distributing.py```；
4. Processed images automatically be saved into ```dst/``` folder.

### image enhancing tool  图片数据增强工具

1. ```cd Enhancing_Tool/```；
2. Build ```src/``` folder and copy dataset into it；
3. Run ```sync_enhancing.py```；
4. Processed images automatically be saved into ```dst/``` folder.

### format conversion tool  格式转换工具

1. ```cd Formatting_Tool/```；
2. Build ```src/``` folder and copy dataset into it；
3. Run ```format_conversion.py```；
4. Processed images automatically be saved into ```dst/``` folder.

### labeling tool  图片标记工具

1. ```cd Labeling_Tool/```；
2. Build ```src/``` folder and copy dataset into it；
3. Run ```labeling.py```；
4. Processed images automatically be saved into ```dst/``` folder.

### resizing tool  图片缩放工具

1. ```cd Resizing_Tool/```；
2. Build ```src/``` folder and copy dataset into it；
3. Run ```pic_resizing.py``` or ```sync_resizing.py```；
4. Processed images automatically be saved into ```dst/``` folder.

## Tutorial of labeling tool

Open the labeling tool:<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/0.png)

Input the name of sub folder:<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/2.png)

Automatically load corresponding Image:<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/3.png)

Automatically create document of the same name:<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/5.png)

Specify the coordinates use single left-click, every two clicks to determine a diagonal box. Right click cancel.:<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/4.png)

Automatically create messages of marked boxes:<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/6.png)

Please enjoy the labeling process (≧▽≦)y :<br>
![](https://github.com/parnec/Labeling_Tool/blob/master/.demo/7.png)


## Requirements

1. Python3.x
2. OpenCV3.x

## Possible problems

```AttributeError``` may met when using python2.

1. Replace the head lines:
```python
import tkinter as tk
import tkinter.messagebox
```
&emsp;&emsp;with:
```python
import Tkinter as tk
from Tkinter import *
import tkMessageBox
```

2. Replace ```tk.messagebox.askyesno```(appear twice in *line 241、255*) with ```tkMessageBox.askyesno```.

Then error will be fixed.

## License

[MIT](https://github.com/parnec/Labeling_tool/blob/master/LICENSE.md)

