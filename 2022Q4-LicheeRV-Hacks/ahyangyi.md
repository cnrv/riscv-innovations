# Gentoo RISCV 试玩和移植

## 参与人

【github: ahyangyi】

(我们后续有可能跟踪 GitHub 上的进展进行一些交流或推荐。可以写多个人。也可以不写。)

## 项目背景

我是一个长期的 Gentoo 用户，一直维护着个人的 Gentoo Overlay。看到这个项目，希望可以申请一块开发板，可以移植更多包到 RISCV 平台上。

## 项目目标

目标有以下三点：

* 在开发板上跑起来一个可用的 Gentoo Linux；
* 在个人的 Overlay 上添加若干包的 RISC-V 支持；
* 把部分结果以 portage tree PR 的形式提交给 Gentoo 官方。

## 预期成果

预期成果就是前述目标的后两点，即 Overlay 里添加 ebuild 和 portage tree 上的 pull request。

## 预期时间表

一定程度上取决于什么时候收到开发板吧。大体上是以下节奏：

* 元旦节前把开发环境配置好；我猜测直接在开发板上跑 Gentoo Linux 会有速度和存储容量的问题，要么需要搞交叉编译，要么需要以某种方式给开发板添加存储（至少也是挂载 NFS）。因此万事开头难。
* 过年前逐步添加 ebuild。

## 成果展示
