# ![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/29/20201229203912.png) 如何使用GitHub做一个笔记库？

![image-20201229235028831](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/30/20201230005128.png)

> **tips**：这里可能需要你对GitHub和Git有一定的认识和了解。不认识这些也不要紧，可以先跟着教程一步一步地完成，或许在某个瞬间就突然理解了呢？

<br>

### Step1：创建本地仓库

我们第一步需要在本地创建一个文件仓库，如图所示：



![image-20201231002631520](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010428.png)

可以根据个人的喜好创建一些目录分类作为自己的笔记仓库，这些仓库到时候会推送到GitHub上进行保存的。这样的好处在于，你不用担心自己换了台电脑之后就不能记录笔记了。当你更换电脑时，你可以重新回到你的GitHub账户下的仓库中，将仓库重新克隆到你的本地电脑中继续编辑你的笔记。每次编辑完成之后继续上传到GitHub的托管仓库中，这样可以保证你的笔记进行及时的备份。



### Step2：创建GitHub仓库

我们第二步需要到GitHub仓库中创建一个代码仓库来存放我们在本地创建好的笔记仓库，如图所示：



![image-20201231003700037](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010445.png)

![image-20201231004245585](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010451.png)

![image-20201231004525255](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010457.png)

点击上图中的复制按钮，复制上面的命令，然后在powershell中运行。

```bash
echo "# note-space" >> README.md
#表示创建一个readme.md文件并且写入# note-space这段文字

git init 
#表示初始化一个git仓库

git add README.md
#表示添加readme.md文件到本地git仓库中

git commit -m "first commit"
#备注这次提交的说明情况，这里是说明这是“第一次提交”

git branch -M main
#创建GitHub仓库中的main分支中

git remote add origin https://github.com/NothingLin/note-space.git
#和GitHub仓库创建连接关系，后面的地址表示GitHub的地址链接

git push -u origin main
#提交到GitHub仓库中去
```

在文件目录空白处，**Shift + 鼠标右键**，如下图所示：



![image-20201231005637977](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010507.png)

点击右键即可进行粘贴：



![image-20201231010228415](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010518.png)

上面报错只是说明你的GitHub账号还没有对本地电脑授权传输的权限，我们需要配置一下GitHub传输权限。



### Step3：设置GitHub账户的SSH Key

我们首先需要在本地生成一个SSH key：

```bash
$ ssh-keygen -t rsa -C “你的GitHub邮箱”
```

![image-20201231112224043](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115343.png)

输入上述命令的时候需要你输入三个回车键：

- 是否将SSH key 保存到这个目录？
- 是否需要免密码登录？（enter之后，每次上传都不需要再输入密码）
- 请再次输入回车键



之后在`C:\Users\Nothing（用户名）\.ssh`这个路径下生成三个文件，如图：

![image-20201231112749937](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115411.png)

我们使用记事本打开`id_rsa`这个文件：

![image-20201231113004990](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115424.png)

按`ctrl+A`全选全部的内容，`ctrl + c`复制全部内容：

![image-20201231113239250](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115438.png)



接下来我们需要返回GitHub账户的设置中去配置SSH keys，[点击直接跳转](https://github.com/settings/keys)：

![image-20201231113538824](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115458.png)

![image-20201231113904328](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115502.png)

![image-20201231113933570](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115507.png)

如果SSH-key的配置设置好了之后，那么就返回第二步：



### Step4：远程仓库push

![image-20201231004525255](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231010457.png)

```bash
echo "# note-space" >> README.md
#表示创建一个readme.md文件并且写入# note-space这段文字

git init 
#表示初始化一个git仓库

git add README.md
#表示添加readme.md文件到本地git仓库中

git commit -m "first commit"
#备注这次提交的说明情况，这里是说明这是“第一次提交”

git branch -M main
#创建GitHub仓库中的main分支中

git remote add origin https://github.com/NothingLin/note-space.git
#和GitHub仓库创建连接关系，后面的地址表示GitHub的地址链接

git push -u origin main
#提交到GitHub仓库中去
```

![image-20201231114341866](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115517.png)

完成上面的基本操作之后，基本上就已经完成了一个GitHub笔记仓库的创建了。



### Step5：管理笔记

一般来说，我的本地电脑和GitHub账号都有一个同步的笔记仓库。如果我需要编辑笔记的话，那么我直接在本地创建markdown文件形式的笔记，并且在本地电脑对笔记内容进行编辑。编辑完成之后，我们需要通过下面这些指令，将本地上的markdown笔记同步上传到GitHub仓库中做一个备份。

<br>



如果你在GitHub仓库中直接进行了一些修改，那么你在本地编辑文件时需要先同步GitHub上面的修改到本地仓库先，否则会造成本地push到GitHub仓库的过程中发生冲突，导致上传失败。

```bash
$ git pull --rebase origin main
```

提交到本地git仓库：

```bash
$ git add .
```

备注提交信息：

```bash
$ git commit -m "初步构建README文件"
```

提交到github远程仓库：

```bash
$ git push  origin main
```

通过这些指令就可以完成本地修改提交至GitHub账号备份的整个过程。

<br>



下图是我的常规编辑操作：

![image-20201231115625050](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115634.png)

![image-20201231115821309](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231115906.png)



<br>



[↪返回首页](https://nothing-lin.github.io/NothingLin-s-knowledge-space/)



<br><br>

![](https://NothingLin.coding.net/p/picture/d/picture/git/raw/master/2020/12/31/20201231121340.png)