# Visual Studio 2010 + OpenCV 2.4.9 安装配置

&emsp;&emsp;2017年暑假，学校要求博士生参加暑期社会实践，服务各地方的单位。经过选课，我去了位于济南的翼菲自动化科技有限公司。这家公司主要从事工业机器人的开发，产品主要用于轻工业产品的生产线，例如药品、食品、日化等等。目前的主要产品是一款名为泰山3的并联机器人，采用3自由度Delta型机器人。  
&emsp;&emsp;我选择的项目是机器视觉，主要利用一个三维视觉摄像头（[图漾科技 RGB-D 传感器](http://www.percipio.xyz/rgbd/)）识别物体信息，辅助机械臂进行操作。  

项目的第一步需要进行环境配置，主要包括3个：
- OpenCV
- PCL
- Halcon

我将分别在三个文档中记录安装和配置的过程。

由于需要在工业机器人上使用，而实际在工业现场多数还是使用32位的控制器，具体开发环境则与公司的工作人员保持一致，使用Visual Studio 2010。其余开发环境力求与公司工作人员一致，配置如下：
- OpenCV 2.4.9
- PCL 1.8.0
- Halcon 11

另外，多说一句，Visual Studio 2010的版本还是比较老的，那时候VS还不够智能，代码不全功能还很搓，为了开发方便，推荐使用JetBrains的[Resharper](https://www.jetbrains.com/resharper-cpp/)，神器（我是JetBrains的脑残粉）。学生的话利用学校邮箱可以申请到免费许可证，虽然有效期只有一年，但是到期后后仍旧可以利用学校邮箱续期，所以只要还在学校就可以一直使用。

## 一、OpenCV下载

OpenCV采用的是2.4.9版本，目前已经出到了OpenCV3，可以根据自己的实际需要选择合适的版本。

想要下载历史版本可以到[OpenCV-Releases](http://opencv.org/releases.html)来下载。如果仍旧找不到需要的版本的话，可以直接到[GitHub上](https://github.com/opencv/opencv/releases)来找。

为了图省事，我直接下载了2.4.9的Win Pack，是一个exe程序。

双击运行后，选择安装路径

![opencvinstall](opencv_install.jpg)

点击Extract，完成安装。安装完毕后目录下分别有source和build文件夹。
![opencvinstalldir](opencv_install2.jpg)

然后需要在系统环境变量中的PATH项中，添加OpenCV的安装路径




