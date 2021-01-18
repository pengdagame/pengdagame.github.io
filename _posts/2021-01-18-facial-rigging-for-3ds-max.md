---
title: 在3ds Max中设计一套表情绑定系统
date: 2021-01-18
---
---
### 前言
大家好。最近，我编写了一个表情绑定工具，如下图所示。

<div align=center><img src="https://pengdagame.github.io/images/facialRigging.png"/></div>

该工具使用Maxscript编写，基于3ds Max的Helper Point和Expression Controller内置技术，以及参考Apple ARKit BlendShapes标准。

因此，这套表情系统不仅可以使用传统的K帧方式制作表情动画，也可以使用Apple设备（具备FaceID深度摄像头）捕捉的表情动画。

---
### 主要功能
1. 一键生成表情绑定（定位骨骼，次级控制器，表情控制器）
2. 向左或者向右镜像定位骨骼
3. 修改表情驱动（表情控制器与次级控制器之间的链接关系）
4. 导入，移动，链接，烘培面部捕捉数据
5. 显示隐藏定位骨骼，次级控制器，表情面板

### 计划功能
1. 增加口型控制器，综合表情控制器（喜怒哀乐等）
2. 定位骨骼信息可以导入和导出
3. 表情驱动信息可以导入和导出，以及左右镜像

---
### 使用方法
+ 在工具加载后，先导入头骨骼信息，在依次选点创建五官各个部位。需要特别注意的事项，眼球和下巴的定位骨骼需要放在该部位的旋转中心点。
<div align=center><img src="https://pengdagame.github.io/images/locatorBone.gif"/></div>

+ 待所有定位骨骼创建完成后，需要把它们加入头部模型的蒙皮列表里。并给每个定位骨骼绘制权重。
<div align=center><img src="https://pengdagame.github.io/images/locatorSkin.gif"/></div>

+ 在所有定位骨骼生成后，点击次级控制器按钮生成即可。
<div align=center><img src="https://pengdagame.github.io/images/secondController.gif"/></div>

+ 在所有次级控制器生成后，点击表情控制器按钮生成即可。
<div align=center><img src="https://pengdagame.github.io/images/facialController.gif"/></div>

+ 在表情控制器生成后，表情控制器沿着单轴向（上下方向，左右方向）移动到最大值。移动次级控制器后，点击驱动修改器按钮修改完成。
<div align=center><img src="https://pengdagame.github.io/images/modifyDrive.gif"/></div>

+ 在表情控制器生成后，点击导入表情捕捉文件按钮，把表情捕捉文件全部导入场景中。
<div align=center><img src="https://pengdagame.github.io/images/importMocapData.gif"/></div>

+ 在表情捕捉文件导入场景后，点击移动面捕模型按钮，可以把捕捉模型移动到表情控制器旁边，方便观察动捕效果。
<div align=center><img src="https://pengdagame.github.io/images/moveMocapData.gif"/></div>

+ 在表情捕捉文件导入场景后，点击链接面捕数据按钮，可以把捕捉模型上的Morpher信息链接到表情控制器上。
<div align=center><img src="https://pengdagame.github.io/images/linkMocapData.gif"/></div>

+ 在表情捕捉模型链接表情控制器后，点击烘培面捕数据按钮，可以把链接控制烘培表情控制器上。
<div align=center><img src="https://pengdagame.github.io/images/bakeMocapData.gif"/></div>