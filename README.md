# VCU108 Support for Chipyard FPGA Prototyping

> 增加 Chipyard 中对 VCU108 开发板的支持，以走 FPGA Prototyping 的流程。

快速开始：将包含本项目的文件夹命名为 `fpga`，然后替换掉 `chipyard` 目录下的 `fpga` 文件夹即可使用。

原理：
Chipyard 原本仅支持 VCU118 和 arty。为了增加对其它开发板的支持，以 VCU108 开发板为例，需要修改或添加以下文件：
1. 修改 Makefile (`chipyard/fpga/Makefile`)，增加 `SUB_PROJECT` 对 VCU108 的匹配；
2. 在 `chipyard/fpga/src/main/scala/vcu108` 文件夹内，加入 VCU108 相应的配置；
3. 在 `chipyard/fpga/fpga-shells/xilinx/vcu108` 文件夹内配置板卡；
4. 在 `chipyard/fpga/fpga-shells/src/main/scala/shell/xilinx/VCU108shell.scala` 中配置时钟和外设引脚；
5. (?) ~~在 `chipyard/fpga/fpga-shells/src/main/scala/ip/xilinx/vcu440mig/vcu440mig.scala` 中配置DDR4 IP核，生成MIG~~。

Credit to @ariusewy
