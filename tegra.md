# tegra tips

+ Jetson TX1
    + [machine arch files for Jetson TX1 (Quad-core ARMCortex-A57 MPCore Processor)](http://yocto.yoctoproject.narkive.com/OOuKNJVm/machine-arch-files-for-jetson-tx1-quad-core-armcortex-a57-mpcore-processor)
    + [Yocto layer for the NVidia Tegra Jetson TK1 board](https://github.com/watatuki/meta-jetson-tk1)
    + [TX1 Yocto layer?](https://devtalk.nvidia.com/default/topic/935629/tx1-yocto-layer-/?offset=5)
    + [Manifests to create an Arch Linux ARM rootfs augmented with Nouveau and the OSS graphics stack for NVIDIA's Jetson TK1/TX1 boards](https://github.com/NVIDIA/tegra-nouveau-rootfs)
    + [tegra-uboot-flasher-scripts](https://github.com/NVIDIA/tegra-uboot-flasher-scripts/blob/master/README-developer.txt)
    + [tegra-scripts](https://github.com/scele/tegra-scripts)
    + [nvidia-persistenced](https://github.com/NVIDIA/nvidia-persistenced)
    + [tegra-uboot-scripts](https://github.com/NVIDIA/tegra-uboot-scripts)
    + [tegra-uboot-flasher-scripts](https://github.com/NVIDIA/tegra-uboot-flasher-scripts/blob/master/tegra-uboot-flasher)
    + [tegra-uboot-flasher-manifests](https://github.com/NVIDIA/tegra-uboot-flasher-manifests)
    + [Das U-Boot](http://www.denx.de/wiki/view/DULG/UBoot)
        + [git for Das U-Boot](http://git.denx.de/?p=u-boot.git;a=summary)
        + [U-Boot tegra](http://git.denx.de/?p=u-boot/u-boot-tegra.git;a=summary)
        + [Linux for Tegra](https://developer.nvidia.com/embedded/linux-tegra)
        + [TX1: how to recover CUDA and Nvidia/X11 drivers…](http://blog.kris-lab.com/2016/06/10/tx1-how-to-recover-cuda-and-nvidiax11-drivers/)
        + [tegra downloads](https://developer.nvidia.com/embedded/downloads)
        + [TX1/R23.1: New Flash Structure...How to Clone?](https://devtalk.nvidia.com/default/topic/898999/jetson-tx1/tx1-r23-1-new-flash-structure-how-to-clone-/post/4784149/#4784149)
        + [Updating TX1 driver package but not rootfs](https://devtalk.nvidia.com/default/topic/940485/updating-tx1-driver-package-but-not-rootfs/)
        + [Jetson/Cloning](http://elinux.org/Jetson/Cloning)
            + [tegrarcm](https://github.com/NVIDIA/tegrarcm)
            ```sh
            sudo python2 ./tegraflash.py --bl cboot.bin --applet nvtboot_recovery.bin --chip 0x21 --cmd "read APP my_backup_image_APP.img"
            Welcome to Tegra Flash
            version 1.0.0
            Type ? or help for help and q or quit to exit
            Use ! to execute system commands
             
            [   0.0011 ] Generating RCM messages
            Error: Could not find tegrarcm
            file ./tegrarcm
            ./tegrarcm: ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), statically linked, for GNU/Linux 2.6.8, not stripped

            ```
            + [Jetpack output when flashing Tegra X1](https://developer.ridgerun.com/wiki/index.php?title=Jetpack_output_when_flashing_Tegra_X1)
            + [NVIDIA/cbootimage](https://github.com/NVIDIA/cbootimage)
            + [org:NVIDIA tegra](https://github.com/search?q=org%3ANVIDIA+tegra)
            + [Flashing Jetson TX1 with tegraflash.py](https://devtalk.nvidia.com/default/topic/900378/tegra-tools/flashing-jetson-tx1-with-tegraflash-py/)
            + [nVidia Jetson TX1 Installation Guide](https://github.com/OpenPTrack/open_ptrack/wiki/Jetson-TX1-Installation)
            + [l4t_prebuilt_image](https://github.com/InES-HPMM/linux-l4t/wiki/l4t_prebuilt_image)
            + [NVIDIA TEGRA LINUX DRIVER PACKAGE QUICK-START GUIDE](http://developer.download.nvidia.com/embedded/L4T/r23_Release_v1.0/l4t_quick_start_guide.txt)
            + [Compiling Tegra X1 source code](https://developer.ridgerun.com/wiki/index.php?title=Compiling_Tegra_X1_source_code)
            + `flash.sh`
                + [NVIDIA Jetson TX1](https://rtime.felk.cvut.cz/hw/index.php/NVIDIA_Jetson_TX1)
                + [NVIDIA TEGRA LINUX DRIVER PACKAGE QUICK-START GUIDE](http://developer.download.nvidia.com/embedded/L4T/r23_Release_v1.0/l4t_quick_start_guide.txt)
                + [jetsonhacks/Install LT4 21.1.md](https://gist.github.com/jetsonhacks/2717a41f7e60a3405b34)

+ ARM cross compile
    + [Problems with linking arm objects : resolution](https://stackoverflow.com/questions/13235748/linker-error-on-a-c-project-using-eclipse)
        + [Problems with linking arm objects](https://bbs.archlinux.org/viewtopic.php?id=185630)
        ```sh
        /usr/lib/gcc/arm-none-eabi/4.9.1/../../../../arm-none-eabi/lib/libc.a(lib_a-exit.o): In function `exit':
        /build/arm-none-eabi-gcc/src/gcc-4.9.1/build/arm-none-eabi/newlib/libc/stdlib/../../../../../newlib/libc/stdlib/exit.c:70: undefined reference to `_exit'
        /usr/lib/gcc/arm-none-eabi/4.9.1/../../../../arm-none-eabi/lib/libc.a(lib_a-sbrkr.o): In function `_sbrk_r':
        ...
        ```
    ```sh
    arm-none-eabi-gcc hi.c -lc -specs=nosys.specs -o hi
    ```

    ```sh
    export ARCH=arm64
    export CROSS_COMPILE=/usr/bin/arm-none-eabi-
    export CROSS_COMPILE=/opt/armgcc/bin/

    ```
+ [Jetson TX1](http://elinux.org/Jetson_TX1)
    + [Tegra210 nvtboot-Based Boot Flow](ftp://download.nvidia.com/tegra-public-appnotes/t210-nvtboot-flow.html)
    + [Tegra Boot Flow](ftp://download.nvidia.com/tegra-public-appnotes/tegra-boot-flow.html)
    + [Built TX1 u-boot from source](https://devtalk.nvidia.com/default/topic/905345/jetson-tx1/built-tx1-u-boot-from-source/)

+ Das U-Boot programming
    + [U-Boot programming: A tutorial -- Part I](http://xillybus.com/tutorials/uboot-hacking-howto-1)
    + [U-Boot programming: A tutorial -- Part II](http://xillybus.com/tutorials/uboot-hacking-howto-2)
    + [U-Boot programming: A tutorial -- Part III](http://xillybus.com/tutorials/uboot-hacking-howto-3)

+ Cross compilation
    + [A versatile (cross-)toolchain generator.](https://github.com/crosstool-ng/crosstool-ng)
    + [Building embedded ARM systems with Crosstool-NG](https://briolidz.wordpress.com/2012/02/07/building-embedded-arm-systems-with-crosstool-ng/)
    + [Bash: Build Binutils, GCC, Newlib, and GDB for ARM EABI (Cross-compiler).](https://gist.github.com/cjmeyer/4251208)
    + [building U-boot](http://odroid.com/dokuwiki/doku.php?id=en:c1_building_u-boot)
    + SDL
        + [SDL - **S**imple **D**irect**M**edia](https://www.libsdl.org/)
        + [SDL installation](https://wiki.libsdl.org/Installation)
        + [Building embedded ARM systems with Crosstool-NG](https://briolidz.wordpress.com/2012/02/07/building-embedded-arm-systems-with-crosstool-ng/)
        + [SDL: How To Build for ARM](https://how-to-build-for-arm.wikispaces.com/sdl)
        + [SDL2: How To Build for ARM](https://how-to-build-for-arm.wikispaces.com/sdl2)
            + [dbus-arch-deps.h missing from usr/include/dbus-1.0/dbus](https://bugs.launchpad.net/ubuntu/+source/dbus/+bug/992463)
            + [symlink for dbus headers](http://askubuntu.com/questions/40763/symlink-for-dbus-headers)
            + TL;DR
            ```sh
            pkg-config dbus-1 --cflags
            ```
+ [Android sparse image format](http://www.2net.co.uk/tutorial/android-sparse-image-format)
