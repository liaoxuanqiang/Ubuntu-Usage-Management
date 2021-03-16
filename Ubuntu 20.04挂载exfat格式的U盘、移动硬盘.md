## Ubuntu 20.04挂载exfat格式的U盘、移动硬盘

### 1)安装exfat的支持软件

```shell
sudo apt-get install exfat-fuse
```

### 2)重启系统

```shell
sudo shutdown -r now
```

### 3)插上U盘、移动硬盘

### 4)查看磁盘信息

```shell
sudo fdisk -l 
```

### 5)挂载U盘、移动硬盘

```shell
cd /mnt
sudo mkdir user_usb   #创建挂载目录
sudo mount /dev/sdb1 /mnt/user_usb  #执行挂载sdb1分区到user_usb目录
```

### 6)执行对挂载U盘移动硬盘的读写操作

### 7)卸载

```shell
sudo umount /mnt/user_usb  #完成操作后需要先执行卸载命令再将U盘、移动硬盘拔出
```
