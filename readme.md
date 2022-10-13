

# rolabelimg 打旋转方框标签工具保姆级安装使用指南
![在这里插入图片描述](https://img-blog.csdnimg.cn/cd2c8060d92c477095be3c7ea54b438c.png)

原作者Github链接: [https://github.com/cgvict/roLabelImg](https://github.com/cgvict/roLabelImg)

Up Github链接(附样例)：[https://github.com/Samsara0Null/roLabelImg](https://github.com/Samsara0Null/roLabelImg)

百度网盘(附样例、附exe)链接：[https://pan.baidu.com/s/1FOxz3gAXcj3ZVQPtX11vqw](https://pan.baidu.com/s/1FOxz3gAXcj3ZVQPtX11vqw)提取码：MBJC 

CSDN主页链接: [https://blog.csdn.net/noneNull0?type=blog](https://blog.csdn.net/noneNull0?type=blog)

Bilibili视频演示讲解链接: [https://www.bilibili.com/video/BV1GR4y1X7fq/?vd_source=a6067b731745325c01a4edfa46bf5a04](https://www.bilibili.com/video/BV1GR4y1X7fq/?vd_source=a6067b731745325c01a4edfa46bf5a04)
### 背景知识：
&emsp;&emsp;相较原有的水平矩形方框标签，OBB定向包围框(oriented bounding box)即旋转方框标签可更加贴合目标，其主要信息由一个五元组组成(cx，cy，w，h，angle)。
![在这里插入图片描述](https://img-blog.csdnimg.cn/65e02f5dd11a4551a7828044b25a7722.png)

&emsp;如上图所示，width是图像的宽，height是图像的高,depth是图像的通道数
&emsp;cx, cy表示bndbox的中心点坐标(坐标系方向和一般的图像坐标系相同，左上角为原点，向右为x正方向，向下为y正方向)；
&emsp;h和w是标记目标的高和宽；
&emsp;angle是旋转角度信息，水平bndbox，angle=0，,顺时针方向旋转，得到的角度值是一个弧度单位的正值，且旋转一周为pi，没有负值。
### 安装过程：
- 1、下载rolabelimg源代码（链接见开头）


&emsp;可选择封装好的exe直接双击运行，直接跳过2、3

![在这里插入图片描述](https://img-blog.csdnimg.cn/0fe334f5f4c2487a8e545f1d9825a02c.png)
- 2 、在Anaconda运行窗口中依次输入创建环境
```javascript
conda create -n rolabelimg python=3.8
activate rolabelimg
conda install pyqt
conda install lxml
```

- 3、cd到下载路径中，输入代码运行即可
```javascript
pyrcc5 -o resources.py resources.qrc 
python roLabelImg.py
```




### 常用快捷键：
快捷键 | 作用|原文
-------- | -----|-----
| Ctrl + u   |从目录加载所有图像| Load all of the images from a directory    |
| Ctrl + r   |更改默认注释目标目录| Change the default annotation target dir   |
| Ctrl + s   |保存|  Save                                       |
| Ctrl + d   |复制当前标签和矩形框 | Copy the current label and rect box        |
| Space      |将当前图像标记为已验证|  Flag the current image as verified         |
| w          |创建矩形框 | Create a rect box                          |
| e          | 创建旋转矩形框| Create a Rotated rect box                  |
| d          |下一个图像 | Next image                                 |
| a          |上一个图像|  Previous image                             |
| r          | 隐藏/显示旋转矩形框| Hidden/Show Rotated Rect boxes             |
| n          |隐藏/显示普通矩形框 | Hidden/Show Normal Rect boxes              |
| del        | 删除所选矩形框| Delete the selected rect box               |
| Ctrl+滚轮     | 放大| Zoom in                                    |
| Ctrl+滚轮  |缩小 | Zoom out                                   |
| ↑→↓←       | 移动选定矩形框的按键| Keyboard arrows to move selected rect box  |
| zxcv       |旋转所选矩形框的按键 | Keyboard to rotate selected rect box       |


<span style="color:pink;">Author: MBJC</span>  
<span style="color:pink;">Last modification time: 2022/10/9 17:56</span>
