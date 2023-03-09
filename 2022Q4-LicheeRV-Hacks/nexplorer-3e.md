# port https://github.com/ssvb/xf86-video-fbturbo/ , 嵌入式计算机图形试验场，以后大概也会搞搞 tf porting 。


## 参与人

【github: @nexplorer-3e】



## 项目背景

- 前阵子某 rv 交流群在聊图形性能相关的玩意，我对这方面比较薄弱想入一块同时学学计算机系统相关的东西
- 现有的除了 amdgpu 方案以外的图形方案都太弱了。 qemu 测试真的是满得吓人。

## 项目目标

- 没有问题的话，半个月到一个月编译出 board-specific package
- 有问题那确实得解决了， render 或者是 driver 之类的毛病
- 原仓库说是 any arch 所以也可以试试别的架构
- 会附上图形性能的，而且锅得比 llvmpipe 少（现有的模拟软解和 mttcg 配合是是有问题的）

## 预期成果

- 当然是 release
- 要是能作为 buildbox 为其他有开放 device tree 的板子提供那更好了
- 图形性能不能比 llvmpipe 差，起码得和 i915 virgil 打个平手


## 预期时间表

- 接下来是考试周。考试周以及别的一些收尾事情完了之后，就可以开始搞环境了。
- 一个月内 devlab 得搭好，这不难，毕竟比起手动评测各个发行版是要 easy 。
- 如上说，和一些小依赖搏斗。没有什么 board-specific issue 的话很快就能出来。
- 如果有的话就得了解一下 linux acceleration layer x11 wayland 都得有，不过先以 x11 实现一个 2d accelerator
- 闲置的时候可以跑跑评测，接个采集卡挂直播什么的都好。

<!--（最好是自己预测一两个月内能完成的工作，最好不要拖到明年。）-->

## 成果展示


