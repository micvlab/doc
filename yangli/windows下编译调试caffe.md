
# windows下编译调试caffe

2017.5.28 更新
发现 caffe官方windows版本已经不提供vs工程文件了，要用cmake编译。重新记录过如下

1. 先装anaconda

2. 用cmake 直接配置根目录下的cmakelists.txt

提示要下载libraries_v120_x64_py27_1.1.0.tar.bz2，根据vs版本不同，文件名可能不同。如果下载很慢，建议用下载工具直接下载。

在caffe根目录下用notepad搜索 下载的提示，找到下载地址，https://github.com/willyd/caffe-builder/releases/download/v1.1.0/libraries_v120_x64_py27_1.1.0.tar.bz2

复制到它提示的目录下。再configure

如果提示atlas错误，则改为openblas

如果没有gpu，记得勾选cpu_only

然后generate ，成功。

3. 打开生成的sln文件，编译，大功告成。



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
