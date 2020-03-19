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
以百度搜索为例

在Selenium自动化测试中，提供了单个元素定位方式和多个元素定位方式。

两种方式都是根据`元素属性 ID、NAME、CLASS_NAME、TAG_NAME、CSS_SELECTOR、XPATH、LINK_TEXT、PARTIAL_LINK_TEXT` 来进行定位。

### Webdriver采用的基本元素定位方式
![](https://github.com/SolerHo/Software-Testing/blob/master/UI-AutoTesting/Images/%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png)

#### 1.ID属性

可以看到，输入框的id为：kw，使用方法：` find_element_by_id` ，代码如下：
```
"""
Date: 2020 - 03 - 19
Author: Soler HO
Description: ID属性定位
"""

# coding = utf-8
import time
from selenium import webdriver

wb = webdriver.Chrome()
wb.get("http://www.baidu.com") // 获取url
wb.implicitly_wait(5) 
wb.find_element_by_id('kw').send_keys('python')
wb.quit()
```

#### 2.name属性
name属性为：wd ,使用的方法：`find_element_by_name`。代码如下：
```
"""
Date: 2020 - 03 - 19
Author: Soler HO
Description: name属性定位
"""

# coding = utf-8
import time
from selenium import webdriver

wb = webdriver.Chrome()
wb.get("http://www.baidu.com")
wb.implicitly_wait(5)
wb.find_element_by_name('wd').send_keys('python')
```
#### 3.class_name属性
class_name 属性为：s_ipt，使用的方法：`find_element_by_class_name`。代码如下：
```
"""
Date: 2020 - 03 - 19
Author: Soler HO
Description: calss_name属性定位
"""

# coding = utf-8
import time
from selenium import webdriver

wb = webdriver.Chrome()
wb.get("http://www.baidu.com")
wb.implicitly_wait(5)
wb.find_element_by_class_name('s_ipt').send_keys('python')
wb.quit()
```

#### 4.使用Xpath定位
使用的方法是：`find_element_by_xpath`。

具体的xpath获取方式：

定位到某个属性，然后右键 `copy ---> copy xpath`即可。

![](https://github.com/SolerHo/Software-Testing/blob/master/UI-AutoTesting/Images/Xpath%E5%AE%9A%E4%BD%8D.png)

代码如下：
```
"""
Date: 2020 - 03 - 19
Author: Soler HO
Description: xpath进行定位
"""

# coding = utf-8
import time
from selenium import webdriver

wb = webdriver.Chrome()
wb.get("http://www.baidu.com")
wb.implicitly_wait(5)
wb.find_element_by_xpath('//*[@id="kw"]').send_keys('python')
wb.quit()

```

