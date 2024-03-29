# tegra tips

+ Jetson TX1 & TX2 & Xavier
    + [Jetson Easy: easy installer for NVidia Jetson](https://www.rnext.it/project/jetson-easy/)
        + [Jetson Easy setup configurator](https://github.com/rbonghi/jetson_easy)
        + [Basic scripts and function to improve the performance in your NVIDIA Jetson](https://github.com/rbonghi/jetson_stats)
    + [Some Jetson Web Links](https://devtalk.nvidia.com/default/topic/793798/embedded-systems/some-jetson-web-links/)
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
        + [Flashing with tegrarcm](https://devtalk.nvidia.com/default/topic/900528/flashing-with-tegrarcm/?offset=3)
        + [Flash nvidia jetson tx1](https://github.com/madisongh/meta-tegra/issues/12)
        ```sh
        git clone -b krogoth git://git.yoctoproject.org/poky.git 
        cd poky
        git clone https://github.com/madisongh/meta-tegra
        . oe-init-build-env build_jetson
        cd build_jetson/conf/
        ...
        ```
    + [Jetson/Porting Arch](http://elinux.org/Jetson/Porting_Arch)

    + **SPI** - **S**erial **P**eripheral **I**nterface
        + [Using the Jetson TK1 SPI - Part 1 (Why is SPI important)](http://neurorobotictech.com/Community/Blog/tabid/184/ID/11/Using-the-Jetson-TK1-SPI--Part-1-Why-is-SPI-important.aspx)
        + [Using the Jetson TK1 SPI - Part 3 (Configuring SPI in the device tree)](http://neurorobotictech.com/Community/Blog/tabid/184/ID/13/Using-the-Jetson-TK1-SPI--Part-3-Configuring-SPI-in-the-device-tree.aspx)

    + [Das U-Boot](http://www.denx.de/wiki/view/DULG/UBoot)
        + [git for Das U-Boot](http://git.denx.de/?p=u-boot.git;a=summary)
        + [U-Boot tegra](http://git.denx.de/?p=u-boot/u-boot-tegra.git;a=summary)
        + [Linux for Tegra](https://developer.nvidia.com/embedded/linux-tegra)
        + [TX1: how to recover CUDA and Nvidia/X11 drivers…](http://blog.kris-lab.com/2016/06/10/tx1-how-to-recover-cuda-and-nvidiax11-drivers/)
        + [tegra downloads](https://developer.nvidia.com/embedded/downloads)
        + [TX1/R23.1: New Flash Structure...How to Clone?](https://devtalk.nvidia.com/default/topic/898999/jetson-tx1/tx1-r23-1-new-flash-structure-how-to-clone-/post/4784149/#4784149)
        + [Updating TX1 driver package but not rootfs](https://devtalk.nvidia.com/default/topic/940485/updating-tx1-driver-package-but-not-rootfs/)
        + cross compile U-Boot
        ```sh
        export CROSS_COMPILE=/opt/linaro/gcc-linaro-5.3-2016.02-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-
        export ARCH=arm64
        make distclean
        make p2371-2180_defconfig
        make
        ```
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
    + [**Tegra210 nvtboot-Based Boot Flow**](http://http.download.nvidia.com/tegra-public-appnotes/t210-nvtboot-flow.html)
    + [**Tegra Boot Flow**](http://http.download.nvidia.com/tegra-public-appnotes/tegra-boot-flow.html)
    + [**Built TX1 u-boot from source**](https://devtalk.nvidia.com/default/topic/905345/jetson-tx1/built-tx1-u-boot-from-source/)

+ Das U-Boot programming
    + [Banana Pi: через U-Boot к Arch Linux](https://habrahabr.ru/post/264259/)
    + [U-Boot programming: A tutorial -- Part I](http://xillybus.com/tutorials/uboot-hacking-howto-1)
    + [U-Boot programming: A tutorial -- Part II](http://xillybus.com/tutorials/uboot-hacking-howto-2)
    + [U-Boot programming: A tutorial -- Part III](http://xillybus.com/tutorials/uboot-hacking-howto-3)
    + [Tegra/Mainline SW/U-Boot](http://elinux.org/Tegra/Mainline_SW/U-Boot)
    + [extlinux.conf](https://github.com/ppisa/rpi-utils/blob/master/u-boot-setup/boot/extlinux/extlinux.conf)
    ```
    TIMEOUT 100
    DEFAULT default
    MENU TITLE Boot menu
    
    LABEL default
        MENU LABEL Linux 3.18.8-rt2+ with Overlay
        LINUX vmlinuz-3.18.8-rt2+
        FDTDIR .
        APPEND dwc_otg.lpm_enable=0 console=ttyAMA0,115200 kgdboc=ttyAMA0,115200 smsc95xx.macaddr=${usbethaddr} root=/dev/mmcblk0p2 rootfstype=ext4 elevator=deadline rootwait ro init=/sbin/init-overlay
    
    LABEL aufs
        MENU LABEL Linux 3.18.8-rt2+ with Aufs
        LINUX vmlinuz-3.18.8-rt2+
        FDTDIR .
        APPEND dwc_otg.lpm_enable=0 console=ttyAMA0,115200 kgdboc=ttyAMA0,115200 smsc95xx.macaddr=${usbethaddr} root=/dev/mmcblk0p2 rootfstype=ext4 elevator=deadline rootwait ro OVERLAY=aufs init=/sbin/init-overlay
    
    LABEL rw
        MENU LABEL Linux 3.18.8-rt2+ RW root
        LINUX vmlinuz-3.18.8-rt2+
        FDTDIR .
        APPEND dwc_otg.lpm_enable=0 console=ttyAMA0,115200 kgdboc=ttyAMA0,115200 smsc95xx.macaddr=${usbethaddr} root=/dev/mmcblk0p2 rootfstype=ext4 elevator=deadline rootwait ro
    
    LABEL nfs-busybox
        MENU LABEL Linux 3.18.8-rt2+ NFS BusyBox
        LINUX vmlinuz-3.18.8-rt2+
        FDTDIR .
        APPEND dwc_otg.lpm_enable=0 console=ttyAMA0,115200 kgdboc=ttyAMA0,115200 smsc95xx.macaddr=${usbethaddr} root=/dev/nfs rw nfsroot=192.168.1.10:/srv/nfs/rpi ip=192.168.1.33:::::eth0 elevator=deadline rootwait
    ...
    ```

    + [PXELINUX](http://www.syslinux.org/wiki/index.php?title=PXELINUX)
    ```sh
    gvim u-boot/common/cmd_pxe.c u-boot/common/cmd_ext2.c uboot/fs/fs.c
    ```
    ```c
    static int get_relfile(cmd_tbl_t *cmdtp, const char *file_path,
	    unsigned long file_addr)
        ...
	    strcat(relfile, file_path);

	    printf("Retrieving file: %s\n", relfile);

	    sprintf(addr_buf, "%lx", file_addr);

	    return do_getfile(cmdtp, relfile, addr_buf);
    ```

    + U-Boot scripts
        + [Where does U-Boot saveenv to?](https://forums.xilinx.com/t5/Embedded-Linux/Where-does-U-Boot-saveenv-to/td-p/532915)

    + [U-Boot splash screen on Jetson TX1](https://devtalk.nvidia.com/default/topic/994301/jetson-tx1/l4t-24-2-plymouth-boot-splash/)

+ PCI & PCIe
    + [The PCI Interface & PCI Addressing](http://www.makelinux.net/ldd3/chp-12-sect-1)
    + [Considerations for host-to-FPGA PCIe traffic](http://xillybus.com/tutorials/pci-express-dma-requests-completions)
    + [Down to the TLP: How PCI express devices talk (Part I)](http://xillybus.com/tutorials/pci-express-tlp-pcie-primer-tutorial-guide-1)
    + [Down to the TLP: How PCI express devices talk (Part II)](http://xillybus.com/tutorials/pci-express-tlp-pcie-primer-tutorial-guide-2)
    + [gittup.org's pciutils](https://github.com/gittup/pciutils)
        + [lspci “Memory at…” vs /proc/bus/pci/devices BAR address](https://serverfault.com/questions/745888/lspci-memory-at-vs-proc-bus-pci-devices-bar-address)


+ Cross compilation
    + [A versatile (cross-)toolchain generator.](https://github.com/crosstool-ng/crosstool-ng)
    + [Cross Compiling Environment Setup For ARM Architecture Pidora OS](https://johnsofteng.wordpress.com/2013/09/02/cross-compiling-environment-setup-for-arm-architecture/)
    + [Building embedded ARM systems with Crosstool-NG](https://briolidz.wordpress.com/2012/02/07/building-embedded-arm-systems-with-crosstool-ng/)
    + [Bash: Build Binutils, GCC, Newlib, and GDB for ARM EABI (Cross-compiler).](https://gist.github.com/cjmeyer/4251208)
    + [building U-boot](http://odroid.com/dokuwiki/doku.php?id=en:c1_building_u-boot)
    + [Jetson/TX1 Upstream Kernel](http://elinux.org/Jetson/TX1_Upstream_Kernel)
    + [tegra-uboot-flasher-scripts : README-developer](https://github.com/NVIDIA/tegra-uboot-flasher-scripts/blob/master/README-developer.txt)
    + [**Compiling Tegra X1 source code**](https://developer.ridgerun.com/wiki/index.php?title=Compiling_Tegra_X1_source_code)
    + [[meta-fsl-arm,5/5] u-boot: fix build error under gcc6](https://patchwork.openembedded.org/patch/124049/)
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
+ [Device Tree for dummies](https://events.linuxfoundation.org/sites/events/files/slides/petazzoni-device-tree-dummies.pdf)

+ Docker
    + [NVIDIA Docker Container User Guide](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/user-guide.html)
    + [issue creating containers due to seccomp failure (error adding seccomp filter rule for syscall clone3: permission denied: unknown](https://github.com/containerd/containerd/issues/6203)
        tl;dr    
        ```sh
        sudo dpkg -i docker.io_20.10.2-0ubuntu1_18.04.2_arm64.deb 
        [sudo] password for alsam: 
        dpkg: warning: downgrading docker.io from 20.10.7-0ubuntu5~18.04.3 to 20.10.2-0ubuntu1~18.04.2
        (Reading database ... 214354 files and directories currently installed.)
        Preparing to unpack docker.io_20.10.2-0ubuntu1_18.04.2_arm64.deb ...
        Unpacking docker.io (20.10.2-0ubuntu1~18.04.2) over (20.10.7-0ubuntu5~18.04.3) ...
        Setting up docker.io (20.10.2-0ubuntu1~18.04.2) ...
        Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
        ...
        sudo apt-mark hold docker.io
        ```
+ misc
    + [Unknown command 'jetson_release' (pip command not found)](https://github.com/rbonghi/jetson_stats/issues/171)
        tl;dr    
        ```sh
        $ sudo -H pip3 install -U setuptools
        Collecting setuptools
          Downloading https://files.pythonhosted.org/packages/b0/3a/88b210db68e56854d0bcf4b38e165e03be377e13907746f825790f3df5bf/setuptools-59.6.0-py3-none-any.whl (952kB)
            100% |████████████████████████████████| 962kB 768kB/s 
        Installing collected packages: setuptools
        Successfully installed setuptools-59.6.0
        $ sudo -H pip3 install -U jetson-stats
        Collecting jetson-stats
        ```

    + [Number of CPU cores on Jetson Xavier](https://forums.developer.nvidia.com/t/number-of-cpu-cores-on-jetson-xavier/69227)
        tl;dr    
        ```sh
        sudo nvpmodel -m 2
        ```
    + restore screen after removing an inserting HDMI
        tl;dr    
        ```sh
        sudo xrandr -s 1
        ```
    + [Enhancements of the massively parallel memory allocator ScatterAlloc and its adaption to the general interface mallocMC](https://zenodo.org/record/34461/files/mallocMC_final.pdf)
    + Network Troubleshooting
        + [Jetson/Remote Access](http://elinux.org/Jetson/Remote_Access)
        + tl;dr
        ```sh
        sudo service networking start
        sudo service network-manager start
        ```

    + cursor disable in X11
        + [cursor disable in X11](http://www.noah.org/wiki/cursor_disable_in_X11)
        ```sh
        cat /lib/systemd/system/X.service
        ...
        ExecStart=/usr/bin/startx -- -nocursor
        ...
        sudo systemctl daemon-reload
        sudo systemctl restart X
        ```
        + [red herring - hhpc](https://github.com/Aktau/hhpc)
        + [How to hide the mouse cursor](https://askubuntu.com/questions/157134/how-to-hide-the-mouse-cursor/586718)

    + [How do I disable my system from going to sleep?](http://askubuntu.com/questions/47311/how-do-i-disable-my-system-from-going-to-sleep)
    ```sh
    sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
    ```

    + [How do I know what version of L4T my Jetson TX1 is running?](https://devtalk.nvidia.com/default/topic/860092/jetson-tk1/how-do-i-know-what-version-of-l4t-my-jetson-tk1-is-running-/)
        tl;dr
        ```sh
        cat /etc/nv_tegra_release
        ```

    + [Bernese GNSS Software](http://www.bernese.unibe.ch)
        + [Bernese GNSS](https://swmath.org/software/26184)

    + [Low frame rate](https://github.com/dusty-nv/jetson-inference/issues/891)

    + [NVIDIA AI IOT](https://github.com/NVIDIA-AI-IOT)

    + [QtCAM is a free, Open Source Linux Webcamera Software with more than 10 image control settings, extension settings and Color space switching](https://github.com/econsysQtCAM/QtCAM)
    ```sh
    sudo apt-get install qtmultimedia5-dev libqt5multimediawidgets5 libqt5multimedia5-plugins libqt5multimedia5 qtdeclarative5
    sudo apt-get install libjpeg-turbo8 libjpeg-turbo8-dev libturbojpeg0-dev libevdev-dev
    ```

    + [Getting started with the Deep Learning Accelerator on NVIDIA Jetson Orin](https://github.com/NVIDIA-AI-IOT/jetson_dla_tutorial)

    + GStreamer
        + [Play webcam using gstreamer](https://medium.com/@petehouston/play-webcam-using-gstreamer-9b7596e4e181)
            + [ERROR: from element /GstPipeline:pipeline0/GstV4l2Src:v4l2src0: Internal data stream error.](https://github.com/awslabs/amazon-kinesis-video-streams-producer-sdk-cpp/issues/205)
        + [How to write a CMAKE file which successfully links gstreamer basic tutorial 5](https://stackoverflow.com/questions/64078308/how-to-write-a-cmake-file-which-successfully-links-gstreamer-basic-tutorial-5)
        + [Gstreamer docs](https://low-level.readthedocs.io/en/latest/applications/)

    + [DATA PLANE DEVELOPMENT KIT (DPDK)](https://developer.nvidia.com/networking/dpdk)
        + [Environment Abstraction Layer](https://doc.dpdk.org/guides/prog_guide/env_abstraction_layer.html#max-simd-bitwidth)
