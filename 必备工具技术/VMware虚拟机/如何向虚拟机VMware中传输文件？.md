# ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/29/20201229203912.png)如何向虚拟机VMware中传输文件？

### 前言：

我一般情况下使用VMware虚拟机都是为了实验测试用的，比如需要安装某个软件的时候，为了避免一些错误的操作而导致安装出错。所以对于一些较为复杂的软件，比如需要配置一些环境变量之类的软件，一般我都选择虚拟机进行安装的演习，同时也可以截图写写记录。

虚拟机的最大好处就是可以拍快照，这是我选择使用它的最重要原因。我可以在安装前拍一个快照，如果在安装过程中出现错误的话，那么我就直接返回初始状态进行重新安装。如果你试过重新安装MySQL这个痛苦过程的话，那么可能你就能体会到拍一个系统快照的优越性。

新装的VMware系统，至少在Windows虚拟操作系统之中是不能够直接在你的电脑系统中将文件直接拖拽进入虚拟机系统中去的，为了解决这个问题，我查询了网络上的资料，跟着教程尝试了一遍，结果把问题解决了，所以下面就是我跟着教程的操作结果。



### Step1：安装VMware Tools

首先点击菜单栏中的虚拟机，再点击安装VMware Tools。

「虚拟机」➡「安装VMware Tools」

可能需要等几分钟，等它安装成功之后再打开虚拟机的操作系统界面。

![image-20210107181933249](https://i.loli.net/2021/01/07/Ys6baUzSo7ftw4V.png)



### Step2：在虚拟机中安装VMware Tools

进入操作系统界面之后，我们可以按快捷键**「windows+R」**键，弹出运行窗口，在窗口中输入**「D:\setup.exe」**，在虚拟机系统中安装VMware Tools工具。

![image-20210107182050475](https://i.loli.net/2021/01/07/BIQwtmrRYn81CUA.png)

如果你不想跟着上面的操作的话，那么可以点击**「我的电脑」**，再双击**「D盘」**，进行VMware Tool的安装。

![image-20210107182334490](https://i.loli.net/2021/01/07/lOLGg4SucP759za.png)



### Step3：VMware Tools安装

首先需要对软件包进行授权，点击接受就行了。

![image-20210107182117564](https://i.loli.net/2021/01/07/jmsH6USeoXvfGkp.png)

等待十几秒就可以弹出安装界面。

![image-20210107182140124](https://i.loli.net/2021/01/07/HWTxBJwDg8at7bC.png)

![image-20210107182200755](https://i.loli.net/2021/01/07/FVi8QLDe27gzXJb.png)

在这里建议**「经典安装」**。

![image-20210107182220050](https://i.loli.net/2021/01/07/new1QE76lfDchJF.png)

**「点击安装」**

![image-20210107182235226](https://i.loli.net/2021/01/07/QHGml5pxMCa96jJ.png)

![image-20210107182252930](https://i.loli.net/2021/01/07/ohwcEdGmaR3x9QI.png)

等待几分钟就安装完成了

![image-20210107182355097](https://i.loli.net/2021/01/07/ADwESsFb2KYHQiC.png)



### Step4：重启虚拟机系统

![image-20210107182411990](https://i.loli.net/2021/01/07/13gj8TC54x6Uahf.png)

![image-20210107182425179](https://i.loli.net/2021/01/07/87noUFZ9tT4SIzk.png)



### Step5：测试是否能够向虚拟机系统中传输文件

![image-20210107182546315](https://i.loli.net/2021/01/07/637cBJxXS2kHzTZ.png)

显然，在我这里是可以直接将Readme文件拖进虚拟机中去的。所以整个过程已经成功完成。



<br><br>



[↪返回首页](https://nothing-lin.github.io/NothingLin-s-knowledge-space/)



<br><br>

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231121340.png)