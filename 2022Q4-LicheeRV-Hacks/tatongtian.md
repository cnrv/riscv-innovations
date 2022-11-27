# 【移植 static call 到 risc-v】

## 参与人

github: tatongtian

## 项目背景

发现 retpoline 方案对于性能影响较大，static call 可以提高性能，分支预测、乱序执行的产生漏洞可以通过此方案修复。

## 项目目标

输出文章：
1、《Meltdown 和 Spectre 漏洞分析》
2、《retpolines 功能及原理》
3、《Static Call 功能及原理》
输出成果：
1、确认 risc-v 架构下存在分支预测、乱序执行造成的内存数据被通过侧信道获取的漏洞。
2、使用 static call 解决漏洞。

## 预期成果

向内核提交 risc-v 架构的 static-call 补丁。

## 预期时间表

11月：
1、《Meltdown 和 Spectre 漏洞分析》
2、《retpolines 功能及原理》
12月：
1、《Static Call 功能及原理》
2、Static Call 功能移植
2023年1月：
1、Static Call 功能移植

## 成果展示


