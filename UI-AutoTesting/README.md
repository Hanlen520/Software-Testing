## UI自动化测试

```
Date : 2020 - 03 - 19

Author : Soler HO
 
Description : UI自动化测试
```
# UI自动化测试

## 自动化测试概述

#### 定义
把人为驱动的测试转化为机器执行的一种过程，重点在于持续集成这个概念；

**优势**：节约人力和时间成本。

## 测试金字塔

![](https://github.com/SolerHo/Software-Testing/blob/master/UI-AutoTesting/Images/%E6%B5%8B%E8%AF%95%E9%87%91%E5%AD%97%E5%A1%94.png)

由敏捷大师Mike Cohn提出该概念，然后由Martin Fowler大师在此基础上提出了测试分层概念，以区别于传统的自动化测试。

## Selenium概述
Selenium 是一个用于`Web 应用程序`的自动化测试工具。

Selenium 直接运行在浏览器中，它可以`模拟用户的行为操作`，操作界面友好。

Selenium 支持 `IE、GoogleChrome、Firefox、Opera` 等主流浏览器。

Selenium也支持主流开发语言，如Java、Python、C#等。

### Selenium 和 Webdriver 的安装问题

#### Selenium的安装
- 如果你使用的 `Python语言` 进行自动化测试，命令行输入：

```
pip3 install selenium
```
截图：

![](https://github.com/SolerHo/Software-Testing/blob/master/UI-AutoTesting/Images/selenium%E5%AE%89%E8%A3%85%E6%88%AA%E5%9B%BE.png)

#### Webdriver的安装

对于Python进行自动化时，要安装对应浏览器的 `Webdriver` 。查看浏览器的版本后下载对应的版本进行解压安装。

由于我使用的是Chrome浏览器，所以具体的下载地址：http://npm.taobao.org/mirrors/chromedriver/

Mac下的安装，Windows用户自行Google一下。

如果使用命令行对下载解压的文件移动到`usr/local/bin`，会出现没法移动文件.

所以可以使用 `command + shift + G` ，输入你要直接前往的`目录文件`。

![]()

将解压的Webdriver文件复制到文件目录下即可。

**验证是否安装成功**
```
# coding = utf-8
from selenium import webdriver

wd = webdriver.Chrome()
wd.get("http://www.baidu.com")
```

以下结果则安装成功

![](https://github.com/SolerHo/Software-Testing/blob/master/UI-AutoTesting/Images/webdriver%E5%AE%89%E8%A3%85%E6%88%90%E5%8A%9F.png)


### 使用浏览器插件Selenium IDE

Selenium IDE是一个带有执行界面的，用于 `录制或编写脚本` 的初级工具。

Chrome 浏览器 直接进入 `扩展程序应用商店` 搜索添加安装即可。

其他的浏览器不做一一介绍。

## Selenium元素定位问题


