# 【请一句话或一个短语描述你想做的事情】

在 RISC-V 平台上对低位宽网络 (low-bitwidth networks) 进行编译优化，实现端到端的推理部署

## 参与人

【github: chhzh123】

(我们后续有可能跟踪 GitHub 上的进展进行一些交流或推荐。可以写多个人。也可以不写。)

## 项目背景

目前在实现一个 PyTorch 到嵌入式 SoC（CPU/FPGA）的编译器，用户可以直接输入神经网络模型，经过我们的编译器优化后直接生成可执行文件并可以直接在对应后端设备上运行。

目前已经有该编译器的原型，也已经在 [Ultra96 V2](https://www.xilinx.com/products/boards-and-kits/1-vad4rl.html) 上进行过测试（该 SoC 上同样有 Linux 环境、ARM CPU 及嵌入式 FPGA），因此希望有更多的后端设备可以测试我们的编译器是否有足够的可移植性 (portability)，即针对不同的目标设备都能起到优化网络模型的作用。

## 项目目标

【展开标题说一两句。也可以是一个清单形式。】

1. 实现基本的 Linux 及 Python 环境部署
2. 实现一些简单的图层级优化方案，如算子融合和布局优化
3. 打通从前端 PyTorch 模型到后端设备运行的完整流程
4. 采用不同低位宽模型（FracBNN[^1], PokeBNN[^2]，UltraNet[^3]）进行测试，编译器优化后推理性能可以达到比手写后端代码的性能，甚至能够与 TVM[^4] 优化的网络性能进行比较
5. 执行图片分类、目标检测等通用计算机视觉任务并有可视化结果输出

## 预期成果

* 一个端到端的编译器可以实现 PyTorch 模型到嵌入式设备的编译及部署，会开源并有详细教程
* 完成后会写 Blog 文章，介绍整个 RISC-V 环境的部署及 PyTorch 模型推理和优化

## 预期时间表

* 2022.12 配置好基本的 Linux 及 Python 环境
* 2023.1 完成基本的优化算法，测试编译流程能够在该 RISC-V 板子上跑通
* 2023.2 测试编译后不同的网络模型的推理性能，主要测试低位宽卷积神经网络，并执行图片分类、目标检测等通用计算机视觉任务

## 成果展示

【提交 proposal 的时候不要填写，留白。等以后做出来之后，将相关的链接PR到这里即可。】


## 参考文献

[^1]: Yichi Zhang, Junhao Pan, Xinheng Liu, Hongzheng Chen, Deming Chen, Zhiru Zhang, **FracBNN: Accurate and FPGA-Efficient Binary Neural Networks with Fractional Activations**, FPGA, 2021
[^2]: Yichi Zhang, Zhiru Zhang, Lukasz Lew, **PokeBNN: A Binary Pursuit of Lightweight Accuracy**, CVPR, 2022
[^3]: https://github.com/heheda365/ultra_net
[^4]: Tianqi Chen, Thierry Moreau, Ziheng Jiang, Lianmin Zheng, Eddie Yan, Haichen Shen, Meghan Cowan, Leyuan Wang, Yuwei Hu, Luis Ceze, Carlos Guestrin, Arvind Krishnamurthy, **TVM: An Automated {End-to-End} Optimizing Compiler for Deep Learning**, OSDI, 2018
