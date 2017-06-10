## Windows 下编译OpenCV

环境：Windows 7/10，64位，Visual Studio 2013以上版本，推荐vs2015。

1. 下载opencv最新版

官网 http://opencv.org 有提供不同平台的专用版本，windows 下有个 win pack。

下载后双击，它会解压到当前目录。

顺便说一个老生常谈的问题：凡是编程相关的目录、文件名，不要用中文。

2. 下载opencv_contrib

这一步可选。地址： https://github.com/opencv/opencv_contrib

opencv_contrib 是opencv还在开发中的新功能集合，可能还不稳定。

可以download zip，或者用git客户端 tortoisegit 下载。

最好把它放在和上一步opencv解压目录相邻的地方。

git客户端不会用？ 参考 https://github.com/micvlab/doc/blob/master/github%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.txt

3. cmake生成解决方案

官网cmake.org下载安装cmake，打开，

where is the source code填入opencv根目录下的cmakelists.txt所在目录，where to build the binaries填入根目录下的一个新建目录。

然后configure, 

注意勾选build_examples，opencv_extra_modules_path设置为opencv_contrib所在目录。其他选项自行搭配。

configure没有错误，则点击generate，生成sln解决方案文件。

4. 编译

打开sln文件，在vs里生成，即可。

在解决方案资源管理器中samples目录下的任意一个工程上右键，设为启动项目，生成，然后ctrl+f5运行，如果能运行，说明编译成功。






