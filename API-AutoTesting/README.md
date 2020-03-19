## 接口自动化测试

```
Date : 2020 - 03 - 19

Author : Soler HO
 
Description : 接口自动化测试
```
# 接口测试基础

## 接口测试的概述
应用程序编程接口（Application ProgrammingInterface，API）。

### 接口的定义？
两个`不同的系统`或者一个系统中`两个不同的功能`，它们之间相互连接的部分称为**接口** 。

常说的接口测试有两种：
- 图形用户接口（Graphical User Interface，GUI），是人与程序的接口；
- 应用程序编程接口（Application ProgrammaInterface，API）
	- API是一组定义、程序及协议的集合，API可实现计算机软件之间的相互通信。
	- 主要功能：提供通用功能集

### 接口的分类

根据遵循协议的不同，接口分为3类：
- **HTTP接口**，：基于超文本传输协议（HyperTextTransfer Protocol，HTTP）开发的接口，但并不能排除没有使用其他协议。
	- 基于浏览器/服务器模式（Brower/Server，B/S）的软件系统接口大多数为HTTP接口
- **Web Service接口**：系统对外的接口。
- **RESTful接口，简称为REST**：其描述了一个架构样式的网络系统，核心是面向资源。

## HTTP协议

## 接口测试的流程

#### 1.编写接口测试计划
接口测试计划包含`概述、测试资源、测试功能及重点、测试策略、测试风险、测试标准`。
#### 2.编写、评审接口测试用例
根据`需求文档、接口文档`等项目相关文档编写并`评审接口测试用例`。
#### 3.执行接口测试
依据编写的接口测试用例，借助`测试工具（如Postman、JMeter、SoapUI等）`执行接口测试，上报发现的问题。
#### 4.接口自动化测试持续集成要点
借助`工具Jenkins`进行持续集成。
- 接口自动化持续集成的主要内容：

	- 流程方面：在回归阶段加强接口异常场景的覆盖，并逐步向系统测试、冒烟测试阶段延伸，最终达到全流程自动化。
	- 结果展示：丰富的结果展示、趋势分析、质量统计和分析等。
	- 问题定位：报错信息、日志更精准，方便问题复现与定位。
	- 结果校验：加强自动化校验能力，如数据库信息校验。
	- 代码覆盖率：尝试由目前的黑盒向白盒下探，提高代码覆盖率。
	- 性能需求：完善性能测试体系，通过自动化的手段监控接口性能指标是否正常。

## 一个完整的API文档包含的主要部分
① 接口名称。

② 简要描述。

③ 请求的URL。

④ 请求方式（GET / POST等）。

⑤ 请求参数（参数名、是否必选、参数类型、说明）。

⑥ 返回示例。

⑦ 返回参数说明（参数名、类型、说明）。

⑧ 备注及责任人。

## postman概述

#### postman工作原理
![](https://github.com/SolerHo/Software-Testing/blob/master/API-AutoTesting/Images/postman%E5%B7%A5%E4%BD%9C%E5%8E%9F%E7%90%86.png)

①postman点击send发送请求给服务器

②服务器响应，对数据进行处理，然后返回给postman

③对返回内容进行加工处理，把格式化后的内容显示出来

#### postman的基础功能

![](https://github.com/SolerHo/Software-Testing/blob/master/API-AutoTesting/Images/postman%E7%9A%84%E5%9F%BA%E7%A1%80%E5%8A%9F%E8%83%BD.png)

## postman基本操作

## postman脚本问题
