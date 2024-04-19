## 一、查看基础环境

检查红框内的BIOS跟安全启动状态是否一致

![1](https://s2.loli.net/2024/03/10/19jSnRu7N5ZJx8C.png)

## 二、准备安装文件

#### 1.下载Ubuntu 22.04.01 LTS镜像ISO文件

这是官网下载：

https://ubuntu.com/download/desktop

如果速度较慢，可以选择清华镜像，清华镜像网址：

https://mirrors.tuna.tsinghua.edu.cn/ubuntu-releases/22.04.1/

#### 2.下载官方推荐的U盘启动制作工具

U盘启动制作工具选择RUFUS：

https://rufus.ie/zh/

#### 3.制作启动U盘

因为该过程会对U盘格式化，擦除u盘上所有数据，建议备份好所有U盘上文件；

（1）打开Rufus 3.20软件，导入镜像文件；分区类型选择GPT，目标分区类型选UEFI（非CSM）；文件系统选择NTFS，簇大小选默认：4096字节（默认），设置完成后点击开始。接下来提示选择写入模式，选择第一个：以ISO镜像模式写入（推荐），点击OK。

![2](https://s2.loli.net/2024/03/10/ztM79wBEGclrQZm.png)



（2）文件开始擦除数据并写入文件，等待几分钟，我的用10分钟，“准备就绪”，点关闭。

![3](https://s2.loli.net/2024/03/10/riJGXa64dzsm7eK.png)

#### 4.新建硬盘分区用来安装Ubuntu系统

设置里面搜磁盘管理->选择一个磁盘->右键->压缩卷。我分了100G：

![4](https://s2.loli.net/2024/03/10/sFyf9H4BTwA5lxS.png)

![5](https://s2.loli.net/2024/03/10/7ZDAxlug5wSrt2J.png)

5.BIOS设置 

在设置找到高级启动，并且点击立即启动，然后在BIOS设置下将自己的U盘设置为启动优先项。

## 三、安装Ubuntu 

#### 1.准备安装

插入U盘，开机，按Delete进入启动项设置，选择第一个“Ubuntu （safe graphics）”，回车，开始进入装机界面。选择语言“中文（简体）”，点击“安装Ubuntu”

![6](https://s2.loli.net/2024/03/10/JShfd4vBGMgEuXa.png)

2.接下来按照Ubuntu系统的提示选择，可一路默认安装。

键盘布局（默认：Chinese）

无线（默认：I donot want to connect to a WI-Fi network right now）

更新和其他软件（默认：正常安装）

安装类型（默认：安装Ubuntu，与Windows Boot Manager 共存，出现“将改动写入磁盘吗？”对话框，点击“继续”）

您在什么地方？（时区选择，省事些建议选择“London”；如果非要选择“Shanghai”，后面会涉及双系统时间不一致问题，需要调整，见第五部分）

您是谁？（输入用户名和密码，点“继续”）

开始安装，等待一会儿，安装完成，提示重启，拔掉U盘，点击“现在重启”，选择第一个Ubuntu系统。至此安装完成。


四、安装成功
