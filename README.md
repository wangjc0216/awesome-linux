# AWESOME-Linux

关于Linux的相关内容


## 对于命令的理解

### whatis与whereis
使用`whatis docker`可以用来描述docker的命令：
```shell
➜  ~ whatis docker
docker (1)           - Docker image and container command line interface
```
使用`whereis docker`可以用来描述docker的位置：
```shell
➜  ~ whereis docker
docker: /usr/bin/docker /etc/docker /usr/share/man/man1/docker.1.gz
```

### man命令分类
```shell
(1)、用户可以操作的命令或者是可执行文件
(2)、系统核心可调用的函数与工具等
(3)、一些常用的函数与数据库
(4)、设备文件的说明
(5)、设置文件或者某些文件的格式
(6)、游戏
(7)、惯例与协议等。例如Linux标准文件系统、网络协议、ASCⅡ，码等说明内容
(8)、系统管理员可用的管理条令
(9)、与内核有关的文件
```
[man命令参考](https://man7.org/linux/man-pages/)

### 对于命令的理解
man命令中写的非常详细，可以通过man来阅读每个命令的含义，如 `man docker`。当我们想了解`docker ps`的意思的时候可以通过使用`man docker-ps`来进行
访问。也可以了解到`docker ps`命令的含义。


## 文件权限
Linux文件类型：
```shell
➜  net ls -alh
总用量 0
drwxr-xr-x.  2 root root      60 5月  20 13:53 .
drwxr-xr-x. 18 root root    2.7K 5月  20 13:53 ..
crw-rw-rw-.  1 root root 10, 200 5月  20 13:53 tun

linux中c表示字符设备文件，b表示块设备文件，l表示符号链接文件，r表示可读权限，w表示可写权限。
linux文件属性解读：
文件类型：
-：普通文件 (f)
d：目录文件
b：块设备文件 (block)
c：字符设备文件 (character)
l：符号链接文件(symbolic link file)
p：命令管道文件(pipe)
s：套接字文件(socket)
文件权限: 9位，每3位一组，每一组：rwx(读，写，执行)，当改组不具有某一权限用-代替。
第一组为: 文件拥有者的权限， 该文件的拥有者可以读写，但不可执行；
第二组为: 同群组的权限
```

