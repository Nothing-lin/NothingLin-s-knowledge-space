# ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/29/20201229203912.png)如何搭建Android开发环境并运行helloworld项目？

![image-20210302211054016](https://i.loli.net/2021/03/02/w8Zopeanhx5XgjP.png)

### 全文概要：

- Android studio 安装
- JDK升级至1.8版本
- 安装雷电模拟器
- Android studio 开发环境配置
- 运行简单的helloworld项目



### 参考文章：

- [android studio连接雷电模拟器](https://blog.csdn.net/yan_jingyu/article/details/81988370)
- [android studio新建工程Unresolved dependencies报错](https://blog.csdn.net/qq_33985931/article/details/103933494)
- [android studio的安装，史上最详细(超多图)！！](https://blog.csdn.net/qq_41976613/article/details/91432304)



### 前言：

学校这个学期开设了Android入门课程，在第一天上课的时候就在Android环境搭建上折腾了半天--补偿性心理作祟--决定把踩坑浪费掉的时间都通过记录笔记的形式补偿回来。总结一下踩过的坑：

- **网速相关**：安装过程需要下载相关的依赖包，由于我们在国内网络环境导致相关依赖包下载速度很慢，所以这个我们需要耐心等待才行。
- **安装路径**：Android studio需要耗费比较大的空间资源，所以安装路径尽量选择非C盘安装，还有就是安装的路径不要出现中文，尽量保证路径的形式以英文字母的形式出现，否则回导致一些奇怪的错误。
- **Gradle project sync failed错误**：目前还不清楚导致这一个错误的原因，我目前猜测是依赖下载的问题，本文的hello world项目运行是正常运行的，但是不知道为什么之前的安装操作会导致**Gradle project sync failed错误**。



### 1、Android studio 安装

![image-20210302161337108](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302225738.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302225832.png)



> Android studio下载地址：http://www.android-studio.org/



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302225844.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302225857.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302225917.png)



如果系统盘的空间资源比较紧缺的话，建议安装路径放在非系统盘（C盘）上...



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302225942.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230002.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230019.png)





### 2、JDK升级至1.8版本

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230037.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230041.png)



> JDK下载地址 ： https://www.oracle.com/java/technologies/javase-downloads.html

jdk建议下载1.8版本以上的--并且选择exe的文件形式更容易安装。

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230101.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230120.png)



选择JDK的安装路径。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230141.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230157.png)



这一个是安装JRE，一般安装JDK的时候都需要JRE运行环境来配合，所以最好都装上JDK和JRE。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230217.png)



选择JRE的安装路径。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230232.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230249.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230306.png)

使用命令`java -version`查看JDK的版本。





### 3、安装雷电模拟器

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230322.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230329.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230344.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230436.png)



选择雷电模拟器的安装路径



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230503.png)

等待下载完相关依赖文件即可安装完毕，可以稍后再打开雷电模拟器。





### 4、Android studio 开发环境配置

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230522.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230545.png)



因为我们这里是第一次安装Android studio ，所以我们没有以前的配置备份文件，我们选择没有就OK。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230605.png)



我们这里并没有代理地址，所以我们这里选择“取消”。

下面由于没有国外的代理地址，所以下载相关依赖的时间会比较长，所以建议在这里需要耐心等待。。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230625.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230645.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230713.png)



这里我的选择是Standard标准安装，Custom自定义安装的话大家可以尝试一下。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230724.png)



这里可以选择夜间主题或者是白天主题。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230733.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230745.png)



这里需要看你的电脑配置，我的电脑是8G内容，所以我就只分配给它2G的运行内存，不然在运行这个模拟器的时候我的电脑会很卡。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230758.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230811.png)



耐心等待。。。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230823.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230836.png)



模拟器设备配置。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230842.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230848.png)



我选择的系统镜像是上图所示的镜像，大家可以根据自己的需求选择。红色字体部分的相关依赖文件也是需要进行安装的，大家需要注意一下。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230855.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230902.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230907.png)



### 5、新建一个hello world项目

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230912.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230916.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230919.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230923.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230928.png)



这里需要注意，方框部分的选项我在勾选的时候--新建项目时出现了**Gradle project sync failed错误**，所以为了项目能够正常运行，这里建议取消勾选。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230932.png)



等待相关的依赖下载和第一次使用时的初始化配置，这个过程也需要下载一些依赖文件，所以这里也会消耗一些时间，所以建议大家在这一步耐心等待。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230939.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302230944.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302231118.png)



在这里我们需要打开雷电模拟器。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302231129.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302231204.png)



我们打开雷电模拟器之后，Android studio就能自动识别到设备，选择第一个USB选项设备即可，不过第一次使用的时候需要下载相关依赖，这里也需要等待一下。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302231212.png)



下载相关依赖并在模拟器中运行项目。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/2/20210302231217.png)

helloworld项目成功运行！！！！



<br><br>



[↪返回首页](https://nothing-lin.github.io/NothingLin-s-knowledge-space/)



<br><br>

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231121340.png)