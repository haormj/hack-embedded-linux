## 嵌入式

### 概述

本文档只是想记录一些个人理解嵌入式的过程，主要通过 Q&A 进行

### Q&A

1. 在进行之前是否有推荐的资料？
    - 嵌入式 linux 基础教程
    - Making Embedded Linux Easy https://buildroot.org/ 
    - Embedded Linux and kernal engineering https://bootlin.com/
    - Buildroot development course https://bootlin.com/doc/training/buildroot/  
    - busybox https://www.busybox.net/ 
2. 你在过程中是否有使用开发板实验？
    - Raspberry Pi 4 https://www.raspberrypi.org/products/raspberry-pi-4-model-b/   
3. 如何使用 buildroot 制作树莓派 4 固件
    - buildroot 命令 https://github.com/buildroot/buildroot/tree/master/board/raspberrypi 
    - buildroot docker 可以简单修改 Dockerfile 更新版本 https://github.com/AdvancedClimateSystems/docker-buildroot 
4. buildroot 镜像打包完成后，系统启动如何将自己的应用在系统中运行？
    - 需要使用 buildroot output/host/bin 中的交叉编译工具对自己的应用进行编译
    - 然后就可以将自己的应用拷贝到系统中尝试
    - 正式发布的时候，需要在 buildroot 中将自己应用进行添加，并使用 sysvinit/systemd 运行
5. 有没有类似buildroot的其他嵌入式构建工具？
    - OpenEmbedded http://www.openembedded.org/
    - Yocto https://www.yoctoproject.org/
