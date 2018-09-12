# USB-Linux-Partition 在你的数据U盘里隐藏一个Linux

1.简述

> Windows对于U盘——不同于移动硬盘——只识别第一个分区, 所以,
> 如果我给U盘分2个区, 把引导启动到第二个分区, 可以实现隐藏一个Linux启动盘。

2.分区(使用DiskGenius)
```
选择U盘 + 快速分区
  自定: 2个分区
  右侧 高级设置
    第二个分区勾选为主分区
    填写第二个分区的大小
  确定

选择U盘第一个分区 + 删除分区
  是

保存更改
  是

选择U盘第二个分区 + 指派新的驱动器号(盘符)
  指派U:
  确定

关闭软件, 安全删除U盘
  此时我的电脑U盘容量显示是错误的
  
重新插入U盘
  我的电脑正确显示U盘容量
```

3.安装Linux(使用Universal USB Installer)
```
选择Ubuntu
选择ISO
  ubuntu-14.04.5-desktop-amd64
选择 U:\
  勾选 Format
Create
  是
```

5.恢复分区(使用DiskGenius)
```
选择U盘 + 选择空闲 + 新建分区
  主分区
  NTFS
  确定

保存更改
  是

关闭软件, 安全删除U盘
```
