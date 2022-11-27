# 移植徐霞客到LicheeRV

* （说明：请不要将个人的电话、地址等信息发送在PR上。审核通过后，个人信息都是通过邮件或微信发送的。）
* （文件名请使用自己的GitHubID命名，不要直接修改模版文件）

## 参与人

【github: bjzhang】

(我们后续有可能跟踪 GitHub 上的进展进行一些交流或推荐。可以写多个人。也可以不写。)

## 项目背景

为了自己学习和支持大家的学习，希望有一个简单且合理的测试RISC-V和LicheeRV的小系统。

## 项目目标

徐霞客取自徐霞客浏览中华大地并撰写徐霞客游记的故事。目前对aarch64已经支持了异常处理和内存映射。对RISC-V仅仅支持异常处理。还没有支持一个完整的板子。
现有项目代码：https://github.com/bjzhang/xuxiake/tree/dev-aarch64

## 预期成果

- 通过openSBI启动徐霞客
- 支持启动到RISC-V的usermode，并打开MMU
- 控制LicheeRV的GPIO跑马灯
- 可以返回网络arping包。

## 预期时间表

- 熟悉环境，自己编译openSBI，Linux内核和文件系统 3天
- 适配licheeRV板子，通过openSBI启动徐霞客 2天
- 支持启动到RISC-V的usermode，并打开MMU 3天
- 控制LicheeRV的GPIO跑马灯 2天
- 可以正确回复arping包。2周

## 成果展示

【提交 proposal 的时候不要填写，留白。等以后做出来之后，将相关的链接PR到这里即可。】
