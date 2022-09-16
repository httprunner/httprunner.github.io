---
title: 录制生成 HAR 文件
weight: 1
description: 基于 HAR 生成测试用例
---

## 什么是 HAR 格式

> 以下内容来自维基百科关于 [HAR](https://zh.wikipedia.org/wiki/.har) 格式的介绍 

HTTP 存档格式（HTTP Archive format，简称 HAR）是一种 JSON 格式的存档文件格式，多用于记录网页浏览器与网站的交互过程。文件扩展名通常为 .har。

HAR 格式的规范定义了一个 HTTP 事务的存档格式，可用于网页浏览器导出加载网页时的详细性能数据。此格式的规范由万维网联盟（W3C）的 Web 性能工作组制作，截至2016年3月是一份规范草案。

## 录制 HAR 文件

采用 Charles 等抓包工具，以及 Chrome 等浏览器均可以导出 HAR 格式的文件，具体方式可以参考如下流程：

### Charles 录制 HAR 文件

Charles 录制 HAR 分为如下两步：
- 步骤一：在抓取到的会话（Session）上右击选择 `Export Session...`

![Charles 录制 HAR 文件步骤1](/image/charles-record-har-1.png)

- 步骤二：导出格式选择 `HTTP Archive (.har)` 来导出为 HAR 文件

![Charles 录制 HAR 文件步骤2](/image/charles-record-har-2.png)

### Chrome 录制 HAR 文件

Chrome 录制 HAR 文件可以通过如下两种方法：

- 方法一：点击按钮导出 HAR 文件
- 方法二：在请求列表空白处右击，选择`以 HAR 格式保存所有内容`

![Chrome 录制 HAR 文件](/image/chrome-record-har.png)
