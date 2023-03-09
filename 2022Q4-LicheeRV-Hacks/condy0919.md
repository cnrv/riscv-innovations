# 开发

- linux perf 支持 riscv 上硬件事件计数器溢出

## 参与人

- condy0919

## 项目背景

在 `riscv` 平台上采样的时候发现 `perf list` 输出表明支持 `cpu-cycles` 与 `instructions` 这
两个硬件事件，但是 `perf record` 时无论怎样改变 freq 都没法采集到事件。后来更换为 `cpu-clock`
软件事件之后立即就观察到了。

`perf record` 采集数据需要硬件提醒，当一定数量的硬件事件发生且对应的 buffer 发生溢出，那么内核
就可以读取对应计数器以此来采集信息。所以一旦硬件事件不溢出，这种事件就无法被 `perf` 观察到。影响

- `perf record`
- `perf top`

`perf stat` 则不影响，因为它是主动去读的。

## 项目目标

使得 `perf record` 和 `perf top` 可以使用

## 预期成果

- 一个 kernel 的 patch

因为这是咱第一个 kernel 的 patch, 所以也会包含新人对 kernel 接受 patch 的流程做一个介绍。

## 预期时间表

2022-11-21 ~ 2023-02-01

预计需要花费 2 个月时间。以前主要作为 `perf` 的使用者，现在要对它作出一点贡献还需要积累一点 `perf`
的知识。

## 成果展示

【提交 proposal 的时候不要填写，留白。等以后做出来之后，将相关的链接PR到这里即可。】
