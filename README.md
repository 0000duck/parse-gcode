
针对萌新C ++练手项目简介
==================
* github下载速度太慢，本项目最新进度移至码云上进行更新项目地址（https://gitee.com/liuwentao1234/robot-simulation-software)
*本仓库只更新readme

![外观](https://images.gitee.com/uploads/images/2021/0221/100430_0b1c4914_6574042.png "屏幕截图.png")

项目介绍
========
* 基于Qt框架,Qt本身可以被称作是一种C++的延伸,Qt本身已经继承了C++的快速、简易、面向对象等许多的优点.
* 本项目模块可分为三大块:
    * 解析G代码
    * 轨迹数据可视化
    * 机器人三维仿真
* 项目技术栈: 基本涵盖了所有C++基础,例如数据结构与算法,设计模式,STL库等
* 面向对象编程: <Effective C++> <More Effective C++>
* 大部分代码都配有注释降低上手难度
* 项目代码行1W+

模块介绍
========
### 解析G代码
![输入图片说明](https://images.gitee.com/uploads/images/2021/0221/103251_fe506ccb_6574042.png "屏幕截图.png")
* 本功能是通过解析数控程序G/M代码指令,获取二维的轨迹数据进行绘制
* 增加了刀补算法: 可根据刀具宽度和计算轨迹调整实际切割轨迹
* 增加了手势操作: 鼠标滚轮放大以及拖拽
![输入图片说明](https://images.gitee.com/uploads/images/2021/0221/103325_a584c0dc_6574042.png "屏幕截图.png")

### 轨迹数据可视化
![界面](https://images.gitee.com/uploads/images/2021/0221/101430_983d6d80_6574042.png "屏幕截图.png")
* 可以将TXT文件的轨迹数据导入,实现轨迹数据的显示
* 除此以外还提供了求交面设置,可以捕捉到轨迹和任意平面的相交的点坐标
![求交面设置](https://images.gitee.com/uploads/images/2021/0221/101721_837020fe_6574042.png "屏幕截图.png")

### 机器人三维仿真
![仿真界面](https://images.gitee.com/uploads/images/2021/0221/101805_88b9ac8d_6574042.png "屏幕截图.png")
* 本功能可以实现三维机器人stl文件的导入, 通过载入关节来装配机器人
* 设置机器人的关键参数: DH参数, 运动范围, 起始角度
* 增加了加载工件功能: 工件提供坐标轴和环, 可以与鼠标交互实现移动和旋转
* 增加机器人示教功能: 通过示教功能实现机器人的运动
* 增加了轨迹运动起始姿态幻影: 每次开始运动时记录原始姿态
![参数设置](https://images.gitee.com/uploads/images/2021/0221/102703_658bce70_6574042.png "屏幕截图.png")
![工件](https://images.gitee.com/uploads/images/2021/0221/102612_18ea056b_6574042.png "屏幕截图.png")
![幻影](https://images.gitee.com/uploads/images/2021/0221/102632_4cd1776f_6574042.png "屏幕截图.png")

### 三维场景节点组织图
* 渲染引擎使用OSG, OSG使用的是树数据结构来管理场景内部的各个节点, 大致组织结构如下
![ss](image/场景节点组织图.jpg)
