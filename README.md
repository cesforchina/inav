# 在Windows 10中使用Linux子系统构建

用于Windows 10的Linux子系统可能是在Windows 10下构建INAV的最简单方法。

1. 使用来自Internet的任何指南启用WSL（Windows Subsystem for Linux）
1. 从Windows应用商店安装 `Ubuntu`
1. 开始`Ubuntu`并运行:
1. `git clone https://github.com/cesforchina/inav-2.1.0.git`
1. `cd inav-2.1.0`
1. `sudo add-apt-repository ppa:team-gcc-arm-embedded/ppa`
1. `sudo apt-get update`
1. `sudo apt-get install gcc-arm-embedded make ruby`

它将安装 `gcc-arm-none-eabi` 版本 _7 q4_

从这时起，可以使用以下命令构建INAV

`make TARGET={TARGET_NAME}`

当然，将`{TARGET_NAME}`替换为您要编译的目标
