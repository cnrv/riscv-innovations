# [rootfs 构建工具](https://github.com/initdc/rootfs-tools)

rootfs 操作命令集及自动构建流程。

## 参与人

【 github: [initdc](https://github.com/initdc) 】

## 项目背景

挂载 rootfs 需要输入的命令太多，chroot 应该安装什么依赖？ 创建修改 rootfs 的资源和教程多且零散，本项目致力于新手快速入门 rootfs 工程。

## 项目目标

1. 为 LicheeRV 生成 Wi-Fi（驱动、配置软件）预建的 Ubuntu 镜像。
2. 构建其他 Linux 发行版。
3. 测试 多语言跨平台编译成果。详见 [Project Workflow](https://github.com/initdc?tab=repositories&q=project-workflow&type=&language=&sort=)
4. Geekbench 5 性能测试。参考 [其他测试结果](https://browser.geekbench.com/user/425390)

## 预期成果

1. LicheeRV 愉快的开箱体验，无须烦恼 不能无线接入网络。
2. 在 LicheeRV 玩到自己喜欢的发行版。

## 预期时间表

**2022-12**

- 构建 Wi-Fi 驱动 module for Linux 5.x
- 发布预构建镜像

**2023**

- 适配其他 Linux 发行版。

## 成果展示

0. 构建 rtl8723ds Wi-Fi 驱动 [5.17.0-1003-allwinner_1.0-0ubuntu1.2](https://github.com/initdc/rtl8723ds/releases/tag/5.17.0-1003-allwinner_1.0-0ubuntu1.2)

   仓库: https://github.com/initdc/rtl8723ds

   本机安装方式（需重启）:

   ```
   install -p -m 644 8723ds.ko /lib/modules/$(uname -r)/kernel/drivers/net/wireless/
   /sbin/depmod -a  $(uname -r)
   ```

1. 预建 Wi-Fi 驱动的 Ubuntu 镜像 [ubuntu-22.10-server-licheerv_mod-wifi](https://github.com/initdc/rootfs-tools/releases/tag/licheerv-22.10)

   下载地址：[ubuntu-22.10-preinstalled-server-riscv64+licheerv_mod-wifi.img.xz](https://github.com/initdc/rootfs-tools/releases/download/licheerv-22.10/ubuntu-22.10-preinstalled-server-riscv64+licheerv_mod-wifi.img.xz)

   > SHA256SUM: `8a12292c68db3b041e640e4e3dee61a97617962ecf0ea64198dc9c00926a991a`

   指南跟随: https://wiki.ubuntu.com/RISC-V/LicheeRV

   - 烧录到 SD 卡使用 [Rufus](https://github.com/pbatard/rufus/releases) - [3.21p](https://github.com/pbatard/rufus/releases/download/v3.21/rufus-3.21p.exe)

   - 设置

     ```
     sudo nano /etc/netplan/wifi.yaml
     ```

     粘贴并修改 Wi-Fi 信息

     ```
     network:
       version: 2
       renderer: networkd
       wifis:
         wlan0:
           dhcp4: yes
           dhcp6: yes
           access-points:
             "你的Wi-Fi":
               password: "你的密码"
     ```

     <kbd>Ctrl</kbd> + <kbd>O</kbd>, <kbd>Enter</kbd> 保存

     ```
     sudo netplan apply
     ```

2. 多语言跨平台编译 的 二进制文件测试

   > 测试使用 [multi-run](https://github.com/initdc/multi-run)

   ```ruby
   {"temp_bin/c_riscv64-linux-gnu-gcc"=>true,
   "temp_bin/c_riscv64-linux-musl"=>true,
   "temp_bin/dlang_riscv64-linux-gnu-gdc"=>false,
   "temp_bin/golang_demo-v0.0.3-linux-riscv64"=>true,
   "temp_bin/nim_riscv64-linux-gnu-gcc"=>true,
   "temp_bin/rust_riscv64gc-unknown-linux-gnu"=>true,
   "temp_bin/zig_riscv64-linux-gnu"=>true,
   "temp_bin/zig_riscv64-linux-musl"=>true}
   ```

3. GeekBench 5

   - Single-Core Score: 33
   - Multi-Core Score: 33
   - 详见 https://browser.geekbench.com/v5/cpu/19242722
