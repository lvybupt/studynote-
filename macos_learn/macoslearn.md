#Rmbp Add U2515 with Hidpi

[Close Rootless](https://www.zhihu.com/question/36108835) 
非开发者一般不推荐，或者建议执行后再次开启）, 重启，开机按住`Command + R`，以`Recovery分区启动`,在`Security Configuration中`关闭`Enforce System Integrity Protection`,命令行操作  
```
csrutil disable
```

[Make `Display PropertyList` File](https://comsysto.github.io/Display-Override-PropertyList-File-Parser-and-Generator-with-HiDPI-Support-For-Scaled-Resolutions/)

Download and compile [`RDM`](https://github.com/avibrazil/RDM)

```
make -f Makefile
```