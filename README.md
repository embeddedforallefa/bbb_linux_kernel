The kernel build sequences for bbb are followed as listed in the below link:
https://www.itdev.co.uk/blog/building-linux-kernel-cross-compiling-beaglebone-black 

sudo apt-get install gcc-arm-linux-gnueabi

git clone git://github.com/beagleboard/linux.git

cd linux/

make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- bb.org_defconfig

make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- menuconfig

make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- LOADADDR=0x80000000 uImage dtbs

make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- modules
