# 【让 IPFS 的 GO 或 JS 语言实现的命令行服务能跑起来】

## 参与人

github: flyskywhy

## 项目背景

我在 ARM 板子上编译运行过 IPFS 的 GO 实现，我也精通 JS react-native 编程。

## 项目目标

让自己获知一下当前 riscv 是否已能支持复杂的 GO 语言项目，就以 IPFS 为例吧。同时也想获知 riscv 对 JS 的支持程度，毕竟“能用 JS 实现的最终都会用 JS 实现”而且我更喜欢 JS 语言。

## 预期成果

* 在我维护的 IoT 项目 https://github.com/flyskywhy/textiot （内含 IPFS 代码）中的 go 语言实现部分增加 riscv 的编译选项
* 在 https://github.com/flyskywhy/ 中新建 JS 在 riscv 运行的示例代码
* 在我的博客 https://github.com/flyskywhy/g 中记录本项目的实践过程、成果。

## 预期时间表

一个月内完成我的 GO 项目的编译、运行尝试，另一个月内试验 JS 的各种可能性。

## 成果展示

* [go-textile: support risc-v](https://github.com/flyskywhy/textiot/commit/046914e)
* [Lichee RV 使用详解](https://github.com/flyskywhy/g/blob/master/i%E4%B8%BB%E8%A7%82%E7%9A%84%E4%BD%93%E9%AA%8C%E6%96%B9%E5%BC%8F/t%E5%BF%AB%E4%B9%90%E7%9A%84%E4%BD%93%E9%AA%8C/%E7%94%B5%E4%BF%A1/Cpu/Riscv/LicheeRV%E4%BD%BF%E7%94%A8%E8%AF%A6%E8%A7%A3.md)
* 上面“Lichee RV 使用详解”一文中描述了安装 nodejs 然后顺利运行 js 程序的过程
