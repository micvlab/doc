python在linux下使用非常友好。如果要在windows下用python，最麻烦的是包管理。

首先是要安装anaconda，然后选择一个IDE，有以下几个选择，推荐2和3，其中pycharm实际使用中最稳定方便，Windows和Linux都支持，最推荐。

## 1. spyder或ipython notebook

安装anaconda 后，就自带 spyder 和 ipython notebook了。

spyder好用，但调试不太方便。ipython notebook 很多人推崇，可以试试。

## 2. pycharm

安装pycharm，打开，新建一个项目，选择你下载的代码的根目录，可能会提示是否用已有的源代码创建工程，选择是。

菜单file, settings, Project, project interpreter, 可以添加安装需要的库。

pycharm调试方便。

由于不同的python程序依赖的包不同，甚至python版本也不同，有的要python2, 有的要python3. 建议创建虚拟环境，即创建一套全新的python运行环境。

例如我们想在anaconda里创建一个名为caffe的虚拟环境，专供caffe程序使用，命令如下：

conda env list  查看当前的环境

conda create --name caffe --clone root  创建一个名为caffe的虚拟环境

source activate caffe  激活虚拟环境，windows 下调用activate.cmd，不需要加source

为保险起见，以上命令最好在conda.exe 和 activate.cmd 所在的目录下执行，特别是当你有多个版本的python并存时。当然，你也可以修改环境变量。

以上命令在pycharm里有对应的UI操作：菜单file, settings, Project, project interpreter, 齿轮图标，create conda env，输入虚拟环境名caffe即可。

但还是推荐在命令行下执行conda create --name caffe --clone root ， 因为图形界面操作很慢，而且没有进度条。

然后在project interpreter 的下拉列表里选择刚刚创建的虚拟环境，即可。

如果你不想再使用某个虚拟环境了，把它所在的目录删掉即可，默认是在Anaconda/envs/下。


## 3. 在viusal studio 里使用python 

下载地址 https://github.com/Microsoft/PTVS
网站上有以下几个东西
Python Tools for VS 2015

Python Tools for VS 2013

Sample Pack

Machine Learning Pack

下载Python Tools for VS 2013 和 Machine Learning Pack，分别双击安装，安装的时把vs关掉。

PTVS的好处有很多，调试方便，而且完全兼容了vs的使用习惯。


