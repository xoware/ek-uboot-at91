./cross-make.sh xoware_exokey_config
./cross-make.sh all



$ cat cross-make.sh 
#!/bin/bash

unset CFLAGS CPPFLAGS CXXFLAGS LDFLAGS MACHINE

ARCH=arm CCPREFIX=/home/karl/Work/yocto/poky-dylan-9.0.2/build_ek/tmp/sysroots/x86_64-linux/usr/bin/cortexa9hf-vfp-poky-linux-gnueabi/arm-poky-linux-gnueabi- \
HOSTCC='arm-poky-linux-gnueabi-gcc  -mno-thumb-interwork -marm' HOSTLD='arm-poky-linux-gnueabi-ld  ' \
CROSS_COMPILE=${CCPREFIX}  make  $@

