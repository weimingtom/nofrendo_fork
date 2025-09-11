# nofrendo_fork
[WIP] My nofrendo fork

## Ref
* (origin) https://web.archive.org/web/20210419085348/http://www.baisoku.org
* (origin) https://web.archive.org/web/20210419085348/http://www.baisoku.org/nofrendo-2.0pre1.zip
* (origin, dead) http://www.baisoku.org/nofrendo-2.0pre1.zip
* https://github.com/weimingtom/wmt_stm32_study/?tab=readme-ov-file#nofrendo-stm32f4
* (origin) https://github.com/rickyzhang82/nofrendo   
Sometimes it can run ./configure better than nofrendo-2.0pre1.zip  
```
nofrendo-2.0pre1.zip  
nofrendo_linux_v2_ubuntu_run_uintptr_t.tar.gz  
nofrendo_vc6_v9_min.rar  
(for ./configure) nofrendo_linux_v2_ubuntu.tar.gz
nofrendo_linux_v1.tar.gz
```

## How to build for Xubuntu 20.04 64bit (x86_64, amd64)  
* $ cd src/xubuntu
* $ make clean
* $ make -j8
* Copy file "DEMO.NES" to ~/.
* $ ./nofrendo ~/DEMO.NES

## (WIP) (TODO) How to build for LiuLianPi V3S (Allwinner v3s, ARM 32bit Cortex-A7)  
* Get toolchain gcc-linaro-6.3.1-2017.05-x86_64_arm-linux-gnueabihf.tar.xz  
https://w.electrodragon.com/w/ARM_GCC  
https://releases.linaro.org/components/toolchain/binaries/6.3-2017.05/arm-linux-gnueabihf/  
https://releases.linaro.org/components/toolchain/binaries/6.3-2017.05/arm-linux-gnueabihf/gcc-linaro-6.3.1-2017.05-x86_64_arm-linux-gnueabihf.tar.xz  
* See src/liulianpi_v3s/Makefile, tar xf gcc-linaro-6.3.1-2017.05-x86_64_arm-linux-gnueabihf.tar.xz to /home/wmt/work_v3s/gcc-linaro-6.3.1-2017.05-x86_64_arm-linux-gnueabihf
* $ cd src/liulianpi_v3s  
* $ make clean
* $ make -j8
* Copy file "nofrendo" and "DEMO.NES" to tf card
* Login UART (COMx) console with Putty
* \# mkdir /mnt/SDCARD
* \# mount /dev/mmcblk0p1 /mnt/SDCARD/
* \# cd /mnt/SDCARD/nofrendo/
* \# SDL_NOMOUSE=1 ./nofrendo ./DEMO.NES
