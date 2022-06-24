# ffplay编译调试项目

macOS Mojave系统编译的FFmpeg-n4.4.1

移植ffplay以及依赖库为cmake项目，方便编译以及代码调试

可以直接导入为CLion工程，并编译。Window系统可以本地编译FFmpeg-n4.4.1项目后，将生成的动态链接文件copy到third/lib路径下

## 简单编译

```shell
mkdir build
cd build
cmake ..
make -j16
```

最后生成的可执行文件 edu-ffplay

用于ffplay源码研究，以及后续自定义修改