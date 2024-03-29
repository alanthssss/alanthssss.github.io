# 环境搭建（编程前的准备）

说明：

- mac自带Python2，可以无差别实现下一章的三个demo（自行安装pip或用其他方法安装flask模块即可），配置Python3开发环境、使用Python都很简单，下面给出安装包链接，在此不做详细介绍。
- 在windows配置Python开发环境有两种方法比下文介绍的朴素方法快的多：Subsystem、Docker。此处只提出方法名，没有使用经验的话就按照朴素方法开始吧。
- 最朴素的安装方法最适合初学者，教程也最乱，这里给出精准的详细步骤，咱们不走弯路。

## 安装包下载

Python安装包(根据系统选择链接下载当前最新Python3安装包)

![Package](assets/19.png)

- [windows x64](https://www.python.org/ftp/python/3.7.3/python-3.7.3-amd64.exe)
- [mac x64](https://www.python.org/ftp/python/3.7.3/python-3.7.3-macosx10.9.pkg)

关于Python版本选择注意：简单学习可先忽略版本，确保使用Python3.x即可，Python核心团队计划2020年停止支持Python2。

## windows安装Python3

此处会安装好Python3以及包管理工具pip

1.选择windows需要的安装包点击开始安装
![Click Installation](assets/000.png)
2.  自动配置环境变量，以及选择自己配置安装（主要为了能让本机所有用户使用此次安装的Python）
![PATH of Python](assets/001.png)
3. 进入下一步，再点击Next（pip为Python的模块管理工具）
![Next](assets/002.png)

1. 勾选为所有用户安装，安装位置发生改变，初步配置完成，点击Install

- 勾选前

![Before Select](assets/003.png)

- 勾选后

![After Select](assets/004.png)

- 安装中

![Installing](assets/005.png)

- 安装完成

![Installed](assets/006.png)
5. 验证安装

- `win+r`打开`运行`，输入`cmd`，按`enter（回车）`打开`命令行窗口（下文简称命令行）`
![CMD in Control](assets/007.png)

- 输入`python -V`、`pip -V`（注意大写V）得到python版本、pip版本，安装完成

![Check Python and Pip Version](assets/008.png)
