```
Date : 2020 - 03 - 17

Author : Soler HO
 
Description : fiddler从安装到使用及细节问题
```
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
![](https://github.com/SolerHo/Auto-Testing/blob/master/Tools-Usage/Images/ubuntu%E9%94%99%E8%AF%AF%E6%8F%90%E7%A4%BA.png)

解决方案：
```
sudo rm /var/lib/dpkg/lock-frontend       

sudo rm /var/lib/dpkg/lock

```

在fiddler的官网下载最新版本，下载地址：http://fiddler.wikidot.com/mono

使用命令行解压文件，然后切换到fiddler.exe文件所在的目录，使用下面命令：
```
mono fiddler.exe
```

