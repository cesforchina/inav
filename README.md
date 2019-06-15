# 在Windows 10中使用Linux子系统构建

用于Windows 10的Linux子系统可能是在Windows 10下构建INAV的最简单方法。

1. 使用来自Internet的任何指南启用WSL（Windows Subsystem for Linux）
1. 从Windows应用商店安装 `Ubuntu`
1. 打开`Ubuntu`并运行:
1. `git clone https://github.com/cesforchina/inav-2.1.0.git`克隆我的inav-2.1.0储存库（也可以从inav官方储存库克隆，要进行分支切换等操作，此处不再赘述）
1. `cd inav-2.1.0`进入项目文件夹
1. `sudo add-apt-repository ppa:team-gcc-arm-embedded/ppa`
1. `sudo apt-get update`
1. `sudo apt-get install gcc-arm-none-eabi`
1. `arm-none-eabi-gcc -v`查询版本号(非必需操作，仅用来确认gcc版本)

它将安装 `gcc-arm-none-eabi` gcc version 6.3.1 20170620

从这时起，可以使用以下命令构建INAV

`make TARGET={TARGET_NAME}`

当然，将`{TARGET_NAME}`替换为您要编译的目标
