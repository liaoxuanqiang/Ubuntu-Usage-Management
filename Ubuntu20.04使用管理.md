#####  一、修改系统软件源并更新软件

###### 1) 备份配置文件：

```
**sudo cp -a /etc/apt/sources.list /etc/apt/sources.list.bak**
```

###### 2) 修改sources.list文件

将http://archive.ubuntu.com 和 http://security.ubuntu.com 替换成 http://repo.huaweicloud.com，可以参考如下命令： 

```
sudo sed -i "s@http://.\*archive.ubuntu.com@http://repo.huaweicloud.com@g" /etc/apt/sources.list

sudo sed -i "s@http://.\*security.ubuntu.com@http://repo.huaweicloud.com@g" /etc/apt/sources.list
```

###### 3)    更新系统软件索引

```
sudo apt-get update
```

###### 4)    更新系统软件

```
sudo apt-get upgrade
```

