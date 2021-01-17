---
title: 在3ds Max中设计一套表情绑定系统
date: 2021-01-18
---
---
大家好啊，最近在项目中完成了一套表情绑定工具，如下图所示。

![GITHUB](https://pengdagame.github.io/images/facialRigging.png "facialRigging")

该工具使用Maxscript编写，基于3ds Max的Helper Point和Expression Controller内置技术，以及参考Apple ARKit BlendShapes标准。

因此，这套表情系统不仅可以使用传统的K帧方式制作表情动画，也可以使用Apple设备（具备FaceID深度摄像头）捕捉的表情动画。

---
### 工具作用
1. 一键生成表情绑定（定位骨骼，次级控制器，表情控制器）
2. 向左或者向右镜像定位骨骼
3. 修改表情驱动（表情控制器与次级控制器之间的链接关系）
4. 导入，移动，链接，烘培面部捕捉数据
5. 显示隐藏定位骨骼，次级控制器，表情面板
