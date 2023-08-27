# 一、Anaconda安装

下载地址：https://www.anaconda.com/download/
百度网盘链接：https://pan.baidu.com/s/1ccqr833QKsxI5qkW97LCJg

提取码：o09u



选All Users 点Next

![](anaconda的安装及使用.assets/image-20230628125204042.png)

接下来选择安装路径，这里不建议装在C盘，安装完大概3个G左右，现在都是固态硬盘了，安装到固态硬盘就好，路径要知道自己安到了哪里（后续使用不同环境的时候会用到这个安装路径）。选择好了之后点击Next

安装好后修改下载源路径

![image-20230628130715862](anaconda的安装及使用.assets/image-20230628130715862.png)

## 1.修改为清华源

打开anaconda prompt输入

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud//pytorch/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --set show_channel_urls yes  //从channel中安装包时显示channel的url
```

移除下载源的操作

```
config --remove channels XX
```

这个命令是为了移除之前`conda config --show channels`显示的清华源。

## 2.配置环境变量

1.可以直接按win键，搜索“环境变量”

![img](anaconda的安装及使用.assets/95cbb4395f404c96b8cb3f8b491a8ea6-1693127141144.png)

 ![img](anaconda的安装及使用.assets/e7e2af85be584d409b08340ff3a762a2-1693127145687.png)

2. 双击Path,点击新建

![img](anaconda的安装及使用.assets/ac003905f2094b06b70a7f16ce8bdd68-1693127147957.png)



！！！把这几条复制到里面（注意我装的是E:\Anaconda这个目录，你要根据自己实际安装目录进行改动，比如装在C盘根目录，就把所有E改成C就行，）：

```
E:\Anaconda 
E:\Anaconda\Scripts 
E:\Anaconda\Library\mingw-w64\bin
E:\Anaconda\Library\usr\bin 
E:\Anaconda\Library\bin
```



# 二、创建虚拟环境

## 1.首选pycharm创建

![image-20230628171332416](anaconda的安装及使用.assets/image-20230628171332416.png)

要是失败可能是anaconda文件夹的访问权限不够，需要改为完全控制

## 2.手动创建特别麻烦

出现某个目录拒绝访问时，考虑文件权限的问题。

anaconda prompt输入：`pip install virtualenv`

![屏幕截图 2023-06-28 164026](anaconda的安装及使用.assets/屏幕截图 2023-06-28 164026.png)

出现安到其他地方了，就按照提示将那个位置路径添加到环境变量中。出现没有哪个包就装哪个包，也别乱改位置了，太麻烦了。

`virtualenv  XX` 创建环境

![image-20230628165104888](anaconda的安装及使用.assets/image-20230628165104888.png)

# 三、根据requirement.txt安装扩展库

激活环境：`activate XX`,	`anaconda3\envs`下的虚拟环境

切换到需求文件所在位置，`pip install -r "文件名"`

![image-20230606160642714](anaconda的安装及使用.assets/image-20230606160642714.png)









