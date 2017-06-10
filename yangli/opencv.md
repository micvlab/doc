## Windows 下编译OpenCV

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

3. cmake编译

官网下载安装cmake，打开，


