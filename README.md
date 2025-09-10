# nofrendo_fork
[WIP] My nofrendo fork

## Ref
* (origin, dead) http://www.baisoku.org/nofrendo-2.0pre1.zip
* https://github.com/weimingtom/wmt_stm32_study/?tab=readme-ov-file#nofrendo-stm32f4
* https://github.com/rickyzhang82/nofrendo
```
nofrendo_linux_v2_ubuntu_run_uintptr_t.tar.gz  
nofrendo_vc6_v9_min.rar  
nofrendo-2.0pre1.zip  
```

## How to build for Xubuntu 20.04
* $ cd src/xubuntu
* $ make clean
* $ make -j8
* $ ./nofrendo ~/DEMO.NES

## How to build for LiuLianPi V3S
* $ cd src/liulianpi_v3s
* $ make clean
* $ make -j8
* Copy file "nofrendo" to tf card
* Login UART (COMx) console with Putty
* \# mkdir /mnt/SDCARD
* \# mount /dev/mmcblk0p1 /mnt/SDCARD/
* \# cd /mnt/SDCARD/nofrendo/
* \# SDL_NOMOUSE=1 ./nofrendo ./DEMO.NES
