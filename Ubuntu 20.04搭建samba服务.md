## Ubuntu 20.04搭建samba服务

### 1)安装软件

```shell
sudo apt update
sudo apt install samba
```

### 2)配置

```shell
vim /etc/samba/smb.conf #修改配置文件
```

文件底部添加配置

```shell
[share]
    path = /home/username/share
    read only = no
    browsable = yes

```

### 3)配置权限

```shell
chmod 777 /home/username/share
sudo smbpasswd -a username #添加用户
```

*username是要添加的用户名，提示输入密码即可

### 4)运行

```shell
sudo service smbd restart
```

