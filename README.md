# 在Windows 10中使用Linux子系统构建

用于Windows 10的Linux子系统可能是在Windows 10下构建INAV的最简单方法。

1. Enable WSL (_Windows Subsystem for Linux) using any guide from internet. [This](https://winaero.com/blog/enable-wsl-windows-10-fall-creators-update/) is up to date step by step (January 2018)
1. From _Windows Store_ install `Ubuntu`
1. Start `Ubuntu` and run:
1. `sudo add-apt-repository ppa:team-gcc-arm-embedded/ppa`
1. `sudo apt-get update`
1. `sudo apt-get install gcc-arm-embedded make ruby`

目前（2018年1月）它将安装 `gcc-arm-none-eabi` 版本 _7 q4_

从这时起，可以使用以下命令构建INAV

`make TARGET={TARGET_NAME}`

当然，将`{TARGET_NAME}`替换为您要编译的目标
