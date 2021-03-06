# ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/29/20201229203912.png)在VMware下如何安装windows 10系统？

### Step1：点击创建新的虚拟机

![image-20210105194740362](https://i.loli.net/2021/01/05/Osj3liR7E2Uuk5I.png)



### Step2：选择自定义（高级）选项

选择典型安装也可以的，只不过我之前看其他教程的时候他们是选择自定义安装，我也还不清楚两者有什么区别。本期是选择自定义安装虚拟机系统。

![image-20210105194840459](https://i.loli.net/2021/01/05/9XgeFY4DQMCnitE.png)



### Step3：选择稍后再安装操作系统

选择稍后再安装操作系统可能更好地配置虚拟机地性能。

![image-20210105194934895](https://i.loli.net/2021/01/05/bUj4DXK1TEvVLkR.png)



### Step4：选择需要安装的系统类型

因为本期是windows在VMware虚拟中的安装，所以这里选择的是Mcrosoft Windows类型的操作系统，我提前准备好的系统镜像（.iso镜像文件)因为是Windows 10 64位的，所以我就选择相关选项。

大家可以根据自己准备好的镜像文件的类型来对应选择相关的选项。

![image-20210105195114271](https://i.loli.net/2021/01/05/Oy58fXLHMVquzxv.png)



### Step5：选择你的虚拟机系统的安装位置

在这一步中，你可以设置你的虚拟机的名称、虚拟机系统的安装位置。

注意，这里特别不推荐你把虚拟机系统安装到C盘（系统盘）中，这不是一种明智的选择。因为虚拟机消耗的存储空间是非常大的，一旦你安装到系统盘，这样你的系统盘将会很快爆满，从而导致你电脑的运行速度会变得特别糟糕。

我是另外准备好一块机械硬盘充当移动硬盘来存储虚拟机系统的相关文件，这样的话就不会消耗电脑本身里面的存储资源。我个人特别推荐你去淘一块机械硬盘来装载操作系统。

![image-20210105195228835](https://i.loli.net/2021/01/05/8lEJ6KcPIwZNUQx.png)



### Step6：选择固件的类型

在这里有BIOS和UEFI两个选项，因为我对这两个固件类型并不了解，并不知道这有什么用，所以在这里我选择了默认选项，默认选项是UEFI这个选项。

大家可以选择默认即可。

![image-20210105195314699](https://i.loli.net/2021/01/05/mpVSgItke7ZRFNU.png)



### Step7：设置虚拟机的处理器配置

这里是根据你的电脑资源为虚拟机系统分配一些你的电脑的剩余资源，也就比如：

我的电脑是8g内存，4核4线程的处理器。如果我为虚拟机分配了4g内存，2个处理器的话。那么每当我在电脑中运行虚拟机的时候，电脑就会分配了4g内存和2个处理器给你的虚拟机。那么你的电脑就还剩下4g内存和2个处理器。相当于你的虚拟机系统会共享你的电脑硬件资源。

所以，如果你的电脑配置不是很高的话，为了保证你的电脑不因虚拟机拿去太多资源而导致卡机的话，建议分配给虚拟机的资源不要太多。

> **内存一般分配2g和处理器分配1个处理器和1个处理器内核数量即可。**

在下面的选项中可以选择**2➡1、4➡1**。先不要分配太多，不然你的电脑会非常卡顿。

![image-20210105195359303](https://i.loli.net/2021/01/05/ZQk572SGIV4aLcE.png)

下面的内存资源分配，一般选择2g即可。

![image-20210105195505347](https://i.loli.net/2021/01/05/qGKPzakwxFyc3rZ.png)



### Step8：虚拟机网络配置

在这一步中，我们选择**“使用网络地址转换（Net）”**选择这一个选项。

为什么要选择这一个选项？一般虚拟机是在你的电脑系统中运行的，对于网络的话直接共享你的电脑系统中的网络，就非常方便。这个选项就是让你的虚拟机直接共享你的电脑网络。

其他选项则需要你配置其他的网络地址进行联网，这样的话就稍微复杂了。

常用的选项一般都是选择**“使用网络地址转换（Net）”**这一个默认选项。

![image-20210105195537442](https://i.loli.net/2021/01/05/gEFkohsBCmaTtry.png)



### Step9：选择输入输出的设备的类型

这一步选择**”LSI Logic SAS“**

大概意思是跟你的电脑系统共享鼠标、键盘等输入输出设备。

![image-20210105195619815](https://i.loli.net/2021/01/05/kYFQThnzwZi93ba.png)



### Step10：选择磁盘类型

这里选择默认选项**”SCSI“**，至于为什么选这个，可能还需要我以后不断学习或许才会明白。

![image-20210105195659692](https://i.loli.net/2021/01/05/gRpUAyWtBnYCMuF.png)



### Step11：新建虚拟磁盘

因为我们这里是第一次安装虚拟机windows系统，我们需要新建一个虚拟磁盘。这个虚拟磁盘是虚拟机系统里面的磁盘。虚拟机里面的系统盘C盘、数据盘D盘等等这些，我们需要在这里选择新建这样的一些盘。

![image-20210105195740782](https://i.loli.net/2021/01/05/rDLVOS9eiWqRg25.png)



### Step12：为虚拟磁盘分配容量

因为我把我的虚拟机系统安装在我80g的机械硬盘中，所以我最高就给他分配70g的磁盘容量。这样进入系统之后，我的虚拟机系统中的磁盘只有一个C盘，C盘容量是70g，也就是我刚刚给他分配的容量。

一般虚拟机是用来学习使用的，所以没有必要分配所有的磁盘空间给虚拟机，分配一定量的空间给虚拟机就行了，如果不够用了后再还可以设置添加容量。

这一步很重要的一点是要选择**”将虚拟磁盘拆分成多个文件“**这一个选项。

![image-20210105195820112](https://i.loli.net/2021/01/05/wW7FT1EeOl2ioAP.png)



### Step13：指定磁盘文件

下面这一步是说，虚拟机将创建一个虚拟系统启动文件，这个文件是以.vmdk结尾的虚拟机系统启动文件。虚拟机就是通过这一个文件来启动系统的。

如果哪一天你把虚拟机卸载了，但是你这个虚拟机安装的这个虚拟系统还没删除的话。也就是我装有windows 10的80g的这个机械硬盘，我拿到其他的电脑的VMware虚拟机中，我只需要通过VMware虚拟机找到我硬盘中以.vmdk结尾的文件就可以启动我的机械硬盘中的虚拟系统了。

![image-20210105195850202](https://i.loli.net/2021/01/05/Hmud2WBvpirgeyS.png)

下面这一步是给我们展示我们刚刚选择创建的系统资源信息。

![image-20210105195920671](https://i.loli.net/2021/01/05/4DCfOIsrqApa9HX.png)



### Step14：编辑虚拟机设置

上面的过程都完成了之后，我们需要点击编辑虚拟机设置，打开后的样子如下图所示：

![image-20210105195959004](https://i.loli.net/2021/01/05/i2RBIZxvMnmpwHX.png)



### Step15：配置系统镜像

我们在虚拟机设置中点击CD/DVD（SATA）选项，如下图所示：

![image-20210105200033145](https://i.loli.net/2021/01/05/JTMYnlcDxR8KjAi.png)

在这里我们**“点击使用ISO映像文件”**，然后找到我们准备好的windows 10 64位系统iso镜像。

![image-20210105200128947](https://i.loli.net/2021/01/05/CtHQK86yYoahMeZ.png)



### Step16：开机配置系统

完成上面的步骤之后，我们点击**“开启此虚拟机选项”**

![image-20210105200156948](https://i.loli.net/2021/01/05/nEU83vSFfHGsAgY.png)

![image-20210105200259330](https://i.loli.net/2021/01/05/So8VXR6EFdqHjrN.png)

![image-20210105200350260](https://i.loli.net/2021/01/05/kZLrGaNjidn2xtg.png)

选择你对应需要的系统版本类型。

![image-20210105202544916](https://i.loli.net/2021/01/05/rq5VDuEFsGWXM8a.png)

点击下一步。

![image-20210105202633444](https://i.loli.net/2021/01/05/DGRMSrFJmv7YQXd.png)

在这一个过程中选择第二个**“自定义选项”**。

![image-20210105202713062](https://i.loli.net/2021/01/05/ILhA9udSbwskzDr.png)

下面我们就看到了我们上面给虚拟机分配的磁盘信息，我们选择整个磁盘，我就不做磁盘拆分成多个盘了，我就只作一个系统盘C盘，并且把系统安装到这个盘中。

> **扩展理解：**
>
> 为什么这里显示70g的未分配磁盘？比如我们的电脑，我刚买了一块80g硬盘插入要装系统的电脑中，电脑就会识别到这一块可用硬盘有80g未分配的磁盘空间，这里是真实硬盘。
>
> 上面我们在80g的真实硬盘中选择划分70g的磁盘空间给虚拟机，相当于给虚拟机一块虚拟硬盘一样。在这一步安装系统中就可以识别出这一块70g虚拟的虚拟硬盘，而不是我们的真实硬盘。

![image-20210105202813977](https://i.loli.net/2021/01/05/ZG4lOWRSau5Yfpg.png)

耐心等待安装。。

![image-20210105202840907](https://i.loli.net/2021/01/05/bXuqRs4AmLnUxyS.png)

![image-20210105202914133](https://i.loli.net/2021/01/05/3oAR75ad4kMNwfV.png)

![image-20210105202938737](https://i.loli.net/2021/01/05/gRxarbEoMfp2w5F.png)

![image-20210105203003088](https://i.loli.net/2021/01/05/seBf9wTyZG25CWH.png)

![image-20210105203046628](https://i.loli.net/2021/01/05/39oUwAm5GBaJ4Y1.png)



### Step17：完成虚拟机Windows 10系统的安装

到这一步就已经完成了虚拟机Windows 10系统的安装了。

![image-20210105203144855](https://i.loli.net/2021/01/05/QFt5NhcEDCgHnP2.png)





[↪返回首页](https://nothing-lin.github.io/NothingLin-s-knowledge-space/)



<br><br>

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231121340.png)