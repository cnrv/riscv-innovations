# 将 Slackware 移植并运行于实体 riscv64 硬件上

适逢
此[开源项目](https://github.com/isrc-cas/tarsier-slkrv)
2022年11月20日的
新[提案](https://github.com/isrc-cas/tarsier-slkrv/blob/portal/reports/proposal-20221120.md)
正计划寻找赞助或申请硬件开发板。


## 参与人

* zxs-un
* hollalinux


## 项目背景

起初 Slackware 被用作构建目标以测试其它 Linux 发行版的交叉构建能力，
随着被测试发行版中发现的问题被逐个解决，Slackware 在 riscv64 上的构建愈发完善，
便成为了独立的发行版移植 riscv64 项目。

目前 slackware-riscv64 的进展快于立项时最初的预期，
已可启动并稳定运行于 qemu-system-riscv64 中，
发行版的工具链与软件集具备完整的自举能力，
并能启动 xfce4 和运行 Mozilla Firefox 等，
移植成功的软件数量仍在不断增长中。


## 项目目标

只能运行在模拟器中的操作系统终究是不完整的。
本提案最优先的目标即实现 slackware-riscv64 于实体硬件上的启动和运行。
以此活动计划提供的开发板为基础，适配 D1 系列开发板。


## 预期成果

1. 构建通用固件和启动引导以，撰写构建流程说明文档
2. 调整内核的构建配置以在实体硬件上可用
3. 打包发行可启动的硬盘镜像或文件系统，配套使用说明文档
4. 展示 slackware-riscv64 的 Firefox 在硬件上的运行效果
5. 构建并展示更多 slackbuilds-riscv64 桌面应用如 VLC、LibreOffice 等

## 预期时间表

- 2022年12月：在硬件上启动 slackware-riscv64 （最高优先级）
- 2022年12月：整理硬件启动所需的各类源码和方法并形成说明文档
- 2023年1月：展示更多直观的成果
- 2023年2月：发行一个 slackware-riscv64 的里程碑版本

【自己的最好的估计，但是请注意这不是承诺，并没有强制性，完不成就……放到明年的新年愿望里】

（最好是自己预测一两个月内能完成的工作，最好不要拖到明年。）


## 成果展示

【提交 proposal 的时候不要填写，留白。等以后做出来之后，将相关的链接PR到这里即可。】