
# windows下编译调试caffe

2017.5.28 更新
发现 caffe官方windows版本已经不提供vs工程文件了，要用cmake编译。重新记录过如下

开发环境：Windows 7/10，64位，Visual Studio 2013以上版本，推荐2015

1. 先装anaconda

2. 下载caffe windows版本源码，生成vs工程

项目地址： https://github.com/BVLC/caffe

最好用git clone下载源码，branch 选择windows，

用cmake 配置根目录下的cmakelists.txt，即where is the source code填入cmakelists.txt所在目录，where to build the binaries填入根目录下的一个新建目录。

然后configure, 提示要下载libraries_v140_x64_py27_1.1.0.tar.bz2，根据vs版本不同，文件名可能不同。下载通常很慢，建议用下载工具直接下载。

在caffe根目录下用notepad搜索 下载的提示，找到下载地址，https://github.com/willyd/caffe-builder/releases/download/v1.1.0/libraries_v120_x64_py27_1.1.0.tar.bz2

下载后复制到它提示的目录下，通常是类似这样的目录 C:\Users\yourname\ .caffe\dependencies\download 。再configure。

如果提示atlas错误，把BLAS 选项改为Open，意思是用OpenBlas

第一次使用，建议勾选cpu_only。如果有GPU并安装cuda，则可以不勾选。

然后generate ，成功。

3. 打开生成的sln文件，编译，大功告成。

验证：在tools目录下的某个工程（例如caffe.bin，extract_features等）上右键，设置为启动项目，然后ctrl+f5运行，如果可以运行，则说明已经编译好了。



# windows下编译调试caffe

杨力 2017.2.22 

## 1. 下载源码
https://github.com/BVLC/caffe
branch选择windows， 下载源码

## 2. 打开工程
CommonSettings.props.example 复制一份，命名为CommonSettings.props，用文本编辑器打开（如notepad++），修改其中选项。

打开windows目录，用vs2013打开sln解决方案文件。


## 3. 编译运行
直接build即可。

此解决方案中自带的多个可执行工程，可直接运行，例如compute_image_mean，extract_features等。
