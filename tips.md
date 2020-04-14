# useful tips

+ Linux distribution tips

    + Gentoo tips
        + [Gentoo Cheat Sheet](https://wiki.gentoo.org/wiki/Gentoo_Cheat_Sheet)
    
    + Arch Linux tips
        + [Arch Linux config files](https://github.com/afiskon/archlinux-on-desktop)
        + [Archlinux PKGBUILDs for Data Science, Machine Learning, Deep Learning, NLP and Computer Vision](https://github.com/mratsim/Arch-Data-Science)
        + first installation
            tl;dr
            don't forget to add UEFI partition at 1st installation `boot/UEFI`
            + [Установка ArchLinux в режиме UEFI + systemd-boot + XFCE4 Часть первая](https://www.youtube.com/watch?v=pUBpGjybH6Q)
            + [Установка ArchLinux в режиме UEFI + systemd-boot + XFCE4 Часть вторая](https://www.youtube.com/watch?v=LisOqIrgba0)
            + [Установка ArchLinux в режиме UEFI + systemd-boot + XFCE4 Часть третья: Настройка XFCE](https://www.youtube.com/watch?v=jjNOcfdB-Ng)
            tl;dr    
            ```sh
            ls /sys/firmware/efi/efivars/
            ...
            lsblk
            ...
            [0:52]
            root@archiso ~ # gdisk /dev/sda
            GPT fdisk (gdisk) version ...
            ...
            [3:25]
            root@archiso ~ # timedatectl set-ntp true
            nano /etc/pacman.d/mirrorlist
            ...
            root@archiso ~ # mount /dev/sdc2 /mnt
            root@archiso ~ # mkdir -p /mnt/{boot,home}
            root@archiso ~ # mount /dev/sdc1 /mnt/boot
            ...
            root@archiso ~ # pacstrap -i /mnt base base-devel
            [8:00]
            ...
            root@archiso ~ # genfstab -U -p /mnt >> /mnt/etc/fstab
            root@archiso ~ # arch-chroot /mnt /bin/bash
            [root@archiso / ]# nano /etc/locale.gen
            [root@archiso / ]# locale-gen
            [root@archiso / ]# hwclock --systohc --utc 
            [root@archiso / ]# ln -s /usr/share/zoneinfo/Europe/Moscow /etc/localtime
            [root@archiso / ]# rm /etc/localtime
            [root@archiso / ]# ln -s /usr/share/zoneinfo/Europe/Moscow /etc/localtime
            [root@archiso / ]# nano /etc/vconsole.conf
            [root@archiso / ]# cat /etc/vconsole.conf 
            KEYMAP=ru
            FONT=cyr-sun16
            ...
            [root@archiso / ]# echo myhostname > /etc/hostname
            [root@archiso / ]# nano /etc/hosts
            [root@archiso / ]# pacman -S iw wpa_supplicant dialog wpa_actiond net_tools mc bash_completion networkmanager
            [root@archiso / ]# systemctl enable NetworkManager.service
            [root@archiso / ]# passwd
            [root@archiso / ]# useradd -m snuppy
            [root@archiso / ]# passwd snuppy
            [root@archiso / ]# usermod -G audio,games,lp,optical,video,power,scanner,storage,wheel snuppy
            [root@archiso / ]# nano /etc/sudoers
            [16:14]
            ...
            [root@archiso / ]# bootctl --path=/boot install
            Created "/boot/EFI".
            Created "/boot/systemd".
            Created "/boot/BOOT".
            Created "/boot/loader".
            Created "/boot/loader/entries".
            Copied "/usr/lib/systemd/boot/efi/systemd-bootx64.efi" to "/boot/EFI/systemd/systemd-bootx64.efi".
            Copied "/usr/lib/systemd/boot/efi/systemd-bootx64.efi" to "/boot/EFI/BOOT/BOOTX64.EFI".
            Created EFI boot entry "Linux Boot Manager".
            [root@archiso / ]# nano /boot/loader/loader.conf
            ...
            default arch
            [root@archiso / ]# nano /boot/loader/entries/arch.conf
            [root@archiso / ]# bootctl update
            [root@archiso / ]# bootctl list
            [root@archiso / ]# mkinitcpio -p linux
            reboot
            ```

            + [Image creation and activation](https://wiki.archlinux.org/index.php/Mkinitcpio#Image_creation_and_activation)

            + [Offline installation](https://wiki.archlinux.org/index.php/Offline_installation)
                + [Archiso](https://wiki.archlinux.org/index.php/Archiso)
                    + [Archiso offline](https://wiki.archlinux.org/index.php/Archiso_offline)    
                    ```sh
                    mkdir -p /tmp/iso_build_dir
                    cp -r /usr/share/archiso/configs/offline_releng/* /tmp/iso_build_dir/
                    cd /tmp/iso_build_dir/
                    echo "python" >> packages.x86_64
                    echo "ripgrep" >> packages.x86_64
                    echo "cntlm" >> packages.aur
                    sudo rm -rf work*
                    sudo ./build.sh -v
                    ls -al out/archlinux-2020.03.13-x86_64.iso 
                    sudo dd if=out/archlinux-2020.03.13-x86_64.iso of=/dev/sde1 status=progress oflag=sync bs=4M
                    ```

            + [WARNING **: Couldn't connect to accessibility bus](https://bbs.archlinux.org/viewtopic.php?id=228894)
                tl;dr
                ```
                export NO_AT_BRIDGE=1
                ```
            + add to /boot/loader/entries/arch.conf  `sudo blkid -s PARTUUID -o value /dev/sda2`

            + [Firmware Bug]: TSC_DEADLINE disabled due to Errata: please ipdate microcode to version: 0x52 (or later)
                + [Firmware Bug TSC_DEADLINE disabled due to Errata](https://bbs.archlinux.org/viewtopic.php?id=230516)
                    + [Microcode](https://wiki.archlinux.org/index.php/Microcode#Enabling_early_microcode_loading_in_custom_kernels)
                        + [Intel-ucode](https://www.archlinux.org/packages/?name=intel-ucode)
                        + [coreboot: Fast, secure and flexible OpenSource firmware](https://www.coreboot.org)

            + ~[install-yaourt-arch-linux](https://www.ostechnix.com/install-yaourt-arch-linux/)~
                + [Yaourt is Dead! Use These Alternatives for AUR in Arch Linux](https://itsfoss.com/best-aur-helpers/)
                    + [Yet another Yogurt - An AUR Helper written in Go ](https://github.com/Jguer/yay)    
                    TL;DR    
                    ```sh
                    git clone https://aur.archlinux.org/yay.git
                    cd yay
                    makepkg -si
                    ```
                    + [Pacman wrapper with AUR support : written in **nim**](https://github.com/kitsunyan/pakku)    
                    TL;DR    
                    ```sh
                    git clone https://aur.archlinux.org/pakku.git
                    cd pakku
                    makepkg -si
                    ```
                        + [Bash completion step fails during compile](https://github.com/kitsunyan/pakku/issues/48)
                            + [fixed bash.patch](https://github.com/kitsunyan/pakku/pull/49)

                + [The 5 Best Arch Linux AUR Helper Apps To Use](https://www.addictivetips.com/ubuntu-linux-tips/best-arch-linux-aur-helper-apps/)
                    + [Octopi](https://octopiproject.wordpress.com/)    
                    tk;dr    
                    ```sh
                    git clone https://aur.archlinux.org/octopi.git
                    cd octopi
                    makepkg -si
                    ```

            + [ArchLinux Tutorial, Part 1: Basic ArchLinux Installation](https://medium.com/@mudrii/arch-linux-installation-on-hw-with-i3-windows-manager-part-1-5ef9751a0be)
            + [ArchLinux Tutorial, Part 2: X Window System and I3 Installation](https://medium.com/@mudrii/arch-linux-installation-on-hw-with-i3-windows-manager-part-2-x-window-system-and-i3-installation-86735e55a0a0)
            + [ArchLinux Tutorial, Part 3: I3 Configuration and Operation](https://medium.com/@mudrii/archlinux-tutorial-part-3-i3-configuration-and-operation-9cd6dc90e524)
            + [i3 desktop install](https://xakep.ru/2017/03/22/geek-desktop/)
            + [Оконный менеджер i3](https://laurvas.ru/i3/)
                + [Incorporate nm-applet in i3 window manager](https://unix.stackexchange.com/questions/372606/incorporate-nm-applet-in-i3-window-manager)    
                tl;dr    
                ```sh
                exec --no-startup-id nm-applet --sm-disable
                ```
                + [ [SOLVED] I3 nm-applet issue.](https://bbs.archlinux.org/viewtopic.php?id=204413)    
                ```sh
                ...

                xrandr --output LVDS1 --primary

                ...

                exec i3
                ```
            + [How to Install LightDM Display Manager on Arch Linux](https://linoxide.com/linux-how-to/install-lightdm-arch-linux/)
        + ArchLinux network tips
            + [Systemd-networkd](https://wiki.archlinux.org/index.php/Systemd-networkd)    
            tl;dr    
            ```sh
            vim /etc/systemd/network/20-wired.network
            systemctl enable systemd-networkd.service
            sudo systemctl start systemctl
            ```
            + [OpenSSH](https://wiki.archlinux.org/index.php/OpenSSH)
            + [How to install and configure NetworkManager and network-manager-applet on Arch Linux with Gnome3](https://evilshit.wordpress.com/2012/09/15/how-to-make-networkmanager-and-network-manager-applet-work-on-arch-linux-with-gnome3/)    
            tl;dr    
            ```sh
            lspci | grep -i net
            lsusb
            ip link
            sudo pacman -S wpa_supplicant
            sudo pacman -S wireless_tools
            sudo pacman -S networkmanager
            sudo pacman -S network-manager-applet
            sudo pacman -S gnome-keyring
            sudo systemctl enable NetworkManager.service
            sudo systemctl enable wpa_supplicant.service
            sudo systemctl start wpa_supplicant.service
            sudo systemctl start NetworkManager.service
            ```
        + Arch migration
            + [Migrate installation to new hardware](https://wiki.archlinux.org/index.php/Migrate_installation_to_new_hardware)
            + [Disk cloning](https://wiki.archlinux.org/index.php/Disk_cloning)
            + [System Tar Restore - Feature-rich Backup Script for Linux](https://linoxide.com/linux-how-to/system-tar-restore-bash-script-linux-backup/)
            + [xlockmore can't find fonts to display messages](https://bbs.archlinux.org/viewtopic.php?id=234854)
        + Arch Linux survival tips
            + [USB flash installation media](https://wiki.archlinux.org/index.php/USB_flash_installation_media)    
                    tl;dr
                    ```sh
                    dd bs=4M if=path/to/archlinux.iso of=/dev/sdx status=progress oflag=sync
                    ```
            + surviving after systemd-boot crash
                + [systemd-boot](https://wiki.archlinux.org/index.php/systemd-boot)
                + [Installing Arch Linux : systemd-boot (reinstall)](http://www.adonespitogo.com/articles/arch-linux-EFI-installation/page-2.html)    
                tl;dr
                ```sh
                boot from flash
                mkfs.fat -F32 /dev/sda1 # where EFI is to be reinstalled
                mount /dev/sda2 /mnt
                mount /dev/sda1 /mnt/boot
                #mount /dev/sdb1 /mnt/home
                arch-chroot /mnt /bin/bash
                bootctl install
                vim /boot/loader/entries/arch.conf:

                title Arch Linux
                linux /vmlinuz-linux
                initrd  /initramfs-linux.img
                options root=/dev/sda2 rw
                vim /etc/fstab # for changed UUID of /dev/sda1
                ```
            + GRUB tips
                + while booting type `e` (stands for edit)
                + add `systemd.unit = resque.target` in `linux` boot menu
                + set correct time to avoid https certificate problemshttps://habr.com/ru/company/yandex/blog/438864/
                ```sh
                ntpdate ntp3.stratum2.ru
                ```
        + [Arch Linux Installation guide](https://wiki.archlinux.org/index.php/installation_guide)
            + [Installing Arch Linux on a USB key](https://wiki.archlinux.org/index.php/Installing_Arch_Linux_on_a_USB_key)
        + [Arch Linux Set timezone](https://wiki.archlinux.org/index.php?title=Time&redirect=no#Time_zone)
            ```sh
            timedatectl status
            timedatectl list-timezones
            timedatectl set-timezone Zone/SubZone
            ```
        + [Arch Linux SSH keys](https://wiki.archlinux.org/index.php/SSH_keys)
        + [Arch Linux AUR](https://wiki.archlinux.org/index.php/Arch_User_Repository)
        + [How to install Yaourt on Arch Linux](http://www.ostechnix.com/install-yaourt-arch-linux/)
        + [Ignore A Package From Being Upgraded In Arch Linux](https://www.ostechnix.com/safely-ignore-package-upgraded-arch-linux/)    
        tl;dr
        ```sh
         Pacman won't upgrade packages listed in IgnorePkg and members of IgnoreGroup
         #IgnorePkg   =
         IgnorePkg   = linux linux-headers linux-firmware linux-lts gcc gcc-libs gcc-fortran nvidia cuda virtualbox-host-modules-arch
         IgnoreGroup =
        ```
        tl;dr downgrade to gcc-6.3.1 from gcc-7.1.1
        ```sh
        sudo vim /etc/pacman.conf
        pacman -U /var/cache/pacman/pkg/gcc-6.3.1-2-x86_64.pkg.tar.xz /var/cache/pacman/pkg/gcc-libs-6.3.1-2-x86_64.pkg.tar.xz /var/cache/pacman/pkg/gcc-fortran-6.3.1-2-x86_64.pkg.tar.xz
        ```
        ```sh
        pacman -S grub
        pacman -S vim gvim
        pacman -S os-prober
        pacman -S bash-completion
        pacman -S gnome build-base base-devel scons python-pip python2-pip python-yaml qt5 wayland gdm python2 python mc gdb cgdb
        pacman -S chromium 
        pacman -S konsole
        pacman -S git
        pacman -S extra/keychain
        pacman -S openssh
        pacman -S gconf
        pacman -S hunspell-en
        pacman -S rsync
        pacman -S extra/emacs
        pacman -S texlive
        pacman -S texlive-bin
        pacman -S texlive-core
        pacman -S extra/texlive-fontsextra
        pacman -S texlive-most
        pacman -S texlive-lang
        pacman -S pandoc
        pacman -S qt extra/qt5-declarative
        pacman -S community/netactview
        pacman -S community/cairo-dock
        pacman -S community/cairo-dock-plug-ins
        pacman -S extra/clang
        pacman -S extra/kdegraphics-okular
        pacman -S the_silver_searcher

        systemctl enable gdm
        systemctl start gdm
        systemctl enable wicd
        systemctl start wicd

        sudo pip install gdbgui --upgrade
        ```

        + [Screen capture](https://wiki.archlinux.org/index.php/Screen_capture)
        tl;dr    
        ```sh
        pacman -S imagemagick
        ```

        + [Pacman option to assume “yes” to every question?](https://unix.stackexchange.com/questions/52277/pacman-option-to-assume-yes-to-every-question)    
        tl;dr
        ```sh
            yay --noconfirm -S ...
            yes | sudo pacman -S firefox
        ```

        + xfce4
            + [Numlock/Capslock indicator](https://aur.archlinux.org/packages/xfce4-kbdleds-pl)    
            tl;dr
            ```sh
            yay -S aur/xfce4-kbdleds-plugin-git
            ```

            + [xfce nm-applet missing : how to display network manager icon on xfce panel](https://askubuntu.com/questions/517467/how-to-display-network-manager-icon-on-xfce-panel/572117)
            tl;dr tinker with nm-applet -> `dbus-launch nm-applet`

        + [FS#59266 - [lvm2] Dependency failed for File System Check with 2.02.179-1](
https://bugs.archlinux.org/task/59266?string=dependency+failed&project=1&type%5B0%5D=&sev%5B0%5D=&pri%5B0%5D=&due%5B0%5D=&reported%5B0%5D=&cat%5B0%5D=&status%5B0%5D=open&percent%5B0%5D=&opened=&dev=&closed=&duedatefrom=&duedateto=&changedfrom=&changedto=&openedfrom=&openedto=&closedfrom=&closedto=)    
            tl;dr    
            downgrade LVM2 to fix the issue    
            ```sh
            sudo pacman -U /var/cache/pacman/pkg/lvm2-2.02.177-5-x86_64.pkg.tar.xz
            ```
 
        + Printer (Brother DCPT500W)    
            + tl;dr
            ```sh
            sudo systemctl start avahi-daemon.service
            sudo systemctl enable avahi-daemon.service
            sudo gvim /etc/nsswitch.conf
            sudo systemctl start org.cups.cupsd.service
            sudo systemctl enable org.cups.cupsd.service
            sudo pacman -S multilib/lib32-glibc
            nmap -sn 192.168.1.0/24
            avahi-resolve-host-name -a 192.168.1.106
                192.168.1.106	BRW48E2448DA308.local
            lpstat -t
            device for DCPT500W: socket://192.168.1.106
            lpr -P DCPT500W /usr/share/cups/data/testprint
            ```

            + [Multilib](https://wiki.archlinux.org/index.php/multilib)
            + [Problem installing Brother printer DCP-T700W](https://forum.antergos.com/topic/5795/problem-installing-brother-printer-dcp-t700w)
            + [CUPS Network printer adds, but won't print..](https://bbs.archlinux.org/viewtopic.php?id=92011)
            + [Brother T500W Driver Install Tool](http://support.brother.com/g/b/downloadhowto.aspx?c=as_ot&lang=en&prod=dcpt500w_all&os=128&dlid=dlf006893_000&flang=4&type3=625)
            + [Brother printers: how to install them in Ubuntu and Linux Mint](https://sites.google.com/site/easylinuxtipsproject/15)
            + [ [SOLVED] Brother wireless printer can't work](https://bbs.archlinux.org/viewtopic.php?id=104778)
            + [ Cups and "waiting for printer to become available"](https://bbs.archlinux.org/viewtopic.php?id=121944)
            + [CUPS - Waiting for printer to become available. - usb](https://artodeto.bazzline.net/archives/663-CUPS-Waiting-for-printer-to-become-available.-usb.html)
            + [ [SOLVED] Can't print from chrome, but from command line](https://bbs.archlinux.org/viewtopic.php?id=229038)    
                tl;dr
                ```sh
                pacman -S gtk3-print-backends
                ```
            + [List of USB ID's](http://www.linux-usb.org/usb.ids)    
            tl;dr
            ```sh
            04f9  Brother Industries, Ltd
            	0394  DCP-T500W
            ```

        + [gdbgui review](https://tproger.ru/articles/gdbgui-for-browser/)
        + [gdb-дуэль — списки, деревья и хэш таблицы против командной строки](https://habrahabr.ru/post/328180/)
            + [Various tools to improve the gdb experience](https://github.com/vuvova/gdb-tools)
        + [Slack Desktop (Beta) for Linux](https://aur.archlinux.org/packages/slack-desktop/)
        + [The Rust toolchain installer](https://aur.archlinux.org/packages/rustup/)
        + [[SOLVED] Graphics / Nvidia / Opengl not working as expected](https://bbs.archlinux.org/viewtopic.php?id=213895)

        + [One or more PGP signatures could not be verified!](https://bbs.archlinux.org/viewtopic.php?id=191954)
            + `TL;DR` `gpg --recv-key <KEYID>`

        + [Solve Kernel Panic on Arch Linux](https://www.unixmen.com/solve-arch-linux-kernel-panic/)
            + [`Kernel Panic - Failed to execute /init`](https://www.linux.org.ru/forum/desktop/11626721)
            + TL;DR
            ```sh
            boot from flash
            mount /dev/sdb2 /mnt
            arch-chroot /mnt /bin/bash
            pacman -U /var/cache/pacman/pkg/linux-4.8..
            pacman -S base
            grub-mkconfig  -o /boot/grub/grub.cfg
            mkinitcpio -k /boot/vmlinuz-linux -g /boot/initramfs-linux.img
            ```
        + Rescue from `Reboot and Select proper Boot device or insert Boot Media...`
            + tl;dr
            ```sh
            boot from flash
            mount /dev/sda2 /mnt
            mount /dev/sda1 /mnt/boot/EFI # this is very important
            mount /dev/sda3 /mnt/home
            mount -t proc none /mnt/proc
            mount -o bind /dev /mnt/dev
            ln /sys /mnt/sys
            or
            mount -t sysfs sys /mnt/sys
            arch-chroot /mnt /bin/bash
            grub-install
            ```

        + [Arch vs. Manjaro](https://www.slant.co/versus/2690/2706/~arch_vs_manjaro)

        + [mount dev, proc, sys in a chroot environment?](https://superuser.com/questions/165116/mount-dev-proc-sys-in-a-chroot-environment)

    + [Arch Linux vs Nix OS](https://www.slant.co/versus/2690/11676/~arch_vs_nix-os)
        + [Switching to Nixos from Arch Linux](https://ramsdenj.com/2017/06/19/switching-to-nixos-from-arch-linux.html)

    + RHEL
        + [Software Collections for Scientific Linux CERN 6](http://linux.web.cern.ch/linux/scl/)
        + [Software Collections for Scientific Linux CERN 6 : RPMS](http://linuxsoft.cern.ch/cern/scl/slc6X/x86_64/RPMS/)

    + Ubuntu
        + [How to list all installed packages](https://askubuntu.com/questions/17823/how-to-list-all-installed-packages)    
        tl;dr
        ```sh
        apt list --installed
        ```

    + [Awesome list dedicated to Windows Subsystem for Linux](https://github.com/sirredbeard/Awesome-WSL)
        + [Linux’izing your Windows PC into a dev machine  Part 2#Java and JVM ecosystem](https://cepa.io/2018/02/20/linuxizing-your-windows-pc-part2/#java)
        + [Is it possible to access my Android device through WSL?](https://www.reddit.com/r/bashonubuntuonwindows/comments/9qmrqs/is_it_possible_to_access_my_android_device/)
        + [Windows Subsystem for Linux not recognizing JAVA_HOME Environmental Variable](https://stackoverflow.com/questions/53365643/windows-subsystem-for-linux-not-recognizing-java-home-environmental-variable)
        + Arch Linux on Windows 10
            + [Running Arch Linux over Windows 10!](https://www.akitaonrails.com/2018/04/29/running-arch-linux-over-windows-10)
            + [Install Arch Linux on Windows 10 Hyper-V](https://medium.com/@mudrii/install-arch-linux-on-windows-10-hyper-v-215b2e71c6db)
            + [Arch Linux on Windows 10](https://hannuhartikainen.fi/blog/arch-wsl/)
            + [Uptime becomes negative after Windows machine has been on for several days](https://github.com/microsoft/WSL/issues/3514)
            + [Ripgrep and other Rust utilities panic](https://github.com/yuk7/ArchWSL/issues/109)    
                tl;dr workaround    
                ```sh
                pacman -U /var/cache/pacman/pkg/glibc-2.30-3-x86_64.pkg.tar.xz
                ...
                warning: downgrading package glibc (2.31-1 => 2.30-3)
                ```

    + misc
        + [8 Best Linux Console File Managers](https://www.tecmint.com/linux-terminal-file-managers/?fbclid=IwAR1j9PzVEJ2TvP0ze0cLKfeB_bBq9ISECNqsPsPSbVyScJO-po-2jY4Q1i0)
        + [9 Best File Comparison and Difference (Diff) Tools for Linux](https://www.tecmint.com/best-linux-file-diff-tools-comparison/)
            tl;dr `meld, diffuse, vimdiff, kompare`
        + [10 Best Markdown Editors for Linux](https://www.tecmint.com/best-markdown-editors-for-linux/)

+ [OOP cheatsheet](https://tproger.ru/translations/oop-principles-cheatsheet/)
    + tl;dr
        + use with inheritance
            + delegation
            + composition
            + aggregation
        + DRY - don't repeat yourself
        + [How I Declare My class And Why](http://howardhinnant.github.io/classdecl.html)

    + [Inheritance, why is bad?](https://users.rust-lang.org/t/inheritance-why-is-bad/35705)

    + SOLID OOP
        + [S.O.L.I.D: The First 5 Principles of Object Oriented Design](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
            + [Простое объяснение принципов SOLID](https://habr.com/en/company/mailru/blog/412699/)
            + [Как с помощью принципа единственной ответственности писать гибкий и модульный код](https://tproger.ru/translations/solid-srp-explained/?fbclid=IwAR3DdqAxAO55xtU-Rq8VWQDoh_FufzB1pPoXcxc60eWlrOj3ieAHy5IrKKY)
    + SFINAE
        + [SFINAE](https://en.cppreference.com/w/cpp/language/sfinae)
        + [C++ SFINAE examples?](https://stackoverflow.com/questions/982808/c-sfinae-examples)

+ Backup + Restore of the system
    + [Howto: Backup and restore your system!](https://ubuntuforums.org/showthread.php?t=35087)
        + Backup:
        ```
        sudo su
        cd /
        tar cvpjf backup.tar.bz2 --exclude=/proc --exclude=/lost+found --exclude=/backup.tar.bz2 --exclude=/mnt --exclude=/sys /
        ```
        + Restore:
        ```sh
        tar xvpfj backup.tar.bz2 -C /
        mkdir proc
        mkdir lost+found
        mkdir mnt
        mkdir sys
        etc...
        ```
+ [Fstab doesn't mount with exec](http://askubuntu.com/questions/678857/fstab-doesnt-mount-with-exec)

+ Distributed versioning systems
    + git & github & gitlab
        + [Lazygit — псевдографический консольный клиент для Git](https://www.linux.org.ru/news/opensource/15584752)
        + Git remote access
            + [s there a way to skip password typing when using https:// on GitHub?](Is there a way to skip password typing when using https:// on GitHub?)
            + [How to use git with gnome-keyring integration](https://stackoverflow.com/questions/13385690/how-to-use-git-with-gnome-keyring-integration)
                + tl;dr
                ```sh
                $ sudo pacman -S libgnome-keyring
                $ pushd /usr/share/git/credential/gnome-keyring
                $ sudo make
                $ popd
                $ git config --global credential.helper /usr/share/git/credential/gnome-keyring/git-credential-gnome-keyring
                ```
            + [Git на сервере - Создание открытого SSH-ключа](https://git-scm.com/book/ru/v1/Git-%D0%BD%D0%B0-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B5-%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BE%D1%82%D0%BA%D1%80%D1%8B%D1%82%D0%BE%D0%B3%D0%BE-SSH-%D0%BA%D0%BB%D1%8E%D1%87%D0%B0)
            + [Как настроить подключение к удаленному Git репозиторию](https://ru.stackoverflow.com/questions/468812/%D0%9A%D0%B0%D0%BA-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B8%D1%82%D1%8C-%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA-%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%BD%D0%BE%D0%BC%D1%83-git-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D1%8E)
        + [Git и Github. Простые рецепты](http://habrahabr.ru/post/273897/)
        + [Моя шпаргалка по работе с Git](http://eax.me/git-commands/)
        + Mary Rose Cook on git
            + [Mary Rose Cook blog](http://maryrosecook.com/)
            + [github for maryrosecook.com](https://github.com/maryrosecook/maryrosecook.com)
        + [Revert Git repo to a previous commit](http://stackoverflow.com/questions/4114095/revert-git-repo-to-a-previous-commit)
        + [git returns http error 407 from proxy after CONNECT](http://stackoverflow.com/questions/24907140/git-returns-http-error-407-from-proxy-after-connect)
        + [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
        + [Git delete a remote/local branch or tag](https://matoski.com/article/git-delete-remote-branch-tag/)

        + [How to change your commit messages in Git?](https://gist.github.com/nepsilon/156387acf9e1e72d48fa35c4fabef0b4)

        + [How to: Delete a remote Git tag](https://nathanhoad.net/how-to-delete-a-remote-git-tag)
            + delete tag
          ```sh
          git tag -d v0.2.3
          git push origin :refs/tags/v0.2.3
          ```

            + pushing new tags to remote
          ```sh
          git push --tags
          ```

        + [19 советов по повседневной работе с Git](http://habrahabr.ru/company/mailru/blog/267595/)
        + [Достаточно Git-а, чтобы быть (менее) опасным](http://habrahabr.ru/post/268951/)
        + [git checkout tag, git pull fails in branch](http://stackoverflow.com/questions/10147475/git-checkout-tag-git-pull-fails-in-branch)
          ```sh
          git push -u origin master
          git pull origin master
          git pull
          git branch --set-upstream-to=origin/master master
          git pull
          git branch -u origin/master
          git branch --set-upstream-to=origin/master master
          git branch -u origin/master
          ```
        + [Reset Demystified](https://git-scm.com/blog/2011/07/11/reset.html)
        + [A Git Horror Story: Repository Integrity With Signed Commits](https://mikegerwitz.com/papers/git-horror-story)

        + [constructive git critique](http://komar.bitcheese.net/en/git-sucks-or-why-do-I-use-darcs-instead)
        + [another point of view on darcs vs. git](http://blog.moertel.com/posts/2007-12-10-how-i-stopped-missing-darcs-and-started-loving-git.html)

        + [Как оформлять коммиты, чтобы потом не было больно](https://habrahabr.ru/company/Voximplant/blog/276695/)

        + [Git: Squash your latests commits into one](https://www.devroom.io/2011/07/05/git-squash-your-latests-commits-into-one/)
            + [How to Squash Multiple Commits Into One with Git](https://forum.freecodecamp.com/t/how-to-squash-multiple-commits-into-one-with-git/13231)
            + [Squash my last X commits together using Git](https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git)

        + [git rebase vs. merge](https://tyvik.ru/blog/49)

        + git rebase memo
        ```sh
        git rebase origin/master
        git status
        <fix conflicts>
        git add <changed>
        git rebase --continue
        git push origin my-branch --force
        <repeat>
        ```
        + aborting & syncing with origin/master
            ```sh
            git rebase --abort
            git merge --abort
            git checkout -B master origin/master
            ...
            git push origin master:master
            ...
            ```

        + [How to import existing Git repository into another?](http://stackoverflow.com/questions/1683531/how-to-import-existing-git-repository-into-another)
        ```sh
        git subtree add -P u-boot /scratch/tegra-sources/u-boot_nvidia_distribution/u-boot master
        ```

        + subtree import of the subfolder
            + [Add subdirectory of remote repo with git-subtree](http://stackoverflow.com/questions/23937436/add-subdirectory-of-remote-repo-with-git-subtree)    
            tl;dr
            ```sh
            git subtree split -P modules/my_module -b temporary-split-branch
            git subtree add -P prefix-name/  /path-to-repo temporary-split-branch
            ```

        + [Git - Find when a method is removed](http://stackoverflow.com/questions/21110272/git-find-when-a-method-is-removed)    
            tl;dr
            ```sh
            git log -c -S'methodName' /path/to/file.cpp
            ```

        + [Support .ssh/config for specifying keys if ssh-agent fails](https://github.com/rust-lang/cargo/issues/2078)

        + [Adding an existing project to GitHub using the command line](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/)

        + [Малоизвестные Git-команды](https://habrahabr.ru/company/mailru/blog/318508/)

        + [two-factor authentication in your Github account leads to inability to push via HTTPS](https://stackoverflow.com/questions/17659206/git-push-results-in-authentication-failed)    
        tl;dr  
        ```sh
        git remote -v
        git remote remove origin
        git remote add origin git@github.com:user/repo.git
        git push --set-upstream origin master
        ```

        + [git - remote add origin vs remote set-url origin](https://stackoverflow.com/questions/42830557/git-remote-add-origin-vs-remote-set-url-origin/42830632)    
        tl;dr    
        below is used to a add a new remote:
        ```sh
        git remote add origin git@github.com:User/UserRepo.git
        ```
        below is used to change the url of an existing remote repository:    
        ```sh
        git remote set-url origin git@github.com:User/UserRepo.git
        ```
        below will push your code to the master branch of the remote repository defined with origin and -u let you point your current local branch to the remote master branch:    
        ```sh
        git push -u origin master
        ```

        + [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

    + gitlab
        + [Gitlab : Managing Issues](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html)
        + [GitLab Quick Actions](https://docs.gitlab.com/ee/user/project/quick_actions.html)

    + [Pijul - distributed version control system written in Rust](https://pijul.org/manual/)

+ **gcc** unsorted question (TODO reorganize)
    + list gcc's pre-defined macros    
        ```sh
        gcc -x c /dev/null -dM -E
        ```
    + [Why doesn't GCC optimize a*a*a*a*a*a to (a*a*a)*(a*a*a)?](http://stackoverflow.com/questions/6430448/why-doesnt-gcc-optimize-aaaaaa-to-aaaaaa)

+ Terminal emulators
    + [A look at terminal emulators, part 1](https://anarc.at/blog/2018-04-12-terminal-emulators-1/)
    + [A look at terminal emulators, part 2](https://anarc.at/blog/2018-05-04-terminal-emulators-2/)
    + [20 Useful Terminal Emulators for Linux](https://www.tecmint.com/linux-terminal-emulators/)
    + [A tiling terminal emulator for Linux using GTK+ 3](https://github.com/gnunn1/tilix)
        + [Tilix is an advanced GTK3 tiling terminal emulator that follows the Gnome Human Interface Guidelines.](https://gnunn1.github.io/tilix-web/)    
        ```sh
        Source vte.sh in bashrc

        Update ~/.bashrc (or ~/.zshrc if you are using zsh) to execute vte.sh directly, this involves adding the following line at the end of the file.

        if [ $TILIX_ID ] || [ $VTE_VERSION ]; then
            source /etc/profile.d/vte.sh
        fi
        ```

+ Editors

    + [What are the best programming text editors?](http://www.slant.co/topics/12/~programming-text-editors)

    + [How to Select Columns in Editors (Kate, Vim, etc.)](http://stackoverflow.com/questions/1802616/how-to-select-columns-in-editors-notepad-kate-vim-sublime-textpad-etc-an)

    + modern ctags
        + [A maintained ctags implementation](https://github.com/universal-ctags/ctags)
        + [Universal-ctags Hacking Guide](http://docs.ctags.io/en/latest/)
            + [C++ Declarations/References?](https://github.com/universal-ctags/ctags/issues/651)
        + [Hong's Technology Blog for ctags for C++](https://www.topbug.net/blog/2012/03/17/generate-ctags-files-for-c-slash-c-plus-plus-source-files-and-all-of-their-included-header-files/)
        ```sh
        ctags -R --c++-kinds=+p --fields=+iaS --extra=+q .
        ```

    + vim tips
        :set ff=unix
        + [Vim: Squeezing the Text Editor’s Juice with More Features](http://www.datastuff.tech/programming/vim-squeezing-text-editors-juice-with-more-features/)
        + [How I revamped my Vim setup](https://alex.dzyoba.com/blog/vim-revamp)
        + [Minimalist Vim Plugin Manager](https://github.com/junegunn/vim-plug)
        + [A guide to setting up Vim for JavaScript development](https://freshman.tech/vim-javascript/)
        + [You Should Be Using Tags In Vim](https://vimways.org/2018/you-should-be-using-tags-in-vim)
        + [Browsing programs with tags](https://vim.fandom.com/wiki/Browsing_programs_with_tags)
        + [Understanding Vim’s Jump List](https://medium.com/breathe-publication/understanding-vims-jump-list-7e1bfc72cdf0)
        + [Что вам стоит знать, если вы начали изучение Vim](https://proglib.io/p/vim-what-i-wish-i-knew/)
        + [Configure coc.nvim for C/C++ Development](https://ianding.io/2019/07/29/configure-coc-nvim-for-c-c++-development/)
            + [CCLS (C/C++) extension for coc.nvim](https://github.com/Maxattax97/coc-ccls)
                + [Is this extension in a usable state?](https://github.com/Maxattax97/coc-ccls/issues/1)    
        ```sh
        pacman -S nodejs yarn
        yay -S ccls
        ```
        + [A guide to modern Web Development with (Neo)vim](https://www.freecodecamp.org/news/a-guide-to-modern-web-development-with-neo-vim-333f7efbf8e2/)
        + [Vim’s absolute, relative and hybrid line numbers](https://jeffkreeftmeijer.com/vim-number/)
            + [How to turn off Vim relativenumber setting?](https://stackoverflow.com/questions/32306604/how-to-turn-off-vim-relativenumber-setting)
        + [Об удобной навигации и отладке C++ кода в Vim](https://habr.com/en/post/245681/)
        + [Vim - open new tab in buffer](https://stackoverflow.com/questions/26073226/vim-open-new-tab-in-buffer)
          + tl;dr
          ```sh
          :Te
          ```
        + [From Vim to Emacs+Evil chaotic migration guide](http://juanjoalvarez.net/es/)
        + [The Modern Vim Config with Pathogen](http://tammersaleh.com/posts/the-modern-vim-config-with-pathogen/)
            + [vim-pathogen](https://github.com/tpope/vim-pathogen)
        + [How to setup vim to edit both Makefile and normal code files?](http://superuser.com/questions/632657/how-to-setup-vim-to-edit-both-makefile-and-normal-code-files)
        + vim+scala
            + [Editing Scala with vim](https://leonard.io/blog/2013/04/editing-scala-with-vim/)
            + [My Vim setup for Scala](http://bleibinha.us/blog/2013/08/my-vim-setup-for-scala)
                + [vim, scala and ctags](http://andrew.stwrt.ca/posts/vim-ctags/)
            + [integration of Scala into Vim](https://github.com/derekwyatt/vim-scala)
                + [coding-scala-with-vim](http://derekwyatt.org/2013/12/31/coding-scala-with-vim.html)
        + [VIM and Python -- a Match Made in Heaven](https://realpython.com/blog/python/vim-and-python-a-match-made-in-heaven/)
        + [vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors)
        + [Provide easy code formatting in Vim by integrating existing code formatters](https://github.com/Chiel92/vim-autoformat)
        + [Vundle vs. Pathogen](http://lepture.com/en/2012/vundle-vs-pathogen)
        + [Разработка → VIM: зачем, если есть IDE, и как?](https://habrahabr.ru/post/303554/)
        + [Vim vs. Neovim](https://www.slant.co/versus/42/62/~vim_vs_neovim)
        + [Install Vim 8.0 on on Ubuntu 16.04, Debian, Fedora, CentOS](http://www.ubuntumaniac.com/2016/09/install-vim-80-on-on-ubuntu-1604-debian.html)
        + [Find in files within Vim](http://vim.wikia.com/wiki/Find_in_files_within_Vim)
        + [Vim: Substitute pattern between braces](https://vi.stackexchange.com/questions/2751/substitute-pattern-between-braces)    
            tl;dr
            ```sh
            viB:s/word/replacement/gc
            ```
            or
            ```sh
            vi{:s...
        + [The Ultimate Vim Distribution](http://vim.spf13.com/)
        + [Ultimate auto-completion system for Vim](https://github.com/Shougo/neocomplcache.vim)
        ```sh
        Plugin 'Shougo/neocomplcache'
        Plugin 'Shougo/neosnippet'
        Plugin 'Shougo/neosnippet-snippets'
        Open up Vim and start installation with :PluginInstall
        ```
        + YouComplete    
            tl;dr
            ```sh
            ~/.vim/bundle/YouCompleteMe$ ./install.sh --clang-completer --racer-completer
            ```
            + [libtinfo.so.* missing in Arch Linux](https://github.com/Valloric/YouCompleteMe/issues/778)
            + [supercede: Package Details: ncurses5-compat-libs 6.1-1 ](https://aur.archlinux.org/packages/ncurses5-compat-libs/?comments=all)    
            tl;dr  
            ```sh
            gpg --keyserver keys.gnupg.net --recv-keys 702353E0F7E48EDB
            yay -S ncurses5-compat-libs
            ```
            + ["ycmd server SHUTDOWN" error on Arch Linux](https://github.com/Valloric/YouCompleteMe/issues/2579#issuecomment-288315182)
                + tl;dr
                ```sh
                yay -S libtinfo
                yay -S libtinfo5
                :YcmGenerateConfig
                :YcmRestartServer
                ```
            + [Ubuntu : fatal error: pyconfig.h: No such file or directory # include <pyconfig.h>](https://github.com/Valloric/YouCompleteMe/issues/2219)
              + tl;dr
              ```sh
              sudo apt install python3-dev
              python3 install.py --clang-completer --racer-completer
              ```

        + [TabNine uses deep learning to help you write code faster.](https://tabnine.com/)
        + CoC - **C**onquer **o**f **C**ompletion
            + [Install coc.nvim](https://github.com/neoclide/coc.nvim/wiki/Install-coc.nvim)
                + Ubuntu install issues
                    + [Ubuntu 17 apt-get installs cmdtest instead of yarn](https://github.com/yarnpkg/yarn/issues/3189)
                    + [How to Install Yarn on Ubuntu 18.04](https://linuxize.com/post/how-to-install-yarn-on-ubuntu-18-04/)    
                    tl;dr    
                    ```sh
                    sudo apt install npm
                    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
                    echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
                    sudo apt update
                    sudo apt install yarn
                    yarn --version
                    1.17.3
                    ```
                + Fast check after install    
                tl;dr    
                ```
                :CocInfo
                :CocList diagnostics
                :CocInstall coc-json
                :CocInstall coc-rls
                :CocConfig
                :CocCommand
                ```    
                tl;dr look into `~/.config/coc`    
                `rustup component add rls rust-analysis rust-src`
            + [Intellisense engine for vim8 & neovim, full language server protocol support as VSCode](https://github.com/neoclide/coc.nvim)
                + [coc.nvim : read it first](https://www.npmjs.com/package/coc.nvim)
                    + [Floating windows](https://github.com/neoclide/coc.nvim/wiki/F.A.Q#how-to-make-preview-window-shown-aside-with-pum)
            + [CoC Language servers : C++](https://github.com/neoclide/coc.nvim/wiki/Language-servers#ccobjective-c)
                + [C/C++/ObjC language server supporting cross references, hierarchies, completion and semantic highlighting](https://github.com/MaskRay/ccls)
                    + [ccls : Build](https://github.com/MaskRay/ccls/wiki/Build#system-specific-notes)
                + [Rust support for coc.nvim](https://github.com/neoclide/coc-rls/)
                + [Guide To Turn Neovim Into A Rust IDE?](https://www.reddit.com/r/rust/comments/adepau/guide_to_turn_neovim_into_a_rust_ide/)
                    + [useful init for nvim](https://github.com/realcr/my_init_vim/blob/master/init.vim)
                    + [Why You Should Still Use Neovim](https://codekoalas.com/blog/why-you-should-still-use-neovim)
                        + [ [RFC] Built-in LSP Support](https://github.com/neovim/neovim/pull/10222)

                    + [~~Amp: "a complete text editor for your terminal"~~](https://www.reddit.com/r/rust/comments/7t6rsq/amp_a_complete_text_editor_for_your_terminal/)

        + [Demystifying multi file searches in `vim` and the command line](https://seesparkbox.com/foundry/demystifying_multi_file_searches_in_vim_and_the_command_line)
        + [Use VIM as your RUST IDE](https://github.com/ivanceras/rust-vim-setup)
        + [How to install NERDTree with Vundle?](https://vi.stackexchange.com/questions/5335/how-to-install-nerdtree-with-vundle)

        + NeoVim specific
            + [Neovim ArchLinux notes](https://wiki.archlinux.org/index.php/Neovim)    
            *tl;dr*
            ```sh
            mkdir -p ~/.config/nvim/
            ln -s ~/.vimrc ~/.config/nvim/init.vim
            ```
            + [rxrc/nvimrc](https://libraries.io/github/rxrc/nvimrc)
                + [from nvimrc](https://devhub.io/repos/makenew-nvimrc)
            + [NeoVim config files](https://github.com/bigeagle/neovim-config)
            + [GTK ui for neovim written in rust using gtk-rs bindings](https://github.com/daa84/neovim-gtk)

    + Emacs
        + [Хорошо настроенный Emacs](http://habrahabr.ru/post/274759/)
        + [Prelude is an enhanced Emacs 24 or 25 distribution that should make your experience with Emacs both more pleasant and more powerful](https://github.com/bbatsov/prelude)

    + kate-config
        + [Kate configuration for Rust](https://github.com/rust-lang/kate-config)

    + [Textadept (Editor)](https://www.openhub.net/p/textadept)
        + [Textadept module for ctags](http://foicica.com/wiki/ctags)
        + [Git mirror of Mitchell's Textadept editor](https://github.com/rgieseke/textadept)

    + [Atom - The hackable text editor](https://atom.io)
        + [atom github](https://github.com/atom/atom)
        + [Atom Flight Manual](https://atom.io/docs/latest/getting-started-atom-basics)
        + [Atom Keymaps In-Depth](http://flight-manual.atom.io/behind-atom/sections/keymaps-in-depth/)
            + [Atom How to replace a keymap binding](https://discuss.atom.io/t/how-to-replace-a-keymap-binding/16834/6)
        + [Atom Editor Keyboard Shortcut Cheat Sheet](https://blog.bugsnag.com/atom-editor-cheat-sheet/)
            + *Line Manipulation*
                1. ⌘ + ] / [ Indent/outdent current line.
                2. ⌘ + enter. Insert new line after current line.
                3. ⌘ + shift + enter. Insert new line before current line.
                4. ctrl + shift + k. Delete current line.
                5. ctrl + ⌘ + up/down. Move current line up/down.
                6. shift + ⌘ + d. Duplicate current line.
                7. ⌘ + j. Join current and next lines.
            + [Auto indent code in Atom editor](http://stackoverflow.com/questions/22611377/auto-indent-code-in-atom-editor)
                + *TL;DR*
                    Package auto-indent exists to apply auto-indent to entire file with this shortcuts :
                    `ctrl+shift+i`
                    Package url : [auto-indent](atom.io/packages/auto-indent)


        + [The Atom text editor and Rust](http://www.perfectchipperman.com/2015/10/the-atom-text-editor-and-rust.html)
            + [Software development and other things](http://markusjais.com/)
            + [atom Force file reload](https://discuss.atom.io/t/force-file-reload/11508)
            + [atom/markdown-preview](https://github.com/atom/markdown-preview/pull/298)
            + [atom/multi-cursor-plus](https://atom.io/packages/multi-cursor-plus)
            + [atom/Sublime Style Column Selection](https://atom.io/packages/Sublime-Style-Column-Selection)
                + *TL;DR*
                ```
                Platform    Modifier Key    Mouse Button
                Linux       Shift           Left
                ```

            + [[Solved] disable alt+mouse "move window"?](https://forum.xfce.org/viewtopic.php?id=2989)
              + [How can I disable 'Alt' + mouse default behavior in KDE?](http://superuser.com/questions/584730/how-can-i-disable-alt-mouse-default-behavior-in-kde)
              + [use 'Shift-MiddleMouse' for column selection](https://github.com/bigfive/atom-sublime-select/issues/26)
              + [Automatically use hard tabs for Makefile buffers #3](https://github.com/atom/language-make/issues/3)
              + [Atom - The Arch Linux Development Package](https://atom.io/packages/language-archlinux)
        + performance issues
            + [atom performance issues](https://github.com/atom/atom/labels/performance)
                + [Atom hangs on large directories/files and when window switching #9325](https://github.com/atom/atom/issues/9325)
                + [ Render lines via tiles #6733 ](https://github.com/atom/atom/pull/6733#issuecomment-108407945)
                + [Find remaining performance bottlenecks for large files #6692](https://github.com/atom/atom/issues/6692)

    + [CppCon 2017: Rong Lu "C++ Development with Visual Studio Code"](https://www.youtube.com/watch?v=rFdJ68WbkdQ)

    + [Slap is a sublime-like text editor which works inside the terminal.](https://www.slant.co/options/53/~slap-review)
        + [Slap - sublime-like terminal-based text editor](https://github.com/slap-editor/slap)

    + [Xi-editor - a modern editor with a backend written in Rust.](https://github.com/google/xi-editor)
        + [GTK frontend for the Xi text editor, written in Rust](https://gitlab.gnome.org/World/Tau)    
        tl;dr    
        `yay -S tau-editor-git`    
        ```sh
        sudo pacman -S flatpak
        ...
        flatpak install flathub org.gnome.Tau
            Required runtime for org.gnome.Tau/x86_64/stable (runtime/org.freedesktop.Platform/x86_64/19.08) found in remote flathub
            Do you want to install it? [Y/n]: 
            
            org.gnome.Tau permissions:
                ipc wayland x11
            
            
            
                    ID                                                       Branch               Remote                Download
             1. [✓] org.freedesktop.Platform                                 19.08                flathub               223.6 MB / 237.7 MB
             2. [✓] org.freedesktop.Platform.GL.default                      19.08                flathub                90.8 MB / 90.8 MB
             3. [✓] org.freedesktop.Platform.GL.nvidia-435-21                1.4                  flathub               103.3 MB / 103.3 MB
             4. [✓] org.freedesktop.Platform.Locale                          19.08                flathub               163.7 MB / 318.9 MB
             5. [✓] org.freedesktop.Platform.openh264                        19.08                flathub               594.2 kB / 593.4 kB
             6. [✓] org.gnome.Tau                                            stable               flathub                 4.6 MB / 4.6 MB
             7. [✓] org.gnome.Tau.Locale                                     stable               flathub                45.3 kB / 41.0 kB
            
                    Installation complete.
        
        flatpak run org.gnome.Tau
        
            Note that the directories 
            
            '/var/lib/flatpak/exports/share'
            '$HOME/.local/share/flatpak/exports/share'
            
            are not in the search path set by the XDG_DATA_DIRS environment variable, so
            applications installed by Flatpak may not appear on your desktop until the
            session is restarted.
            
            Gtk-Message: 23:05:39.139: Failed to load module "canberra-gtk-module"
            Gtk-Message: 23:05:39.140: Failed to load module "canberra-gtk-module"
        ```

    + [Monaco Editor](https://microsoft.github.io/monaco-editor/)
        + [Monaco Editor repo](https://github.com/Microsoft/monaco-editor)

    + [Collection of miscellaneous portable C snippets.](https://github.com/nemequ/portable-snippets)
        + [Debug trap portable](https://github.com/nemequ/portable-snippets/blob/master/debug-trap/debug-trap.h)
            + [Is there a portable equivalent to DebugBreak()/__debugbreak?](https://stackoverflow.com/questions/173618/is-there-a-portable-equivalent-to-debugbreak-debugbreak)

    + [juCi++: a lightweight, platform independent C++-IDE with support for C++11, C++14 and C++17 features depending on libclang version.](https://gitlab.com/cppit/jucipp)
    + [ C++ Ecosystem: Compilers, IDEs, Tools, Testing and More ](https://www.bfilipek.com/2019/10/cppecosystem.html?m=1)    
        + [and meson, missed from the above review](https://mesonbuild.com/)
            + [The Meson Build System](https://github.com/mesonbuild/meson)
            + [List of projects using Meson](https://mesonbuild.com/Users.html)
                + [HelenOS is a portable microkernel-based multiserver operating system designed and implemented from scratch](http://www.helenos.org/)
    + [Thoughts about Software Development with an eye on the world of modern C++ Programming](https://thoughts-on-cpp.com/)
        + [My God, It’s Full Of Stars: The N-Body-Problem Series](https://thoughts-on-cpp.com/2019/02/08/the-n-body-problem-series/)
        + [My God, It’s Full Of Stars: And then there was CMake](https://thoughts-on-cpp.com/2019/02/14/and-then-there-was-cmake/)
        + [My God, It’s Full Of Stars: Testing Point Mass Attraction with Catch2](https://thoughts-on-cpp.com/2019/02/28/testing-point-mass-attraction-with-catch2/)
        + [My God, It’s Full of Stars: Implementing the implicit Euler-Method with STL](https://thoughts-on-cpp.com/2019/03/07/implementing-the-implicit-euler-method-with-stl/)
        + [Introduction into Logging with Loguru](https://thoughts-on-cpp.com/2019/03/12/introduction-into-logging-with-loguru/)
        + [Using Pointer to Members on STL Algorithms](https://thoughts-on-cpp.com/2019/02/22/cpp-using-pointer-to-members/)
        + [Introduction into Logging with Loguru](https://thoughts-on-cpp.com/2019/03/27/introduction-into-build-automation-setup-with-jenkins-and-cmake/)
        + [Introduction into C++ Builds with Gradle](https://thoughts-on-cpp.com/2019/04/10/introduction-into-c-builds-with-gradle/)
        + [A short Introduction into IEEE 754 Floating-Point Model](https://thoughts-on-cpp.com/2019/04/03/a-short-introduction-into-ieee-754-floating-point-model/)
        + [Numerical Methods with C++ Part 1: Newton-Cotes Integration](https://thoughts-on-cpp.com/2019/04/17/numerical-methods-in-c-part-1-newton-cotes-integration/)
        + [Numerical Methods with C++ Part 2: Gauss-Legendre Integration](https://thoughts-on-cpp.com/2019/04/25/numerical-methods-in-c-part-2-gauss-legendre-integration/)
        + [Numerical Methods with C++ Part 3: Root Approximation Algorithms](https://thoughts-on-cpp.com/2019/06/06/numerical-methods-with-cpp-part-3-root-approximation-algorithms/)
        + [Numerical Methods with C++ Part 4: Introduction Into Decomposition Methods of Linear Equation Systems](https://thoughts-on-cpp.com/2019/06/12/numerical-methods-with-c-part-4-introduction-into-decomposition-methods-of-linear-equation-systems/)

    + [Is C++ fast?](https://zeux.io/2019/01/17/is-c-fast/)
        + [Flavors of SIMD](https://zeux.io/2019/02/17/flavors-of-simd/)

+ [Technical typesetting](https://github.com/alsam/bookmarks/blob/master/technical_typesetting.md)

+ [ZeroMQ \zero-em-queue\, \ØMQ\:](http://zeromq.org/)
    + [source git](http://zeromq.org/docs:source-git)
    + [ØMQ Language Bindings](http://zeromq.org/bindings:_start)
    + [Scala binding for ZeroMQ http://www.zeromq.org/bindings:scala-binding](https://github.com/valotrading/zeromq-scala-binding)

+ MIT online courses
    + [physics](http://ocw.mit.edu/courses/physics/)
    + [special courses](http://ocw.mit.edu/courses/special-programs/)

+ Linux distros specific
    + [How to Keep ‘sudo’ Password Timeout Session Longer in Linux](http://www.tecmint.com/set-sudo-password-timeout-session-longer-linux/)
    + `systemd` vs. `init`
        + [RHEL7: How to get started with Systemd](https://www.certdepot.net/rhel7-get-started-systemd/)
        + [The Story Behind ‘init’ and ‘systemd’: Why ‘init’ Needed to be Replaced with ‘systemd’ in Linux](http://www.tecmint.com/systemd-replaces-init-in-linux/)
        + [ELI5: The SystemD vs. init/upstart controversy](https://www.reddit.com/r/linux/comments/132gle/eli5_the_systemd_vs_initupstart_controversy/)
        + [Systemd Essentials: Working with Services, Units, and the Journal](https://www.digitalocean.com/community/tutorials/systemd-essentials-working-with-services-units-and-the-journal)
        + [Comparison of init systems](https://wiki.gentoo.org/wiki/Comparison_of_init_systems)
        + [gentoo - systemd](https://wiki.gentoo.org/wiki/Systemd)
        + [How does systemd use /etc/init.d scripts?](http://unix.stackexchange.com/questions/233468/how-does-systemd-use-etc-init-d-scripts)
        + [`systemds for `upstart` users](https://wiki.ubuntu.com/SystemdForUpstartUsers)
        + `journald`
            + [Logging message workflow with journald](http://www.gabriel.urdhr.fr/2015/04/29/journald-workflow/)
            + [systemd for Developers III : Logging to the Journal](http://0pointer.de/blog/projects/journal-submit.html)    
            tl;dr
            ```c
            #include <systemd/sd-journal.h>
            #include <unistd.h>
            #include <stdlib.h>
             
            int main(int argc, char *argv[]) {
                    sd_journal_send("MESSAGE=Hello World!",
                                    "MESSAGE_ID=52fb62f99e2c49d89cfbf9d6de5e3555",
                                    "PRIORITY=5",
                                    "HOME=%s", getenv("HOME"),
                                    "TERM=%s", getenv("TERM"),
                                    "PAGE_SIZE=%li", sysconf(_SC_PAGESIZE),
                                    "N_CPUS=%li", sysconf(_SC_NPROCESSORS_ONLN),
                                    NULL);
                    return 0;
            }
            ```
            ```sh
            journalctl -o json-pretty MESSAGE="Hello World!"
            ```
            ```sh
            printf "hola\n\rbro\n\r" | systemd-cat -t HOLA-BRO-SLASH-R
            journalctl --sync
            journalctl -b -t HOLA-BRO-SLASH-R --no-pager --no-hostname
            ```
            + [How to configure systemd journal-remote?](https://serverfault.com/questions/758244/how-to-configure-systemd-journal-remote)
            + [LOGGING DONE RIGHT systemd-journal-upload & systemd-journal-remote setup](https://www.youtube.com/watch?v=45CQ0tgXQmY)
            + [log4cplus](https://github.com/wilx/log4cplus)
            + polltest
            ```c
            #include <stdio.h>
            #include <stdlib.h>
            #include <string.h>
            #include <systemd/sd-journal.h>
            
            int main(int argc, char *argv[]) {
                    int r;
                    sd_journal *j;
                    r = sd_journal_open(&j, SD_JOURNAL_LOCAL_ONLY);
                    if (r < 0) {
                            fprintf(stderr, "Failed to open journal: %s\n", strerror(-r));
                            return 1;
                    }
            
                    /* Opening the fd now means the first sd_journal_wait() will actually wait */
                    r = sd_journal_get_fd(j);
                    if (r < 0) {
                            fprintf(stderr, "Failed to get fd: %s\n", strerror(-r));
                            return 1;
                    }
            
                    r = sd_journal_seek_tail(j);
                    if (r < 0) {
                            fprintf(stderr, "Failed to seek tail: %s\n", strerror(-r));
                            return 1;
                    }
            
                    if (getenv("seek"))
                            r = sd_journal_previous_skip(j, 0);
                    else
                            r = sd_journal_next_skip(j, 0);
                    if (r < 0) {
                            fprintf(stderr, "Failed to skip: %s\n", strerror(-r));
                            return 1;
                    }
            
                    r = sd_journal_wait(j, (uint64_t) -1);
                    if (r < 0) {
                            fprintf(stderr, "Failed to wait for changes: %s\n", strerror(-r));
                            return 1;
                    }
            
                    for (;;)  {
                            const void *d;
                            size_t l;
                            r = sd_journal_next(j);
                            if (r < 0) {
                                    fprintf(stderr, "Failed to iterate to next entry: %s\n", strerror(-r));
                                    break;
                            }
                            if (r == 0) {
                                    /* Reached the end, let's wait for changes, and try again */
                                    r = sd_journal_wait(j, (uint64_t) -1);
                                    if (r < 0) {
                                            fprintf(stderr, "Failed to wait for changes: %s\n", strerror(-r));
                                            break;
                                    }
                                    continue;
                            }
                            r = sd_journal_get_data(j, "MESSAGE", &d, &l);
                            if (r < 0) {
                                    fprintf(stderr, "Failed to read message field: %s\n", strerror(-r));
                                    continue;
                            }
                            printf("%.*s\n", (int) l, (const char*) d);
                    }
                    sd_journal_close(j);
                    return 0;
            }

    + D-Bus
        + [Understanding D-Bus](http://free-electrons.com/pub/conferences/2016/meetup/dbus/josserand-dbus-meetup.pdf)
        + [terse DBus introspection table - borrowed from D lang](http://www.dsource.org/projects/dbus-d/wiki/Introspection)
        + [Building object-oriented software with the D-Bus messaging system](https://www.doria.fi/bitstream/handle/10024/78669/gradu2012Salli.pdf?sequence=1)
        + [Profiling and Optimizing D-Bus APIs](https://willthompson.co.uk/talks/profiling-and-optimizing-d-bus-apis.pdf)
        + [DBus: How to use variant](https://lists.freedesktop.org/archives/dbus/2007-July/008119.html)
        + [The Extended Introspection XML Format](https://wiki.allseenalliance.org/irb/extended_introspection_xml)
        + [CommonAPI C++ D-Bus in 10 minutes (from scratch)](https://at.projects.genivi.org/wiki/pages/viewpage.action?pageId=5472316)
            + [CommonAPI C++ Tutorial](https://at.projects.genivi.org/wiki/pages/viewpage.action?pageId=5472311)
            + [A framework for defining and transforming interfaces](https://github.com/franca/franca)
        + Telepathy
            + [Telepathy is a modular framework for real-time communications](http://www.aosabook.org/en/telepathy.html)
            + [Telepathy docs](https://telepathy.freedesktop.org/wiki/Documentation/)
            + [Telepathy DbusSpec](https://telepathy.freedesktop.org/wiki/DbusSpec/)
        + [QDBus : Send an array of objects (C++)](http://www.qtcentre.org/threads/47018-QDBus-Send-an-array-of-objects-(C-))
        + [[dbus-cplusplus-devel] Variant type handling](https://sourceforge.net/p/dbus-cplusplus/mailman/message/25874526/)
        + [Passing structure over d-bus - glib - example](https://lists.freedesktop.org/archives/dbus/2008-January/009171.html)
        + [[dbus-cplusplus-devel] Proposal: Give objects through dbus-c++](https://sourceforge.net/p/dbus-cplusplus/mailman/message/20200933/)
        + [DBus speed presentation](https://willthompson.co.uk/talks/the-slothful-ways-of-d-bus.pdf)
        + dbus-c++ and g++-7.1
            + [#18 Invalid template code in Threading class](https://sourceforge.net/p/dbus-cplusplus/patches/18/)    
            + tl;dr
              patch '/usr/include/dbus-c++-1/dbus-c++/dispatcher.h'
        + sdbus - and shutdown
            + [The new sd-bus API of systemd](http://0pointer.net/blog/the-new-sd-bus-api-of-systemd.html)
                + [Patrick Williams' gists for sdbus](https://gist.github.com/williamspatrick)
            + [systemd-233/src/libsystemd/sd-bus/test-bus-objects.c](https://fossies.org/linux/systemd/src/libsystemd/sd-bus/test-bus-objects.c)
            + [C++ bindings for systemd dbus APIs](https://github.com/openbmc/sdbusplus)    

            tl;dr poweroff
            ```
            gdbus introspect --system --dest org.freedesktop.systemd1 --object-path /org/freedesktop/systemd1
            ...
              interface org.freedesktop.systemd1.Manager {
                methods:
            ...
                 PowerOff();
            ...
            ```
            ```sh
            sudo busctl call org.freedesktop.systemd1 /org/freedesktop/systemd1 org.freedesktop.systemd1.Manager PowerOff
            reboot: Power down
            ```
            ```c++
            #include <stdio.h>
            #include <stdlib.h>
            #include <systemd/sd-bus.h>
             
            int main(int argc, char *argv[])
            {
                sd_bus_error error = SD_BUS_ERROR_NULL;
                sd_bus_message *m = NULL;
                sd_bus *bus = NULL;
                const char *path;
                int r;
             
                // Connect to the system bus
                r = sd_bus_open_system(&bus);
                if (r < 0) {
                    fprintf(stderr, "Failed to connect to system bus: %s\n", strerror(-r));
                    goto finish;
                }
             
                // Issue the method call and store the respons message in m
                r = sd_bus_call_method(bus,
                                       "org.freedesktop.systemd1",           // service to contact
                                       "/org/freedesktop/systemd1",          // object path
                                       "org.freedesktop.systemd1.Manager",   // interface name
                                       "PowerOff",                           // method name
                                       &error,                               // object to return error in
                                       nullptr,                              // input signature
                                       nullptr);                             // 1st arg
                if (r < 0) {
                    fprintf(stderr, "Failed to issue method call: %s\n", error.message);
                    goto finish;
                }
             
                /* Parse the response message */
                r = sd_bus_message_read(m, "o", &path);
                if (r < 0) {
                    fprintf(stderr, "Failed to parse response message: %s\n", strerror(-r));
                    goto finish;
                }
             
                printf("Queued service job as %s.\n", path);
             
            finish:
                sd_bus_error_free(&error);
                sd_bus_message_unref(m);
                sd_bus_unref(bus);
             
                return r < 0 ? EXIT_FAILURE : EXIT_SUCCESS;
            }
            ```
            ```sh
            g++ systemd-service-client.cc -o systemd-service-client `pkg-config --cflags --libs libsystemd`
            ``` 

    + WebSockets
        + [ws: a Node.js WebSocket library](https://github.com/websockets/ws#sending-and-receiving-text-data)
            + [Autobahn test suite reports](http://websockets.github.io/ws/)    
            tl;dr
            ```sh
            npm install -g ws
            ...
            ```

    + [How to shutdown Linux using C++ or Qt without call to “system()”?](http://stackoverflow.com/questions/28812514/how-to-shutdown-linux-using-c-or-qt-without-call-to-system/28812629)
        + [Core utility library for all LXQt components http://lxqt.org](https://github.com/lxde/liblxqt/blob/master/lxqtpower/lxqtpowerproviders.cpp)


+ profilers
    + [gperftools: Fast, multi-threaded malloc() and nifty performance analysis tools](https://code.google.com/p/gperftools/?redir=1)
        + [cpuprofile doc](http://google-perftools.googlecode.com/svn/trunk/doc/cpuprofile.html)
        + [Issue 278 in google-perftools: CPU profiler shows function addresses instead of function names](https://groups.google.com/forum/#!topic/google-perftools/BQqP6ectdoQ)
        + [Instructing configure where libunwind lives: an answer to `#error Cannot calculate stack trace: will need to write for your environment`](https://groups.google.com/forum/#!topic/google-perftools/30OlGHFNKZw)
    + [IgProf, The Ignominous Profiler](http://igprof.org/index.html)
    + [OProfile](http://oprofile.sourceforge.net/news/)
    + [Heaptrack - A Heap Memory Profiler for Linux](http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux)

    + [http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux](http://milianw.de/blog/heaptrack-a-heap-memory-profiler-for-linux)

    + [Ubuntu Linux C++ error: undefined reference to 'clock_gettime' and 'clock_settime' : add `-lrt`](http://stackoverflow.com/questions/2418157/ubuntu-linux-c-error-undefined-reference-to-clock-gettime-and-clock-settim)
    + Memory profiling
        + [How do VmRSS and resident set size match?](http://stackoverflow.com/questions/10400751/how-do-vmrss-and-resident-set-size-match)

+ [purescript - A small strongly typed language that compiles to Javascript](http://purescript.org)
    + [github repo for purescript](https://github.com/purescript/purescript)
    + [a bunch of purescript repos](https://github.com/freebroccolo?tab=repositories)

+ [How to extract RPM or DEB packages](http://www.g-loaded.eu/2008/01/28/how-to-extract-rpm-or-deb-packages/)

+ Linux From Scratch
    + [LFS root](http://www.linuxfromscratch.org/)
    + [Beyond Linux® From Scratch (systemd edition)](http://www.linuxfromscratch.org/blfs/view/systemd/)

+ Docker+Kubernetes+FireCracker
    + [Основы Kubernetes](https://habr.com/ru/post/258443/)
        + [How to install Kubernetes on Ubuntu 18.04 Bionic Beaver Linux](https://linuxconfig.org/how-to-install-kubernetes-on-ubuntu-18-04-bionic-beaver-linux)
            + [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

    + [Поняв Docker](https://habrahabr.ru/post/277699/)
    + [Образы и контейнеры Docker в картинках](http://habrahabr.ru/post/272145/)
    + [Configure and troubleshoot the Docker daemon](https://docs.docker.com/engine/admin/)
    + [Starting Docker as Daemon on Ubuntu](https://stackoverflow.com/questions/26137834/starting-docker-as-daemon-on-ubuntu)
        + tl;dr
        ```sh
        sudo service docker restart
        ```
    + [add-apt-repository: command not found in Docker installation on Ubuntu](https://github.com/threatstream/mhn/issues/284)
        + tl;dr docker command to add g++-7 to ubuntu16.04 docker image
        ```sh
        apt-get install -y software-properties-common python-software-properties && \
        add-apt-repository ppa:ubuntu-toolchain-r/test && \
        apt-get -qq update && \
        apt-get install -y -qq gcc-7 g++-7 gfortran-7 && \
        ```
    + [docker run -> name is already in use by container](https://stackoverflow.com/questions/31697828/docker-run-name-is-already-in-use-by-container)
        + tl;dr `docker rm $(docker ps -aq --filter name=CONTAINER_NAME)`

    + [Secure and fast microVMs for serverless computing](https://github.com/firecracker-microvm/firecracker)

+ CLion
    + [Debugging in CLion](https://blog.jetbrains.com/clion/2015/05/debug-clion/)
    + [How to enable debugging for CLion](https://stackoverflow.com/questions/42509757/how-to-enable-debugging-for-clion)
    + [Commands available during CGDB mode](http://cgdb.sourceforge.net/docs/cgdb-no-split.html)

+ Jenkins
    + [Jenkins - Running a single job in master as well as slave](https://stackoverflow.com/questions/9214501/jenkins-running-a-single-job-in-master-as-well-as-slave)
    + [Hudson: Copy artifact from master to slave fails](https://stackoverflow.com/questions/5830334/hudson-copy-artifact-from-master-to-slave-fails)
    + [A VERY QUICK GUIDE TO DEPLOYING ARTIFACTS WITH JENKINS](https://codurance.com/training/2014/10/03/guide-to-deploying-artifacts-with-jenkins/)

+ Haskell (see also `pandoc` and `diagrams` links above)
    + [Haskell Communities and Activities Report Twenty-Ninth Edition – November 2015](https://www.haskell.org/communities/11-2015/html/report.html)
        + [Haskell Programming _from first principles_](http://haskellbook.com/feedback.html)
+ C
    + [9 интересных трюков на Си, с которыми вы раньше не сталкивались](https://tproger.ru/translations/9-clang-tricks/)
    + [How do I create a custom file system in C?](https://www.quora.com/How-do-I-create-a-custom-file-system-in-C)

+ C++
    + [Feature freeze C++20. Coroutines, Modules и прочее](https://habr.com/ru/company/yandex/blog/438864/)

    + C++ Best Practices
        + [C++ Best Practices](https://lefticus.gitbooks.io/cpp-best-practices/content/02-Use_the_Tools_Available.html)
        + [C++ Russia 2017: Антон Полухин, Как делать не надо: C++ велосипедостроение для профессионалов](https://www.youtube.com/watch?v=rJWSSWYL83U)
        + [Зачем избегать друзей, или как я растерял все свои плюсы](https://habr.com/ru/post/472780/)
        + [How to split a string in C++](https://www.fluentcpp.com/2017/04/21/how-to-split-a-string-in-c/)

+ [free modern C++ book: Discovering Modern C++](https://github.com/stoneyang-cs/cpp_book/blob/master/Discovering%20Modern%20C%2B%2B%20-%20Peter%20Gottschling.pdf)

    + CppCon
        + [C++ Atomics, From Basic to Advanced by Fedor Pikus](https://github.com/CppCon/CppCon2017/tree/master/Presentations/C%2B%2B%20Atomics%2C%20From%20Basic%20to%20Advanced)
        + [Building C++ Modules by Boris Kolpackov](https://github.com/CppCon/CppCon2017/tree/master/Presentations/Building%20C%2B%2B%20Modules)
        + [Concurrency, Parallelism and Coroutines - Anthony Williams](https://github.com/CppCon/CppCon2017/blob/master/Presentations/Concurrency%2C%20Parallelism%20and%20Coroutines/Concurrency%2C%20Parallelism%20and%20Coroutines%20-%20Anthony%20Williams%20-%20CppCon%202017.pdf)
        + [CUDA Kernels with C++ by Michael Gopshtein](https://github.com/CppCon/CppCon2018/blob/master/Presentations/cuda_kernels_with_cpp/cuda_kernels_with_cpp__michael_gopshtein__cppcon_2018.pdf)

    + [C++ TUTORIAL - TEMPLATES - 2018](https://www.bogotobogo.com/cplusplus/templates.php)

    + [C++11 async tutorial](https://solarianprogrammer.com/2012/10/17/cpp-11-async-tutorial/)

    + [C++ Lifetime safety, inspired by Rust](https://github.com/isocpp/CppCoreGuidelines/blob/master/docs/Lifetime.pdf)

    + [C++17 features list](http://www.bfilipek.com/2017/01/cpp17features.html)
        + [C++17 in details: Standard Library Utilities](http://www.bfilipek.com/2017/09/cpp17-details-utils.html)
        + [C++17 in details: Parallel Algorithms](http://www.bfilipek.com/2017/08/cpp17-details-parallel.html)
        + [Value Categories in C++17](https://medium.com/@barryrevzin/value-categories-in-c-17-f56ae54bccbe)
            + [Категории выражений в C++](https://m.habr.com/ru/post/441742/)
            + [C++17 **Guaranteed** Copy Elision](https://jonasdevlieghere.com/guaranteed-copy-elision/)
        + [Simplify code with 'if constexpr' in C++17](https://www.bfilipek.com/2018/03/ifconstexpr.html)
            + [Constexpr if alternative](https://stackoverflow.com/questions/43587405/constexpr-if-alternative)
        + [C++17 Fold expressions](http://filipjaniszewski.com/2016/11/24/c17-folding-expression/)
            + [Reduce: From functional programming to C++17 Fold expressions - Nikos Athanasiou - Meeting C++ 2016](https://www.youtube.com/watch?v=ymNdAkS7Ljc)
        + [simplify C++](https://arne-mertz.de/category/cpp/modern-cpp/)
            + [`std::make_shared` vs. the Normal `std::shared_ptr` Constructor](https://arne-mertz.de/2018/09/make_shared-vs-the-normal-shared_ptr-constructor/)
            + [Как устроен shared_ptr](http://artemy-kolesnikov.blogspot.com/2014/11/sharedptr.html?m=1)
            + [Как устроен weak_ptr](http://artemy-kolesnikov.blogspot.com/2014/11/weakptr.html?m=1)
        + [Top 10 dumb mistakes to avoid with C++ 11 smart pointers](https://www.acodersjourney.com/top-10-dumb-mistakes-avoid-c-11-smart-pointers/)

        + [Stanford C++ Style Guide](http://stanford.edu/class/archive/cs/cs106b/cs106b.1158/styleguide.shtml)
            + [Stanford C++ Style Guide](https://tproger.ru/translations/stanford-cpp-style-guide/amp/)

    + [Trending C++ github repositories](https://github.com/trending/c++)

    + [Optimized C++ book](http://www.guntheroth.com/)

    + [C++17 High Performance](https://github.com/PacktPublishing/Cpp-High-Performance)

    + Valery Lesin. C++ In-Depth, 2014
        + [Лекция 3. Move семантика и Rvalue reference](https://compscicenter.ru/media/slides/cpp_2_2014_spring/2014_02_25_cpp_2_2014_spring.pdf)

    + [The C++ Standards Library for Concurrency and Parallelism http://stellar-group.org/libraries/hpx](https://github.com/STEllAR-GROUP/hpx)
        + [HPX (High Performance ParalleX) is a general purpose C++ runtime system for parallel and distributed applications of any scale](http://stellar-group.org/libraries/hpx)
        + [HPX — рантайм-система для параллельных и распределенных вычислений](https://corehard.by/2016/02/15/conf2016-hpx/)

    + [Modern C++ for fun and profit](https://chariotsolutions.com/wp-content/uploads/2016/04/Modern-C-for-Fun-and-Profit-ETE.pdf)
        + [free C++ books](http://freecomputerbooks.com/langCppBooks.html)
        + [MODERN C++ FOR C PROGRAMMERS: PART 4](https://ds9a.nl/articles/posts/cpp-4/)

    + [using extern template (C++11)](https://stackoverflow.com/questions/8130602/using-extern-template-c11)
        + tl;dr
            + use case in [Flexible Collision Library](https://github.com/flexible-collision-library/fcl)
            + don't confuse with [export templates](https://stackoverflow.com/questions/5416872/using-export-keyword-with-templates)

    + [Is pass-by-value a reasonable default in C++11?](https://stackoverflow.com/questions/7592630/is-pass-by-value-a-reasonable-default-in-c11/7592741#7592741)

    + [C++ samples](http://www.cppsamples.com/)
        + [Introduction To valarray](http://cppisland.com/?p=518)
            + [C++ valarray vs. vector](https://stackoverflow.com/questions/1602451/c-valarray-vs-vector)
        + [Atomic Basics](http://cppisland.com/?p=436)
        + [Подборка ресурсов с примерами кода на разных языках](https://tproger.ru/digest/learn-everything-by-examples/)

    + enum to string in modern C++11 / C++14 and future C++17 / C++20
        + [enum to string in modern C++11 / C++14 and future C++17 / C++20](https://stackoverflow.com/questions/28828957/enum-to-string-in-modern-c11-c14-and-future-c17-c20)
        + [Enum to string в современном C ++ и будущем C ++ 17 / C ++ 20](http://qaru.site/questions/9861/enum-to-string-in-modern-c-and-future-c17-c20)
        + [How to perform tuple arithmetic in C++ (c++11/c++17)?](https://stackoverflow.com/questions/47209672/how-to-perform-tuple-arithmetic-in-c-c11-c17)

    + [CRTP demystifyed](http://scrutator.me/post/2014/06/26/crtp_demystified.aspx)
        + [The Curiously Recurring Template Pattern (CRTP)](https://www.fluentcpp.com/2017/05/12/curiously-recurring-template-pattern/)
        + [What the Curiously Recurring Template Pattern can bring to your code](https://www.fluentcpp.com/2017/05/16/what-the-crtp-brings-to-code/)
        + [An Implementation Helper For The Curiously Recurring Template Pattern](https://www.fluentcpp.com/2017/05/19/crtp-helper/)
        + [The “Extract Interface” refactoring, at compile time](https://www.fluentcpp.com/2017/04/28/extract-interface-cpp/)

    + C++ and multithreading
        + Memory Model
            + [C++11 introduced a standardized memory model. What does it mean? And how is it going to affect C++ programming?](https://stackoverflow.com/questions/6319146/c11-introduced-a-standardized-memory-model-what-does-it-mean-and-how-is-it-g?rq=1)
        + [Top 20 C++ multithreading mistakes and how to avoid them](http://www.acodersjourney.com/2017/08/top-20-cplusplus-multithreading-mistakes/)    
        tl;dr
            1. Not using `join()` to wait for background threads before terminating an application.
            2. Trying to `join()` a thread that has been previously detached.
            3. Not realizing that `std::thread::join()` blocks the calling thread.
            4. Thinking that thread function arguments are pass by reference by default.    
                tl;dr use `std::ref()` for passing by reference.
            5. Not protecting shared data or shared resources with a critical section (eg. mutex).
            6. Forgetting to release locks after a critical section.
            7. Not keeping critical sections as compact and small as possible.
            8. Not acquiring multiple locks in the same order.
            9. Trying to acquire a `std::mutex` twice.
            10. Using mutexes when `std::atomic` types will suffice.
            11. Creating and Destroying a lot of threads directly when using a thread pool is available.
            12. Not handling exceptions in background threads.
            13. Using threads to simulate Asyn jobs when `std::async` will do.
            14. Not using `std::launch::async` if asynchronicity is desired.
            15. Calling `.get()` on a `std::future` in a time sensitive code path.
            16. Not realizing that an exception thrown inside an async task is propagated when `std::future::get()` is invoked.
            17. Using `std::async` when you need granular control over thread execution.
            18. Creating many more "Runnable" threads than available cores.
            19. Using `volatile` keyword for synchronization.
            20. Using a Lock Free architecture unless absolutely needed

        + [lucid and terse multithread intro](http://www.bogotobogo.com/cplusplus/multithreaded.php)
        + [Multithreading in C++11/14 – Part 1](http://www.loic-yvonnet.com/articles/multithreading-in-cpp14-part-1/)
        + [Multithreading in C++11/14 – Part 2](http://www.loic-yvonnet.com/articles/multithreading-in-cpp14-part-2/)
        + [Multithreading in C++11/14 – Part 12](http://www.loic-yvonnet.com/articles/multithreading-in-cpp14-part-12/)
        + Locking and Conditional Variables
            + [C++11 Multithreading  Part 7: Condition Variables Explained](https://thispointer.com/c11-multithreading-part-7-condition-variables-explained/)
            + [C++11-concurrency-tutorial-advanced-locking-and-condition-variables](http://baptiste-wicht.com/posts/2012/04/c11-concurrency-tutorial-advanced-locking-and-condition-variables.html)
            + [C++11 concurrency: condition variables](http://codexpert.ro/blog/2013/03/01/cpp11-concurrency-condition-variables/)
                + [Потоки, блокировки и условные переменные в C++11 [Часть 2]](https://habrahabr.ru/post/182626/)
            + [std::unique_lock<std::mutex> or std::lock_guard<std::mutex>?](https://stackoverflow.com/questions/20516773/stdunique-lockstdmutex-or-stdlock-guardstdmutex)
            + [std::unique_lock vs. от std::lock_guard?](https://ru.stackoverflow.com/questions/843495/%D0%A7%D0%B5%D0%BC-stdunique-lock-%D0%BE%D1%82%D0%BB%D0%B8%D1%87%D0%B0%D0%B5%D1%82%D1%81%D1%8F-%D0%BE%D1%82-stdlock-guard)
                + tl;dr
                almost the same, but `lock_guard` has less functionality, locks only once and more preferrable;
                use `lock_guard` unless you need unlocling, for `condition_variable`s that `wait()`ing from sleep.
        + [http://preshing.com/20130618/atomic-vs-non-atomic-operations/](http://preshing.com/20130618/atomic-vs-non-atomic-operations/)
        + [Comparison: Lockless programming with atomics in C++ 11 vs. mutex and RW-locks](https://www.arangodb.com/2015/02/comparing-atomic-mutex-rwlocks/)
        + [THE INFINITE LOOP: The ticket spinlock](https://geidav.wordpress.com/tag/spinlock/)
        + [Разработка → Конкурентность: Параллелизм](https://m.habrahabr.ru/post/318374/)
        + [What is the equivalent of boost::upgrade_to_unique_lock in STL?](http://stackoverflow.com/questions/30300212/what-is-the-equivalent-of-boostupgrade-to-unique-lock-in-stl)
        + [Охранные классы в boost::thread](http://htrd.su/wiki/zhurnal/2012/12/10/oxrannye_klassy_v_boost_thread)
        + [code review: Yet another event dispatcher in c++11](http://codereview.stackexchange.com/questions/123296/yet-another-event-dispatcher-in-c11)
        + [A simple proof-of-concept for C++11 event dispatching](https://github.com/Submanifold/Events)
    + [C++11 FAQ rom the author of C++](http://www.stroustrup.com/C++11FAQ.html)
    + [C++11 Tidbits: Template Aliases](https://blogs.oracle.com/pcarlini/entry/template_aliases)
        + [Why is `allocator::rebind` necessary when we have template template parameters?](http://stackoverflow.com/questions/12362363/why-is-allocatorrebind-necessary-when-we-have-template-template-parameters)
        + tl;dr
        instead of
        ```c++
        template<typename T>
        class allocator {
            //...
 
            template<typename U>
                struct rebind { typedef allocator<U> other; };
        };

        allocator<T>::rebind<U>::other x;  // sample usage
        ```
        can be rewritten
        ```c++
        template<typename T>
        class allocator {
            //...

            template<typename U>
                using rebind = allocator<U>;
        };

        allocator<T>::rebind<U> x;         // sample usage
        ```
        + why `rebind`
        ```c++
        template <typename T, typename A = std::allocator<T>>
        class list {
            struct node {
                T value;
                node* next;
                node* prev;
            };
            using allocator = typename A::template rebind<node>::other;
        };
        ```
    + [Variable template](http://en.cppreference.com/w/cpp/language/variable_template)
        + tl;dr
        ```
        template<class T>
        constexpr T pi = T(3.1415926535897932385);  // variable template
         
        template<class T>
        T circular_area(T r) // function template
        {
            return pi<T> * r * r; // pi<T> is a variable template instantiation
        }
        ```
    + [What Every C++ Developer Should Know to (Correctly) Define Global Constants](https://www.fluentcpp.com/2019/07/23/how-to-define-a-global-constant-in-cpp/)
    + [Why const Doesn't Make C Code Faster](https://theartofmachinery.com/2019/08/12/c_const_isnt_for_performance.html)
    + [Impossibly fast delegate in C++11](http://codereview.stackexchange.com/questions/14730/impossibly-fast-delegate-in-c11)
    + [Разработка → RAII + С++ variadic templates = win](https://habrahabr.ru/post/172817/)
    + [C++ convert integer to string at compile time](https://stackoverflow.com/questions/6713420/c-convert-integer-to-string-at-compile-time)
    + [Is there any RAII file handle already implemented?](https://stackoverflow.com/questions/22775500/is-there-any-raii-file-handle-already-implemented)
    + [Perfect forwarding and universal references in C++](http://eli.thegreenplace.net/2014/perfect-forwarding-and-universal-references-in-c/)
    + [Nobody Understands C++](http://blog2.emptycrate.com/tags/nobody-understands)
        + [Nobody Understands C++: Part 5: Template Code Bloat](http://blog2.emptycrate.com/content/nobody-understands-c-part-5-template-code-bloat)
    + [The C++ Core Guidelines are a set of tried-and-true guidelines, rules, and best practices about coding in C++](https://github.com/isocpp/CppCoreGuidelines)
    + [Поразрядная сортировка с человеческим лицом Radix sort in C++](http://habrahabr.ru/post/271677/)
    + [http://habrahabr.ru/company/infopulse/blog/274549/](http://habrahabr.ru/company/infopulse/blog/274549/)
    + [Советы о том, как писать на С в 2016 году](https://habrahabr.ru/company/inoventica/blog/275685/)
    + [The C++ scientist](http://jmabille.github.io/)
    + [Algorithms in C++](https://towardsdatascience.com/algorithms-in-c-62b607a6131d)
    + [Fast function to parse strings into double floating-point values](https://github.com/lemire/fast_double_parser)
    + [C++20: Python's map Function](https://www.modernescpp.com/index.php/c-20-pythons-map-function)
    + [HowardHinnant.github.io World-class C++ expert](http://howardhinnant.github.io/)
        + [Everything You Ever Wanted To Know About Move Semantics](https://github.com/HowardHinnant/presentations/blob/master/accu_2014/accu_2014.pdf)
        + [A date and time library based on the C++11 (and beyond) <chrono> header](https://github.com/HowardHinnant/date)
            + [This paper fully documents a date and time library for use with C++11 and C++14.](https://howardhinnant.github.io/date/date.html)
            + [How to get current time and date in C++?](http://stackoverflow.com/questions/997946/how-to-get-current-time-and-date-in-c)
            + [Convert std::duration to human readable time](https://stackoverflow.com/questions/22590821/convert-stdduration-to-human-readable-time)
    + [GoF patterns in modern C++](https://accu.org/content/conf2013/Tobias_Darm_Effective_GoF_Patterns.pdf)
        + [Effective GoF Patterns with C++11 and Boost—Tobias Darm](https://isocpp.org/blog/2013/10/patterns) 
    + selected stackoverflow questions
        + [What is the usefulness of `enable_shared_from_this`?](https://stackoverflow.com/questions/712279/what-is-the-usefulness-of-enable-shared-from-this)
            + [std::enable_shared_from_this](http://ru.cppreference.com/w/cpp/memory/enable_shared_from_this)
        + [How and why one would use Boost signals2?](http://stackoverflow.com/questions/18663490/how-and-why-one-would-use-boost-signals2)
            + [Is boost::signals2 overkill for simple applications?](http://stackoverflow.com/questions/22416860/is-boostsignals2-overkill-for-simple-applications?noredirect=1&lq=1)    
            tl;dr almost 100x performance penalty over plain function call
            + [Conversion of Qt Signals to Boost Signals2](http://stackoverflow.com/questions/20562430/conversion-of-qt-signals-to-boost-signals2)
                + [Messaging and Signaling in C++](https://meetingcpp.com/index.php/br/items/messaging-and-signaling-in-cplusplus.html)
            + [Making Boost.Signals2 More OOP‐Friendly](https://thehermeticvault.com/software-development/making-boost-signals2-more-oop-friendly)
                + [Protected вызов сигналов в Boost.Signals2](http://www.prog.org.ru/topic_29431_0.html)
        + [Should I use std::function or a function pointer in C++?](http://stackoverflow.com/questions/25848690/should-i-use-stdfunction-or-a-function-pointer-in-c)
            + [C++11 variadic std::function parameter](http://stackoverflow.com/questions/9242234/c11-variadic-stdfunction-parameter)
        + [Difference in make_shared and normal shared_ptr in C++](http://stackoverflow.com/questions/20895648/difference-in-make-shared-and-normal-shared-ptr-in-c)
        + [Usage of std::forward vs std::move](http://stackoverflow.com/questions/28828159/usage-of-stdforward-vs-stdmove)
        + [Advantages of using forward](http://stackoverflow.com/questions/3582001/advantages-of-using)
        + [How does std::forward work?](http://stackoverflow.com/questions/8526598/how-does-stdforward-work)
        + [Why is std::forward useless in this context](http://stackoverflow.com/questions/33999565/why-is-stdforward-useless-in-this-context)
        + [throwing exceptions out of a destructor](http://stackoverflow.com/questions/130117/throwing-exceptions-out-of-a-destructor)
            + summary: `Throwing an exception out of a destructor is dangerous. If another exception is already propagating the application will terminate.` 
            + ["More Effective C++" Item 11: Prevent exceptions from leaving destructors](http://bin-login.name/ftp/pub/docs/programming_languages/cpp/cffective_cpp/MEC/MI11_FR.HTM)
        + [What does the explicit keyword in C++ mean?](http://stackoverflow.com/questions/121162/what-does-the-explicit-keyword-in-c-mean)
            + dubbed from above link
            ```c++
            // Suppose you have a class String:

            class String {
            public:
                String(int n); // allocate n bytes to the String object
                String(const char *p); // initializes object with char *p
            };
            // Now if you try
            
            String mystring = 'x';
            // the char 'x' will be implicitly converted to int and then will call the String(int) constructor.
            // But this is not what the user might have intended. So to prevent such conditions, we shall define the constructor as explicit:
            
            class String {
            public:
                explicit String (int n); //allocate n bytes
                String(const char *p); // initialize sobject with string p
            };
            ```
        + [C++ convert from 1 char to string?](https://stackoverflow.com/questions/17201590/c-convert-from-1-char-to-string)
            + tl;dr
            ```c++
            char c = 42; std::cout << string(1, c) << std::endl;
            ```
        + [How to automatically convert strongly typed enum into int?](http://stackoverflow.com/questions/8357240/how-to-automatically-convert-strongly-typed-enum-into-int)

        + [Can a C++ lambda constructor argument capture the constructed variable?](http://stackoverflow.com/questions/29738655/can-a-c-lambda-constructor-argument-capture-the-constructed-variable)

        + generic variadic lambdas
            + TL;DR
            ```c++
            auto get_item = [&ifs](auto& item) {
                std::string line;
                std::getline(ifs, line);
                std::istringstream iss(line);
                iss >> item;
            };
            ...
            get_items(std::ref(params.thorus_params.xfirst), std::ref(params.thorus_params.yfirst));
            ```
            + [Fun with Lambdas: C++14 Style (part 3)](http://cpptruths.blogspot.ru/2014/08/fun-with-lambdas-c14-style-part-3.html)
            + [What is the easiest way to print a variadic parameter pack using std::ostream?](http://stackoverflow.com/questions/27375089/what-is-the-easiest-way-to-print-a-variadic-parameter-pack-using-stdostream)
            + [Composing Continuations](https://functionalcpp.wordpress.com/)
            + [Unpacking Tuples in C++14](http://aherrmann.github.io/programming/2016/02/28/unpacking-tuples-in-cpp14/)

        + [how to get only keys of values from map](https://stackoverflow.com/questions/39555726/stdmapstring-string-to-string-first-values)
            + [boost::adaptors::map_keys](https://greek0.net/boost-range/boost-adaptors-map_keys.html)

        ```c++
        #include <boost/range/adaptor/map.hpp>
        #include <boost/range/algorithm/copy.hpp>
        #include <boost/assign.hpp>
        #include <boost/algorithm/string/join.hpp>
        #include <algorithm>
        #include <iostream>
        #include <map>
        #include <vector>
        
        int main()
        {
            std::map<std::string, std::string> m;
            m["hello"] = "world";
            m["goodbye"] = "now";
        
            std::vector<std::string> o;
        //    boost::copy(m | boost::adaptors::map_keys, std::back_inserter(o));
            boost::copy(m | boost::adaptors::map_values, std::back_inserter(o));
            std::cout << boost::algorithm::join(o, ", ") << std::endl;
        }
        ```

        + boost.histogram **bare-bone** installation    
        ```sh
        https://github.com/boostorg/histogram.git
        https://github.com/boostorg/mp11.git
        https://github.com/boostorg/callable_traits.git
        https://github.com/boostorg/assert.git
        https://github.com/boostorg/throw_exception.git
        https://github.com/boostorg/core.git
        https://github.com/boostorg/config.git
        https://github.com/boostorg/variant2.git
        ```

        + [Python bindings for the C++14 Boost::Histogram library](https://github.com/scikit-hep/boost-histogram)
            + [Boost-histogram is a Python package providing Python bindings for Boost.Histogram ](https://boost-histogram.readthedocs.io/en/latest/)
            + [issues to Boost-histogram](https://github.com/scikit-hep/boost-histogram/issues)
        + [Boosting the Accuracy of Differentially Private Histograms Through Consistency](https://www.vldb.org/pvldb/vldb2010/pvldb_vol3/R91.pdf)
        + [Improving Accuracy and Robustness of Self-Tuning Histograms by Subspace Clustering](https://dbis.ipd.kit.edu/download/MineClusSTHoles_-_Minor_Revision.pdf)
            + [Improving Accuracy and Robustness of Self-Tuning Histograms by Subspace Clustering](https://www.youtube.com/watch?v=ZXb0ETrzhrs)

        + cheat-sheet for callbacks in C++
            + [Callback functions in c++](http://stackoverflow.com/questions/2298242/callback-functions-in-c)
        + [Using std::make_unique with custom deleter on a derived class?](http://stackoverflow.com/questions/37514101/using-stdmake-unique-with-custom-deleter-on-a-derived-class)
            + tl;dr you cannot indicate a custom deleter with the `make_*` helper functions for smart pointers (neither with `make_unique`, nor with `make_shared`). use
              to explicitly construct your pointer as it follows:
              ```c++
              std::unique_ptr<T, D> ptr{new T{)};
              ```
              If the deleter is not default constructible, you can do this:
              ```c++
              std::unique_ptr<T, D> ptr{new T{}, d};
              ```

        + [std::unique_ptr for class data member ABI (Pimpl idiom)](https://stackoverflow.com/questions/30072094/stdunique-ptr-for-class-data-member-abi-pimpl-idiom)
            + [Move constructor involving const unique_ptr](https://stackoverflow.com/questions/29194304/move-constructor-involving-const-unique-ptr)
            + [Why am I getting compile error “use of deleted function 'std::unique_ptr …”](https://stackoverflow.com/questions/39703954/why-am-i-getting-compile-error-use-of-deleted-function-stdunique-ptr/39705668)    
            tl;dr 
            The chief feature of std::unqiue_ptr is that it cannot be copied. That's by design, and the name tells you as much.
            take `std::unique_ptr<..> const&` -- no copy is needed.

        + `std::call_once()`
            + [std::call_once, std::once_flag](https://riptutorial.com/cplusplus/example/30171/std--call-once--std--once-flag)
            + [std::call_once vs std::mutex for thread-safe initialization](https://stackoverflow.com/questions/26985370/stdcall-once-vs-stdmutex-for-thread-safe-initialization)
            + [Why is this pointer needed when calling std::call_once()?](https://stackoverflow.com/questions/23197333/why-is-this-pointer-needed-when-calling-stdcall-once)
            + [std::call_once safe for non atomic variables?](https://stackoverflow.com/questions/48221492/stdcall-once-safe-for-non-atomic-variables)
            + [Is std::call_once a blocking call?](https://stackoverflow.com/questions/43054677/is-stdcall-once-a-blocking-call)

        + Some tips on iterators
            + [Common Knowledge: Output Iterator Adapters](http://www.drdobbs.com/common-knowledge-output-iterator-adapter/184401483)
            + [A smart iterator for inserting into a sorted container in C++](https://www.fluentcpp.com/2017/03/17/smart-iterators-for-inserting-into-sorted-container/)
        + C++ specialization
            + [Function Templates Partial Specialization in C++](https://www.fluentcpp.com/2017/08/15/function-templates-partial-specialization-cpp/)
            + [C++ Template specialization for subclasses with abstract base class](https://stackoverflow.com/questions/24936862/c-template-specialization-for-subclasses-with-abstract-base-class)
                + [c++ template specialization for base class](https://stackoverflow.com/questions/21437730/c-template-specialization-for-base-class)    
                tl;dr look [partial_specialization.cpp](https://github.com/alsam/cpp-samples/blob/master/c%2B%2Bnew-features/partial_specialization.cpp)
                ```c++
                template <typename M>
                struct SetTarget
                {
                  SetTarget(M* t): target(t) {}
                  M* target;
                };
                
                template <typename M, typename T, bool = std::is_base_of<OperationMessage, T>::value>
                struct SetId : public SetTarget<M>
                {
                  SetId(M* t) : SetTarget<M>(t) {}
                  void operator()(T)
                  {
                    std::cout << "SetId with -1\n";
                    SetTarget<M>::target->setId(-1);
                  }
                };
                
                // partial specialization
                template <typename M, typename T>
                struct SetId<M, T, true> : SetTarget<M>
                {
                  SetId(M* t) : SetTarget<M>(t) {}
                  void operator()(T msg)
                  {
                    std::cout << "SetId with msg.getSequence()\n";
                    SetTarget<M>::target->setId(msg.getSequence());
                  }
                };
                ```

        + selected boost tips
            + boost property tree
                + [boost property tree 5 minutes tutorial](http://www.boost.org/doc/libs/1_61_0/doc/html/property_tree/tutorial.html)
                + [3 ways of getting data from propert tree](http://www.boost.org/doc/libs/1_61_0/doc/html/property_tree/accessing.html)    
                tl;dr
                ```
                auto dump_vector = [](std::string const& name, auto const& v)
                {
                    std::cout << name << " : { ";
                    for (auto val : v)
                    {
                        std::cout << val << ", ";
                    }
                    std::cout << "}\n";
                };
                auto vec = xml_data.get("A.E.S.coeffs", std::vector<float>());
                dump_vector("coeffs", vec);
                ```
            + [Christian Aichinger's thoughts : boost::make_iterator_range](https://greek0.net/boost-range/boost-make_iterator_range.html)
                + [Overview of C++ Variable Initialization](https://greek0.net/cpp/initialization.html)

            + [A method to list all files in directory and sub-directories using boost and c++](https://stackoverflow.com/questions/37618229/a-method-to-list-all-files-in-directory-and-sub-directories-using-boost-and-c)
                + [GitGist : vivithemage/boost_list_directory.cpp](https://gist.github.com/vivithemage/9517678)
                ```c++
                #include <iostream>
                #include <string>
                #include <vector>
                #include <boost/filesystem.hpp>
                #include <boost/range.hpp>
                
                std::vector<std::string>
                get_file_list(std::string const& path)
                {
                    std::vector<std::string> files;
                    if (!path.empty()) {
                        boost::filesystem::path dir = ".";
                        boost::filesystem::recursive_directory_iterator it(dir), end;
                
                        for (auto& entry : boost::make_iterator_range(it, end))
                            if (boost::filesystem::is_regular(entry))
                                files.push_back(entry.path().native());
                    }
                    return files;
                }
                
                int main(int argc, char** argv)
                {
                    if (argc > 1) {
                        auto file_list = get_file_list(argv[1]);
                        for (auto const& f : file_list) {
                            std::cout << "- " << f << std::endl;
                        }
                    }
                }
                ```

        + [non-trivial designated initializers not supported](https://stackoverflow.com/questions/31215971/non-trivial-designated-initializers-not-supported)
        + [No matching function std::forward with lambdas](https://stackoverflow.com/questions/42044116/no-matching-function-stdforward-with-lambdas)
        + [Lambda expressions as class template parameters](https://stackoverflow.com/questions/5849059/lambda-expressions-as-class-template-parameters)
        + [Passing capturing lambda as function pointer](https://stackoverflow.com/questions/28746744/passing-capturing-lambda-as-function-pointer)
        + [Can I use std::vector as a template parameter or does it need to be std::vector<T>?](https://stackoverflow.com/questions/16925041/can-i-use-stdvector-as-a-template-parameter-or-does-it-need-to-be-stdvector)
        + [Clang refuses to compile libstdc++'s <filesystem> header](https://stackoverflow.com/questions/57963460/clang-refuses-to-compile-libstdcs-filesystem-header)
            + [How can I create directory tree in C++/Linux?](https://stackoverflow.com/questions/675039/how-can-i-create-directory-tree-in-c-linux)
            + [C++ Copy directory recursive under unix](https://stackoverflow.com/questions/36428121/c-copy-directory-recursive-under-unix)

        + [Hash Functions for C++ Unordered Containers](https://marknelson.us/posts/2011/09/03/hash-functions-for-c-unordered-containers.html)
            + [About size_t and ptrdiff_t](https://www.viva64.com/en/a/0050/)

    + REST API
        + [REST APIs in C++](http://lordjeb.com/category/c-2/)
        + [What is a good open source C++11 web/HTTP server library for building an application server ?](https://www.reddit.com/r/cpp/comments/2rjbrd/what_is_a_good_open_source_c11_webhttp_server/)
    + XML, HTML and network libraries in C++
        + [A Cheat Sheet for HTTP Libraries in C++](http://kukuruku.co/hub/cpp/a-cheat-sheet-for-http-libraries-in-c)
            + [Boost asio docs](http://theboostcpplibraries.com/boost.asio-network-programming)
        + [Benchmark. Analyzing and Testing Current HTML Parsers TL;DR HTML5Ever is written in Rust:) MyHTML is the fastest; Gumbo is produced by Google](https://lexborisov.github.io/benchmark-html-persers/)
        + [Parsing HTML with C++: Revisited](http://blog.laplante.io/2014/11/parsing-html-c-revisited/)
        + [Getting directory listing over http](http://stackoverflow.com/questions/4496182/getting-directory-listing-over-http)
        + [Downloading flv from youtube using curlpp on top of curl - video not playing](http://stackoverflow.com/questions/3850934/downloading-flv-from-youtube-using-curlpp-on-top-of-curl-video-not-playing)

    + [How do I terminate a thread in C++11?](http://stackoverflow.com/questions/12207684/how-do-i-terminate-a-thread-in-c11)
        + [How to terminate a C++ std::thread?](http://www.bo-yang.net/2017/11/19/cpp-kill-detached-thread)
            + [terminate_cpp_thread : kill thread](https://github.com/bo-yang/terminate_cpp_thread/blob/master/kill_cpp_thread.cc)
    + [What's the difference between “mutex” and “lock”?](http://stackoverflow.com/questions/9382122/whats-the-difference-between-mutex-and-lock)
    + [Потоки, блокировки и условные переменные в C++11 [Часть 2] ](https://habrahabr.ru/post/182626/)
    + [C++11 threads, affinity and hyperthreading](http://eli.thegreenplace.net/2016/c11-threads-affinity-and-hyperthreading/)
    + C++11 and semaphores
        + [C++0x has no semaphores? How to synchronize threads?](http://stackoverflow.com/questions/4792449/c0x-has-no-semaphores-how-to-synchronize-threads/19659736#19659736)
        + [Semaphores C++11 when Multithreading](http://austingwalters.com/multithreading-semaphores/)
        + [why do I need std::condition_variable?](http://stackoverflow.com/questions/16350473/why-do-i-need-stdcondition-variable)
    + intrusive prt vs. `std::shared_ptr`
        + [Boost intrusive_ptr and its usage in C++ programming](http://baptiste-wicht.com/posts/2011/11/boost-intrusive_ptr.html)
        + [Archives for posts with tag: intrusive_ptr](https://kinestheticcoding.wordpress.com/tag/intrusive_ptr/)
        + [intrusive_ptr против shared_ptr. Что лучше.](http://www.gamedev.ru/code/forum/?id=34739)
    + [Double-Checked Locking is Fixed In C++11](http://preshing.com/20130930/double-checked-locking-is-fixed-in-cpp11/)
        + [Several C++ singleton implementations](http://silviuardelean.ro/2012/06/05/few-singleton-approaches/) 
        ```c++
        class smartSingleton
        {
          private:
            static std::mutex _mutex;
         
            smartSingleton();
            smartSingleton(const smartSingleton& rs);
            smartSingleton& operator = (const smartSingleton& rs);
         
          public:
            ~smartSingleton();
         
          static std::shared_ptr& getInstance() {
            static std::shared_ptr instance = nullptr;

            if (!instance) {
              std::lock_guard lock(_mutex);

              if (!instance) {
                instance.reset(new smartSingleton());
              }
            }
         
            return instance;
          }
         
          void demo() { std::cout << "smart pointers # next - your code ..." << std::endl; }
        };
        ```
        + [How to implement multithread safe singleton in C++11 without using <mutex>](http://stackoverflow.com/questions/11711920/how-to-implement-multithread-safe-singleton-in-c11-without-using-mutex) 
        ```c++
        class Singleton
        {
        public:
        static Singleton & Instance()
        {
            // Since it's a static variable, if the class has already been created,
            // It won't be created again.
            // And it **is** thread-safe in C++11.
        
            static Singleton myInstance;
        
            // Return a reference to our instance.
            return myInstance;
        }
        
        // delete copy and move constructors and assign operators
        Singleton(Singleton const&) = delete;             // Copy construct
        Singleton(Singleton&&) = delete;                  // Move construct
        Singleton& operator=(Singleton const&) = delete;  // Copy assign
        Singleton& operator=(Singleton &&) = delete;      // Move assign
        
        // Any other public methods
        
        protected:
        Singleton()
        {
             // Constructor code goes here.
        }
        
        ~Singleton()
        {
             // Destructor code goes here.
        }
        
         // And any other protected methods.
        }
        ```

        + Progress Bar
            + [How to display a progress indicator in pure C/C++ (cout/printf)?](https://stackoverflow.com/questions/14539867/how-to-display-a-progress-indicator-in-pure-c-c-cout-printf)
            tl;dr more neat and nice solution    
            ```c++
            void printProgressNice (float percentage, int wid = 60)
            {
                const char PBFILLER[] = "█";
                int val = (int) (percentage * 100);
                int lpad = (int) (percentage * wid);
                int rpad = wid - lpad;
                printf("\r%3d%%[", val);
                while (lpad--)
                    printf("%s", PBFILLER);
                while (rpad--)
                    putchar(' ');
                printf("]");
                fflush(stdout);
            }
            ```
            + [Make better CLI progress bars with Unicode block characters](https://mike42.me/blog/2018-06-make-better-cli-progress-bars-with-unicode-block-characters)
            + [How to repeat a string a variable number of times in C++?](https://stackoverflow.com/questions/166630/how-to-repeat-a-string-a-variable-number-of-times-in-c)

        + [К тридцатилетию первого C++ компилятора: ищем ошибки в Cfront](http://www.viva64.com/ru/b/0355/)

        + [Is C++21 the Next Standard?](https://stackoverflow.com/questions/38789652/is-c21-the-next-standard/38789876)
            + [jucipp A lightweight & cross-platform IDE supporting the most recent C++ standards](https://gitlab.com/cppit/jucipp)
            + [Filament is a physically based rendering engine for Android, Windows, Linux and macOS](https://github.com/google/filament)

+ Test-driven development
    + [Test-driven development and unit testing with examples in C++](http://alexott.net/en/cpp/CppTestingIntro.html)
    + Google Unit Test
        + [github repository](https://github.com/google/googletest)
        + [good intro from IBM](http://www.ibm.com/developerworks/aix/library/au-googletestingframework.html)
        + [another good introduction](https://blog.jetbrains.com/rscpp/unit-testing-google-test/)
        + [Google Test Primer](https://github.com/google/googletest/blob/master/googletest/docs/Primer.md)
        + [Google TestAdvanced](https://github.com/google/googletest/blob/master/googletest/docs/AdvancedGuide.md)
        + fast deployment in `/usr/local`
        ```sh
        git clone https://github.com/google/googletest && pushd googletest && mkdir build && cd build && cmake .. && sudo make install
        ```
+ Scriptics selected tips
    + [Is double square brackets [[ ]] preferable over single square brackets [ ] in Bash?](https://stackoverflow.com/questions/669452/is-double-square-brackets-preferable-over-single-square-brackets-in-ba)
    + The most recently changed file.
        + [from here #5: 20 SHELL SCRIPTING QUESTIONS FOR PRACTICE](http://www.techbeamers.com/20-shell-scripting-questions-answers/)
    ```sh
    ls -lrt | grep ^- | awk 'END{print $NF}'
    ```
+ Build Systems
    + [CMake cheat sheet](https://ps-group.github.io/cxx/cmake_cheatsheet)
    + [CMake cannot find GoogleTest required library in Ubuntu](https://stackoverflow.com/questions/24295876/cmake-cannot-find-googletest-required-library-in-ubuntu)
    + [CMake by Example](https://mirkokiefer.com/cmake-by-example-f95eb47d45b1)
        + [How to copy contents of a directory into build directory after make with CMake?](https://stackoverflow.com/questions/13429656/how-to-copy-contents-of-a-directory-into-build-directory-after-make-with-cmake)    
        ```cmake
        add_custom_command(TARGET ${PROJECT_NAME} POST_BUILD
                           COMMAND ${CMAKE_COMMAND} -E copy_directory
                               ${CMAKE_SOURCE_DIR}/config $<TARGET_FILE_DIR:${PROJECT_NAME}>/config)
        ```
        + [Executing multiple post build commands in CMake depending on condition](https://stackoverflow.com/questions/33769077/executing-multiple-post-build-commands-in-cmake-depending-on-condition)
        + [Problems with directory delimiters turning into backslashes when running cmake](https://stackoverflow.com/questions/48717138/problems-with-directory-delimiters-turning-into-backslashes-when-running-cmake)    
        tl;dr    
        ```sh
         cmake -DCMAKE_CXX_COMPILER:FILEPATH=C:\Game Dev\Tools\MingW-
        ```

    + [What are the best open-source build systems for C/C++?](https://www.slant.co/topics/4263/~open-source-build-systems-for-c-c)
        + [Meson](https://www.slant.co/topics/4263/viewpoints/14/~open-source-build-systems-for-c-c~meson)
            + [Investigate using Meson build system alongside CMake](https://musescore.org/en/node/120116)
            + [Can you glob source code with meson?](https://stackoverflow.com/questions/34441673/can-you-glob-source-code-with-meson)

+ [Getting started with Google Test (GTest) on Ubuntu](https://www.eriksmistad.no/getting-started-with-google-test-on-ubuntu/)

+ Text search-and-replace (grep-like tools)
    + [Grep все, что можно](https://habrahabr.ru/post/316414/)
    + [amber (written in Rust - a good starting point)](https://github.com/dalance/amber)
        + [ag - the silver searcher](https://github.com/ggreer/the_silver_searcher)
    + [ripgrep is faster than {grep, ag, git grep, ucg, pt, sift}](https://blog.burntsushi.net/ripgrep/)
    + [A simple, fast and user-friendly alternative to 'find'](https://github.com/sharkdp/fd)

+ config formats : CSV vs. JSON vs. XML vs. YAML
    + [XML, JSON, YAML, TOML for Configuration](http://www.client9.com/article/xml-json-yaml-toml-for-configuration/)
    + [Is CSV a good alternative to XML and JSON?](http://programmers.stackexchange.com/questions/224929/is-csv-a-good-alternative-to-xml-and-json)
    + [C/C++ JSON parser/generator benchmark](https://github.com/miloyip/nativejson-benchmark)
        + [Tutorial for yaml-cpp](https://github.com/jbeder/yaml-cpp/wiki/Tutorial)

+ [Implementing an update/upgrade system for embedded Linux devices](http://stackoverflow.com/questions/6937592/implementing-an-update-upgrade-system-for-embedded-linux-devices)
    + [SWUpdate - Software Update for Embedded Systems](https://github.com/sbabic/swupdate)
        + [Creating Linux based Embedded System Images with Yocto](https://github.com/Nuand/bladeRF/wiki/Creating-Linux-based-Embedded-System-Images-with-Yocto)

+ VirtualBox
    + [VirtualBox on ArchLinux](https://wiki.archlinux.org/index.php/VirtualBox)
        + [GNU Parted](https://wiki.archlinux.org/index.php/GNU_Parted)
        ```sh
        parted /dev/sda
        (parted) mklabel gpt
        (parted) mkpart primary ext4 0% 100%
        mkfs.ext4 /dev/sda1
        tune2fs -L "/scratch" /dev/sda1
        ```
        + [ [Solved]Vboxdrv kernel module is not loaded](https://bbs.archlinux.org/viewtopic.php?id=117795)
    + [How To Install Ubuntu 14.04.3 LTS On VirtualBox](https://www.unixmen.com/install-ubuntu-14-04-3-lts-virtualbox/)
        ```sh
        sudo gpasswd -a <username> vboxusers
        VBoxManage list usbhost
        ```
+ [Checkpoint/Restore tool http://criu.org](https://github.com/xemul/criu)
    + [CRIU, a project to implement checkpoint/restore functionality for Linux.](http://criu.org/Main_Page)

+ Ext4
    + [Ext4 Disk Layout](https://ext4.wiki.kernel.org/index.php/Ext4_Disk_Layout)
    + [How to extract raw ext3 inode data from disk?](http://unix.stackexchange.com/questions/167222/how-to-extract-raw-ext3-inode-data-from-disk)
    + `debugfs` sample session:
    ```sh
    debugfs:  imap <262328>
    Inode 262328 is part of block group 32
            located at block 1048619, offset 0x0700
    debugfs:  show_inode_info <262328>
    Inode: 262328   Type: regular    Mode:  0644   Flags: 0x80000
    Generation: 933973137    Version: 0x00000000:00000001
    User:  1000   Group:  1000   Project:     0   Size: 948
    File ACL: 0    Directory ACL: 0
    Links: 1   Blockcount: 8
    Fragment:  Address: 0    Number: 0    Size: 0
     ctime: 0x5809deb8:1af1cef0 -- Fri Oct 21 12:24:08 2016
     atime: 0x5809deb8:1af1cef0 -- Fri Oct 21 12:24:08 2016
     mtime: 0x5809deb6:00000000 -- Fri Oct 21 12:24:06 2016
    crtime: 0x5809deb8:1af1cef0 -- Fri Oct 21 12:24:08 2016
    Size of extra inode fields: 32
    EXTENTS:
    (0):1082813
    ```

    + [Determine the size of a block device](http://unix.stackexchange.com/questions/52215/determine-the-size-of-a-block-device)
        + tl;dr with `sudo`
        ```sh
        #include <linux/fs.h>
        ...
        ioctl(file, BLKGETSIZE64, &file_size_in_bytes);
        ```
+ bash
    + [comparison operators](http://www.tldp.org/LDP/abs/html/comparison-ops.html)
    ```sh
    if [ "${target_partname}" = "" -o "${target_partname}" = "APP" ]; then
	build_fsimg "$localsysfile" "$fillpat" \
		    "$rootfssize" "$rootfs_type" "$rootfs_dir";
    fi;
    ```
    is equivalent to more readable
    ```sh
    if [[ "${target_partname}" == "" || "${target_partname}" == "APP" ]]; then
    ...
    ```
+ tmux
    + [Краткая шпаргалка по tmux](https://habrahabr.ru/post/126996/)

+ TCP backup
    + [Chapter 2. The Transport Layer: TCP, UDP, and SCTP](https://notes.shichao.io/unp/ch2/)
        + [Chapter 4. Elementary TCP Sockets](https://notes.shichao.io/unp/ch4/)
    + [«Boost.Asio C++ Network Programming». Глава 4: Клиент и Сервер](https://habrahabr.ru/post/195794/)
    + [Boost.Asio C++ Network Programming examples](http://www.boost.org/doc/libs/1_65_1/doc/html/boost_asio/examples/cpp11_examples.html)
    + [SOCKETS - SERVER & CLIENT C++ - 2017](http://www.bogotobogo.com/cplusplus/sockets_server_client.php#block_vs_non_blocking)
    + [Error : “Transport endpoint is already connected”](https://stackoverflow.com/questions/7140438/error-transport-endpoint-is-already-connected)
        + [Socket program gives “Transport endpoint is already connected” error](https://stackoverflow.com/questions/9873650/socket-program-gives-transport-endpoint-is-already-connected-error)
        + [Reconnecting with connect() on restarted server returns -Transport endpoint is already connected](https://stackoverflow.com/questions/16910973/reconnecting-with-connect-on-restarted-server-returns-transport-endpoint-is-a)
        + [Starter UDP Server And Client in C++](https://prglb.ru/4evp2)
        + [Creating a TCP Server in C++ [Linux / Code Blocks]](https://www.youtube.com/watch?v=cNdlrbZSkyQ)
        + [How to Watch TCP and UDP Ports in Real-time](https://www.tecmint.com/watch-tcp-and-udp-ports-in-linux/)

+ [The Illustrated TLS Connection Every byte of a TLS connection explained and reproduced](https://tls.ulfheim.net/)
    + [The Illustrated TLS Connection: Every byte explained](https://github.com/syncsynchalt/illustrated-tls)

+ [VPP](https://wiki.fd.io/view/VPP)
    + [VPP/What is VPP? The VPP platform is an extensible framework that provides out-of-the-box production quality switch/router functionality](https://wiki.fd.io/view/VPP/What_is_VPP%3F)
    + [VPP/Pulling, Building, Running, Hacking and Pushing VPP Code](_Hacking_and_Pushing_VPP_Code)    
    tl;dr
    ```
    git clone https://USERNAME@gerrit.fd.io/r/a/vpp
    ```
    + [Building FD.io VPP 18.10 on Ubuntu 18.04 LTS with Mellanox DPDK PMD without OFED](http://www.jimmdenton.com/vpp-1810-mellanox/)
    + [VPP/Installing VPP binaries from packages](https://wiki.fd.io/view/VPP/Installing_VPP_binaries_from_packages)
    + [Arch Linux in the Arch User Repository (AUR)](https://aur.archlinux.org/packages/vpp/)

+ [WHY MILLISECONDS MATTER : REST vs. gRPC](https://www.yonego.com/nl/why-milliseconds-matter/#gref)

+ Data transfer
    + [So you want to write to a file real fast…](https://blog.plenz.com/2014-04/so-you-want-to-write-to-a-file-real-fast.html)
        + tl;dr
        ```c++
        ssize_t do_sendfile(int in, int out)
        {
            ssize_t t = filesize(in);
            off_t ofs = 0;

            while(ofs < t) {
                if(sendfile(out, in, &ofs, t - ofs) == -1) {
                    assert(errno == EINTR);
                    continue;
                }
            }

            return t;
        }
        ```
        + [Use sendfile() to speed up transfers](https://github.com/giampaolo/pyftpdlib/issues/152)
    + [high CPU load by 'mmcqd' in Ubuntu](https://community.nxp.com/thread/318739)
    + [Copy a file in a sane, safe and efficient way](http://stackoverflow.com/questions/10195343/copy-a-file-in-a-sane-safe-and-efficient-way)
    + [Linux function to get mount points](http://stackoverflow.com/questions/9280759/linux-function-to-get-mount-points)
        + tl;dr    
        ```c
        #include <stdio.h>
        #include <stdlib.h>
        #include <mntent.h>
        
        int main(void)
        {
          struct mntent *ent;
          FILE *aFile;
        
          aFile = setmntent("/proc/mounts", "r");
          if (aFile == NULL) {
            perror("setmntent");
            exit(1);
          }
          while (NULL != (ent = getmntent(aFile))) {
            printf("%s %s\n", ent->mnt_fsname, ent->mnt_dir);
          }
          endmntent(aFile);
        }
    + [How to Get Available Filesystem Space on Linux: a C Function with a C++ Example](https://www.systutorials.com/136585/how-to-get-available-filesystem-space-on-linux-a-c-function-and-a-cpp-example/)    ```

+ [Linking](http://www.cs.utexas.edu/~witchel/429/lectures/11-linking.pdf)
    + [Controlling the Exported Symbols of Shared Libraries](https://www.gnu.org/software/gnulib/manual/html_node/Exported-Symbols-of-Shared-Libraries.html)
    + [Control over symbol exports in GCC](http://anadoxin.org/blog/control-over-symbol-exports-in-gcc.html)

+ packaging
    + [Hosting a Private Apt Repository on S3](https://zcox.wordpress.com/2012/08/13/hosting-a-private-apt-repository-on-s3/)
    + [Managing Apt Repos in S3 Using Lambda](http://webscale.plumbing/managing-apt-repos-in-s3-using-lambda)
        + [apt-s3](https://github.com/castlabs/apt-s3)

+ lock files
    + [Linux: What is the difference between advisory lock and mandatory lock?](https://www.quora.com/Linux-What-is-the-difference-between-advisory-lock-and-mandatory-lock)
    + [`flock` use case](http://stackoverflow.com/questions/1599459/optimal-lock-file-method)
    + [lock files: 2.9 Synchronizing Resource Access Across Processes on Unix](http://etutorials.org/Programming/secure+programming/Chapter+2.+Access+Control/2.9+Synchronizing+Resource+Access+Across+Processes+on+Unix/)

+ misc
    + [nm vs “readelf -s”](https://stackoverflow.com/questions/9961473/nm-vs-readelf-s)    
    tl;dr    
    ```sh
    nm -o -D *.so
    ```
    + [fdupes – A Comamndline Tool to Find and Delete Duplicate Files in Linux](http://www.tecmint.com/fdupes-find-and-delete-duplicate-files-in-linux/)
    + [Is there a difference between using pmount and mount?](https://superuser.com/questions/273956/is-there-a-difference-between-using-pmount-and-mount)
    + [How To Quickly Generate A Large File On The Command Line (With Linux)](http://www.skorks.com/2010/03/how-to-quickly-generate-a-large-file-on-the-command-line-with-linux/)
    + [How to check programatically if the Ethernet cable is plugged in?](https://unix.stackexchange.com/questions/163503/how-to-check-programatically-if-the-ethernet-cable-is-plugged-in)    

    tl;dr
    ```sh
    for i in $( ls /sys/class/net ); do echo $i; done
    dummy0
    enx00044b5acf64
    ip6tnl0
    lo
    rmnetctl
    sit0
    tunl0
    wlan0

    for i in $( ls /sys/class/net ); do echo -n $i: ; cat /sys/class/net/$i/carrier; done
    dummy0:cat: /sys/class/net/dummy0/carrier: Invalid argument
    enx00044b5acf64:1
    ip6tnl0:cat: /sys/class/net/ip6tnl0/carrier: Invalid argument
    lo:1
    rmnetctl:cat: /sys/class/net/rmnetctl/carrier: Invalid argument
    sit0:cat: /sys/class/net/sit0/carrier: Invalid argument
    tunl0:cat: /sys/class/net/tunl0/carrier: Invalid argument
    wlan0:1

    for i in $( ls /sys/class/net ); do echo -n $i: ; cat /sys/class/net/$i/operstate; done
    dummy0:down
    enx00044b5acf64:up
    ip6tnl0:down
    lo:unknown
    rmnetctl:down
    sit0:down
    tunl0:down
    wlan0:unknown
    ```
+ [Maximum length of the textual representation of an IPv6 address?](https://stackoverflow.com/questions/166132/maximum-length-of-the-textual-representation-of-an-ipv6-address)

+ [Apache Thrift vs Protocol Buffers detailed comparison as of 2019](https://www.slant.co/versus/9125/9127/~apache-thrift_vs_protocol-buffers)
    + [Apache Thrift Language Support](https://thrift.apache.org/docs/Languages)

+ [Slimjet Browser Review – speed and utility](https://malwarecomplaints.info/slimjet-browser-review-speed-utility/)

+ [Предметно-ориентированное проектирование на самом деле](https://habr.com/ru/post/490270/)
