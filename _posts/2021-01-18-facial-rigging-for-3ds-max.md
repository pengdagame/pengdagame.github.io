---
title: 在3ds Max中设计一套表情绑定系统
date: 2021-01-18
---
## 前言
大家好啊，最近在项目中完成了一套表情绑定工具，如下图所示。

![GITHUB](https://pengdagame.github.io/images/facialRigging.png "facialRigging")

该工具使用Maxscript编写，基于3ds Max的Helper Point和Expression Controller内置技术，以及参考Apple ARKit BlendShapes标准。

因此，这套表情系统不仅可以使用传统的K帧方式制作表情动画，也可以使用Apple设备（具备FaceID深度摄像头）捕捉的表情动画。