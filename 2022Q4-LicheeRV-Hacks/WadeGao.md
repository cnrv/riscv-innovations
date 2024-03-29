# 【[实现功能完整的RISC-V体系结构模拟器](https://github.com/WadeGao/rv64_emulator)】

## 参与人

【github: WadeGao】

## 项目背景

对体系结构相关知识比较感兴趣，工作中多多少少有过涉猎，想实现一个完整的RISC-V体系结构模拟器，以便更好的理解体系结构相关知识。

## 项目目标

- 用C++完整模拟一个RISC-V处理器，并成功运行Linux内核


## 预期成果

* ✅ 实现RV64IMA指令集，并通过[官方用例](github.com:riscv-software-src/riscv-tests)
* ✅ 特权架构
* ✅ 异常
* ✅ PLIC与CLINT
* ✅ UART
* ✅ 中断
* ~~Virtio~~
* ✅ 虚拟内存
* ✅ ...
* ✅ Linux内核！


## 预期时间表
* ✅ 特权架构：2022.11.30
* ✅ 异常：2022.12.15
* ✅ PLIC与CLINT：2022.12.30
* ✅ UART：2023.1.15
* ✅ 剩下的明年再规划吧~打工狗时间有限

## 成果展示

* 本模拟器成功运行了主线的Linux内核，详情请见[项目主页](https://github.com/WadeGao/rv64_emulator)

[![run-kernel.png](https://i.postimg.cc/xjtcDGPG/run-kernel.png)](https://postimg.cc/RqJMwHyq)