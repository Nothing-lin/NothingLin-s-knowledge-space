# ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/29/20201229203912.png)如何搭建vue.js开发环境？

### ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304114902.png)

### 前言：

本文是基于我们老师给的教材进行编辑的，因为我的系统已经安装了相关环境--但是我没有及时记录下来--唉，只能借用老师的文档进行编写了。



### 全文概要：

- 安装Node.js环境
- 安装cnpm淘宝镜像
- 搭建vue开发环境
- 启动第一个vue项目



### 安装Node.js环境

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304114917.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304114937.png)

> 首先需要到node.js官网中去下载相关的安装包，下载地址：[http://nodejs.cn/download/](https://links.jianshu.com/go?to=http://nodejs.cn/download/)

关于node.js的安装其实是傻瓜式安装的模式，只需要一直点下一步就OK了。



##### 检测是否安装成功：

关于检测是否成功安装需要知道两条指令：`node -v` 和 `npm -v`。

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304115000.png)



安装好之后需要对npm安装的全局模块所在路径以及缓存所在路径进行环境配置。



##### npm全局安装：

```cmd
npm install express -g
```

全局安装的目的是--你可以在任何一个CMD指令界面当中执行npm开头的指令，也就是随便打开一个命令行界面就行，不需要再到可执行文件目录下去执行npm指令了。



##### 设置缓存文件和全局安装文件的路径存放：

首先在node.js安装目录下创建两个文件夹`node_cache`和`node_global`。其中一个是用来存放缓存文件的，另一个是用来存放我们全局安装的文件。为什么要这样做呢？一般默认情况下，缓存文件都是存放在系统盘中的，如果你的系统盘比较充裕的话可以跳过此步骤，如果需要节省C盘空间的话可以按照下面的步骤进行。

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304115013.png)

```cmd
//设置全局安装文件的路径
npm config set prefix "D:\Program Files\nodejs\node_global"
//设置缓存文件的存放位置
npm config set cache "D:\Program Files\nodejs\node_cache"
```



##### node环境变量配置：

首先打开环境变量配置的地方。

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304115031.png)![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304115106.png)





### 配置cnpm

由于网络原因，国内访问npm的速度会比较慢，这里通过设置国内的淘宝镜像来访问npm。

```cmd
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

检查是否安装成功：`npm -v` 和 `cnpm -v`



安装cnpm的全局环境：

```cmd
cnpm install express -g
```



### 搭建vue开发环境

安装全局vue-cli脚手架，用于帮助搭建vue框架的模板项目。

```cmd
 cnpm install vue-cli -g 
```

检测是否安装成功：`vue` 和`vue -V`。



### 创建一个vue模板项目

首先我们需要找到一个路径来存放我们创建的项目，在该目录下点击`shift+右键`打开powershell。

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304115144.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304121606.png)



##### 使用webpack打包工具来启动vue项目

```cmd
vue init webpack hellovue（项目文件名）
```



指令一旦输入--接下来将会出现选择项，除了`vue-router`选择`yes`，其余一律`no`。



![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304121611.png)

上面我觉得选择`yes,use npm`就OK了，当然也可以选择`No,I will handle that myself`,应该没什么影响。

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304121648.png)

```cmd
//进入hellovue项目文件中
cd hellovue

//使用cnpm进行安装
cnpm install

//使用cnpm指令进行项目启动
cnpm run dev
```

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304121700.png)

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2021/3/4/20210304121710.png)



在这里能够启动vue模板项目就说明相关的环境已经安装和配置好了，接下来就需要进入vue的细节学习了。



<br><br>



[↪返回首页](https://nothing-lin.github.io/NothingLin-s-knowledge-space/)



<br><br>

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231121340.png)