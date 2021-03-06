---
layout:     post
title:      "基于Swift的Web框架Vapor2.0文档（翻译）Core-Package"
subtitle:   ""
date: 2017-08-24 08:00:00.000000000 +08:00
author:     "范东"
header-img: "img/post-bg-ios9-web.jpg"
catalog:    true
tags:
    - iOS
    - Swift
    - Web
    - Vapor
---
## 前言
之前一直有做Java后台开发的兴趣，可是想到要看好多的Java教程，作为一个iOS开发者，我放弃了，
后来从朋友[韩云智VL](http://www.jianshu.com/u/92f7630a351b)那里知道了这个框架，竟是用Swift写的，不得不说，它燃起了我的兴趣。
[Vapor](http://vapor.codes)是一个基于Swift开发的服务端框架，可以工作于iOS，Mac OS，Ubuntu。
为了配合Swift部署到服务器,我把ECS的服务器系统改为Ubuntu16.04。
> [Vapor 2.0 - 文档目录](https://github.com/fandongtongxue/VaporDoc/blob/master/README.md)
> 以下文字翻译自[Vapor Docs/Core/Package](https://docs.vapor.codes/2.0/core/package/)

## 使用Core(核心)
### 通过Vapor
默认情况下,这个依赖包就包含在Vapor当中,只需要添加

```
import Core
```
### 没有Vapor
Core(核心)为任何服务器端的Swift项目提供了大量的便利,要将其包含在您的包中,请将以下内容添加到您的`Package.swift`文件中.

```
import PackageDescription

let package = Package(
    name: "Project",
    dependencies: [
        ...
        .Package(url: "https://github.com/vapor/core.git", majorVersion: 2)
    ],
    exclude: [ ... ]
)
```
使用`import Core`方位Core(核心)的API.