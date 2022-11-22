# 为rt-thread smart添加riscv asid支持和licheeRV bsp

## 参与人

github: chenhy0106(1002138131@qq.com)

gitee：c__hy(1002138131@qq.com)

## 项目背景

近期在为rt-thread社区添加rt-smart操作系统的riscv asid支持，需要一个硬件的实验测试环境。

## 项目目标

1. 移植rt-thread smart到licheeRV上，必要的话需要制作一个licheeRV的bsp。
2. 添加rt-smart的riscv asid支持。

## 预期成果

1. 用于rt-smart的licheeRV板级支持包（bsp）
2. rt-smart的riscv asid单核支持。（全志D1似乎是riscv单核的，所以做多核支持也没法测试）代码提交到仓库https://gitee.com/rtthread/rt-thread/tree/rt-smart/

## 预期时间表

1. 12月前在rt-smart上添加单核asid支持。
2. 收到板子后到12月底，制作licheeRV的bsp
3. 剩下时间测试asid的功能正确性。

## 成果展示

【提交 proposal 的时候不要填写，留白。等以后做出来之后，将相关的链接PR到这里即可。】
