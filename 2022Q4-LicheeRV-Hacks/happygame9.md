
# 【请一句话或一个短语描述你想做的事情】
基于全志D1-H 芯片与 Tina Linux 框架下的 LCD 屏幕适配


## 参与人
[github: happygame9]

## 项目背景
想要做一个嵌入式驱动的项目，学习嵌入式开发


## 项目目标
1.确保显示框架的内核配置有使能
2.前期准备以下资料和信息：
	屏手册。主要是描述屏基本信息和电气特性等，向屏厂索要。
	Driver IC 手册。主要是描述屏 IC 的详细信息。这里主要是对各个命令进行详解，对我们进行初始化定制有用，向屏厂索要。
	屏时序信息。请向屏厂索要。
	屏初始化代码，请向屏厂索要。一般情况下 DSI 和 I8080 屏等都需要初始化命令对屏进行初始化。
	万用表。调屏避免不了测量相关电压。
3.通过第2步屏厂提供的资料，定位该屏的类型，然后选择一个已有同样类型的屏驱动作为模板进行屏驱动添加或者直接在上面修改。
4.修改屏驱动目录
5.修改Makefile。
6.修改 board.dts 中的 lcd0 节点。
7.编译测试


## 预期成果
LCD屏幕能够正常点亮，能够显示正常的效果，可以切换屏幕显示


## 预期时间表
三周的时间阅读datasheet,了解完整的开发流程；
1个月左右编程，包括代码编写和debug，完成项目目标

## 成果展示
