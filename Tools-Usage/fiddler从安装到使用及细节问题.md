## fiddler在Ubuntu Linux上的安装

#### 安装mono
```
sudo apt-get install mono-complete
```

如果在安装过程中出现了如下的错误：
```
E: Could not get lock /var/lib/dpkg/lock-frontend - open (11: Resource temporarily unavailable)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), is another process using it?
```
截图如下：
![]()

解决方案：
```
sudo rm /var/lib/dpkg/lock-frontend       

sudo rm /var/lib/dpkg/lock

```

在fiddler的官网下载最新版本，下载地址：[](http://fiddler.wikidot.com/mono)

使用命令行解压文件，然后切换到fiddler.exe文件所在的目录，使用下面命令：
```
mono fiddler.exe
```

