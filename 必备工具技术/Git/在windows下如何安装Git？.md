# ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/29/20201229203912.png) 在windows下如何安装Git？

### Step1：先到git官网下载window版git安装包

官网地址：[点击我](https://git-scm.com/download/win)

我的电脑cpu是64位的，因为每个人的电脑配置都不一样，可以根据自己的选择进行下载。

下载点击：

- 32-bit Git for windows Setup
- 64-bit Git for windows Setup

![image-20210105165521725](https://i.loli.net/2021/01/05/83FHPgerbY2hEvV.png)



### Step2:安装包在本地准备就绪



![image-20210105165604523](https://i.loli.net/2021/01/05/haoZnEfiQK6T1Fr.png)



### Step3:安装包授权安装

一般在window10的环境下，我们对安装包进行安装的时候都需要给安装包进行授权，这样才能够进行正常的安装。

![image-20210105165624591](https://i.loli.net/2021/01/05/9ApBqlYhnW53LSc.png)



### Step4:接受git软件的使用协议



![image-20210105165649775](https://i.loli.net/2021/01/05/eOM7rqBnPgWHd9U.png)



### Step5：选择git的安装路径

下面可以根据自己的喜好或者电脑的容量情况，选择一个合适的盘位进行安装。如果你C盘容量足够大的话，那么还是建议安装在C盘中。

![image-20210105165718046](https://i.loli.net/2021/01/05/UbnjHJB3gvMkfQO.png)



### Step6：选择安装选项

下面的安装选项中一般来说是默认就行了，不过你也可以根据自己的需求进行选择。

```
口----添加图标
	|----在桌面添加快捷图标
	
口----在鼠标右键快捷菜单中添加下列选项
	|----Git Bash Here	(git命令行界面）
	|----Git GUI Here	(git图形管理界面)

口----是否安装Git扩展插件LFS

口----是否将.git*开头的文件与系统默认文本编辑器关联

口----是否和命令行关联.sh结尾的文件

口----是否在所有cmd控制台窗口中使用TrueType类型的字体

口----是否自动检测新版本且自动更新
```

![image-20210105165810253](https://i.loli.net/2021/01/05/zXV2sqCcGaTY8ZD.png)



### Step7：修改git在windows10下的开始菜单中的名称

在这里你可以修改你的开始菜单中git的名称，当然你也可以选择不在开始菜单栏中创建git文件夹。

![image-20210105165834207](https://i.loli.net/2021/01/05/XWUT31VpFytN5Iq.png)![image-20210105174021572](https://i.loli.net/2021/01/05/HlzYkbKByDNpGTs.png)



### Step8：选择Git文件默认的编辑器

这一步是为.git后缀的文件设置默认的打开编辑器，一般来说我们很少会用到.git后缀结尾的文件，所以这一步直接默认就可以了。

这里默认使用的编辑器是Vim编辑器。

![image-20210105165903442](https://i.loli.net/2021/01/05/XVbe2fAcy9QkrJG.png)



### Step9：为Git设置PATH环境

```
口----只从Git Bash命令行控制界面中使用git

口----使用来自cmd命令行界面的git或者是第三方的软件git工具来使用git

口----从命令提示符中使用git可选Unix工具
```

- 如果选择第一项的话，那么我们只能够通过Git Bash Here，git自带的命令行界面使用git，不能再windows下的cmd上使用git。我个人不是很推荐这个
- 如果选择第二项的话，相对使用git的权限会高一点。我们可以使用Windows自带的cmd命令行进行使用git，同时像Github桌面版这类第三方软件也是可以直接使用本地安装的git进行GitHub远程仓库的文件传输的。我个人推荐使用第二项。
- 第三项不知道是干啥的，有兴趣的话可以了解一下，我个人推荐使用第二项，同时默认也是第二项，所以默认吧。

![image-20210105165923008](https://i.loli.net/2021/01/05/IYp7g2NqA1wHZxL.png)



### Step10：选择http的后端传输方式

>   第一个选项是“使用 OpenSSL 库”。服务器证书将使用ca-bundle.crt文件进行验证。这也是我们常用的选项。
>
>   第二个选项是“使用本地 Windows 安全通道库”。服务器证书将使用Windows证书存储验证。此选项还允许您使用公司的内部根CA证书，例如通过Active Directory Domain Services 。

上面的解释是我拷贝网上的资料，我也不懂这一个选项有什么关键作用，我暂时先跳过这一步。

一般来说我们对于git的后端的http传输方式，默认选择第一个。

![image-20210105165941656](https://i.loli.net/2021/01/05/dkyWsSoDeNFwAgC.png)



### Step11:选择git bash here界面的样式

![image-20210105170006806](https://i.loli.net/2021/01/05/LMIWrmHGKqjOh5J.png)



### Step12:配置终端模拟器与git bash一起使用

>   第一个选项是“使用MinTTY（MSYS2的默认终端）”。Git Bash将使用MinTTY作为终端模拟器，该模拟器具有可调整大小的窗口，非矩形选择和Unicode字体。Windows控制台程序（例如交互式Python）必须通过“ winpty”启动才能在MinTTY中运行。
>
>   第二个选项是“使用Windows的默认控制台窗口”。Git将使用Windows的默认控制台窗口（“cmd.exe”），该窗口可以与Win32控制台程序（如交互式Python或node.js）一起使用，但默认的回滚非常有限，需要配置为使用unicode 字体以正确显示非ASCII字符，并且在Windows 10之前，其窗口不能自由调整大小，并且只允许矩形文本选择。

这里我也不清楚是干什么的，上面的文字拷贝于互联网。

![image-20210105170022452](https://i.loli.net/2021/01/05/62CrL1wGn5Eyhuq.png)



### Step13:配置其他选项

>   第一个选项是“启用文件系统缓存”。文件系统数据将被批量读取并缓存在内存中用于某些操作（“core.fscache”设置为“true”）。 这提供了显著的性能提升。
>
>   第二个选项是“启用Git凭证管理器”。Windows的Git凭证管理器为Windows提供安全的Git凭证存储，最显着的是对Visual Studio Team Services和GitHub的多因素身份验证支持。 （需要.NET Framework v4.5.1或更高版本）。
>
>   第三个选项是“启用符号链接”。启用符号链接（需要SeCreateSymbolicLink权限）。请注意，现有存储库不受此设置的影响。

上面的文字拷贝于互联网。

这一部分的选项配置不是很清楚干什么用的，一般选择默认选项，进行下一步就行了。

![image-20210105170036201](https://i.loli.net/2021/01/05/Lr1vhg9J5DQlYqx.png)



### Step14:等待安装···

![image-20210105170103904](https://i.loli.net/2021/01/05/QV21zGciPB4unZ8.png)



### Step15：完成安装界面

- 第一个选项是选择现在就启动Git Bash命令行界面
- 是否需要查看所有的git版本相关信息（该选项会打开一个网站） 

![image-20210105170123875](https://i.loli.net/2021/01/05/HIAxUQildvXgc7Z.png)



### Step16：检测是否安装成功

再桌面单击右键，看是否新增两个选择项

- Git GUL Here
- Git  Bash Here

![image-20210105170146931](https://i.loli.net/2021/01/05/PM3G8xymetdbIuh.png)

在Git Bash中输入下面这条命令行指令（是不是很想windows的cmd？）

```
git --version
```

如果显示git的版本信息的话，那么说明你已经安装成功了。

![image-20210105170251913](https://i.loli.net/2021/01/05/PrVLoCikgpsyFNW.png)







[↪返回首页](https://nothing-lin.github.io/NothingLin-s-knowledge-space/)



<br><br>

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231121340.png)