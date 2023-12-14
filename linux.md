# linux links

+ Linux distributions tips

    + [GNU-Linux Anatomy](https://habr.com/ru/post/531872/)
        + [GNU-Linux Anatomy](https://gitlab.com/bergentroll/gnu-linux-anatomy)

    + Gentoo tips
        + [Gentoo Cheat Sheet](https://wiki.gentoo.org/wiki/Gentoo_Cheat_Sheet)

    + Arch Linux tips
        + [USB flash installation medium](https://wiki.archlinux.org/title/USB_flash_installation_medium)    
        ```sh
        dd bs=4M if=path/to/archlinux-version-x86_64.iso of=/dev/sdx conv=fsync oflag=direct status=progress
        sdx replacing /dev/sdx with your drive, e.g. /dev/sdb. (Do not append a partition number, so do not use something like /dev/sdb1):
        ```
        + [Arch Linux config files](https://github.com/afiskon/archlinux-on-desktop)
        + [Archlinux PKGBUILDs for Data Science, Machine Learning, Deep Learning, NLP and Computer Vision](https://github.com/mratsim/Arch-Data-Science)
        + [Arch Linux as your Day-to-day Desktop (2020)](https://ajohnsc.com/2020/arch-linux-as-your-day-to-day-desktop-(2020)/)
        + [The Recommended Way To Clean The Package Cache In Arch Linux](https://ostechnix.com/recommended-way-clean-package-cache-arch-linux/#:~:text=So%2C%20it%20is%20recommended%20to,sudo%20pacman%20%2DSc%22%20command.)    
        tl;dr    
        ```sh
        sudo paccache -r
        sudo paccache -rk 1
        sudo pacman -Sc
        sudo pacman -Scc
        ```
        + [Arch Linux first installation](https://d3s0x.github.io/arch-installation/)
            + [Arch Linux Installation (2020)](https://www.youtube.com/watch?v=UiYS8xWFXLY&feature=youtu.be)
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

            + [How to set up Systemd-boot on a new Arch Linux system](https://www.addictivetips.com/ubuntu-linux-tips/set-up-systemd-boot-on-arch-linux/)

            + [mkinitcpio (Русский)](https://wiki.archlinux.org/index.php/Mkinitcpio_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9))

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
                        + HOWTO up network see [Systemd-networkd](wiki.archlinux.org/index.php/Systemd-networkd)    
                        tl;dr    
                        ```sh
                        sudo vim /etc/systemd/network-20-wired.network

                        [Match]
                        Name=eno1

                        [Network]
                        Address=xx.xxx.xxx.xxx/xx
                        Gateway=xx.xxx.xxx.xxx
                        DNS=xx.xx.xx.xx
                        DNS=xx.xx.xx.xx
 
                        systemctl enable systemd-networkd.service
                        systemctl start systemd-networkd.service
                        ```

            + [Arch-Instruction.md](https://gist.github.com/tz4678/bd33f94ab96c96bc6719035fcac2b807)
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
            + [How to Use Arch Linux Network Manager](https://linuxhint.com/arch_linux_network_manager)    
            tl;dr    
            ```sh
            sudo systemctl enable NetworkManager.service
            sudo systemctl disable dhcpcd.service
            sudo systemctl enable wpa_supplicant.service
            sudo systemctl start NetworkManager.service

            sudo reboot

            nmcli device wifi list
            nmcli device wifi connect <SSID> password <SSID_password>
            nmcli connection show
            nmcli device
            nmcli connection show
            nmcli connection up uuid <UUID>
            nmcli radio wifi off
            nmcli radio wifi on
            sudo ls /etc/NetworkManager/system-connection
            ```
            + [PRIME is a technology used to manage hybrid graphics found on recent desktops and laptops](https://wiki.archlinux.org/index.php/PRIME)
            + HP Omen systemd-boot boot menu not working
                + [systemd-boot boot menu ignoring keyboard input (PS/2)](https://github.com/systemd/systemd/issues/19191)
                + [commit: boot: Use str_verscmp for special UEFI](https://github.com/systemd/systemd/pull/19319/commits)
                + [patch: boot: Use str_verscmp for special UEFI](https://github.com/systemd/systemd/pull/19319/files)
            + [Linux: We need Tiling Desktop Environments](https://haydenjames.io/linux-tiling-desktop-environments/)
            + [The Ultimate Guide to i3 Customization in Linux](https://itsfoss.com/i3-customization/)
            + [i3 desktop install](https://xakep.ru/2017/03/22/geek-desktop/)
            + [Disabling Sleep / Hybernate / Suspend not working](https://forum.endeavouros.com/t/disabling-sleep-hybernate-suspend-not-working/24217)
            ```sh
            # cat ~/.config/i3/config
            # disable power saving for display
            exec --no-startup-id xset s off -dpms
            ```
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
            + [Lock and blank screen?](https://www.reddit.com/r/i3wm/comments/941rbd/lock_and_blank_screen/)    
            tl;dr `i3lock -c 000000`
            + Screen brightness
                + [Control screen brightness in i3](https://unix.stackexchange.com/questions/526653/control-screen-brightness-in-i3)
                + [How to change LCD intensivity/brightness](https://unix.stackexchange.com/questions/61256/how-to-change-lcd-intensivity-brightness)
                                ```sh
                                cat /sys/class/backlight/amdgpu_bl0/actual_brightness
                                sudo cat 8 > /sys/class/backlight/amdgpu_bl0/brightness
                                `````
            + [Advanced Linux Sound Architecture (Русский)](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9)#%D0%92%D1%8B%D0%B1%D0%BE%D1%80_%D1%81%D1%82%D0%B0%D0%BD%D0%B4%D0%B0%D1%80%D1%82%D0%BD%D0%BE%D0%B9_PCM_%D1%81_%D0%BF%D0%BE%D0%BC%D0%BE%D1%89%D1%8C%D1%8E_%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9_%D0%BE%D0%BA%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)    
            tl;dr    
            ```sh
            $ aplay -l

            **** List of PLAYBACK Hardware Devices ****
            card 0: Intel [HDA Intel], device 0: CONEXANT Analog [CONEXANT Analog]
              Subdevices: 1/1
              Subdevice #0: subdevice #0
            card 0: Intel [HDA Intel], device 1: Conexant Digital [Conexant Digital]
              Subdevices: 1/1
              Subdevice #0: subdevice #0
            card 1: JamLab [JamLab], device 0: USB Audio [USB Audio]
              Subdevices: 1/1
              Subdevice #0: subdevice #0
            card 2: Audio [Altec Lansing XT1 - USB Audio], device 0: USB Audio [USB Audio]
              Subdevices: 1/1
              Subdevice #0: subdevice #0

            Важно: Simply setting a type hw as default card is equivalent to addressing hardware directly, which leaves the device unavailable to other applications. This method is only recommended if it is a part of a more sophisticated setup ~/.asoundrc or if user deliberately wants to address sound card directly (digital output through eic958 or dedicated music server for example).

            For example, the last entry in this list has the card ID 2 and the device ID 0. To set this card as the default, you can either use the system-wide file /etc/asound.conf or the user-specific file ~/.asoundrc. You may have to create the file if it does not exist. Then insert the following options with the corresponding card.

            pcm.!default {
                type hw
                card 2
            }

            ctl.!default {
                type hw
                card 2
            }

            $ cat /etc/asound.conf
            pcm.!default {
                type hw
                card 2
            }

            ctl.!default {
                type hw
                card 2
            }
            ```
            + [Настройка звука в Ubuntu](https://habr.com/ru/post/343718/)
            + [5.11: amdgpu: Unsupported power profile mode 0 on RENOIR](https://gitlab.freedesktop.org/drm/amd/-/issues/1488)
            + [How to Install LightDM Display Manager on Arch Linux](https://linoxide.com/linux-how-to/install-lightdm-arch-linux/)
            + [pacman db locked](https://bbs.archlinux.org/viewtopic.php?id=233989)    
              tl;dr `sudo rm /var/lib/pacman/db.lck`
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

        + 2 video cards iGPU & dGPU and external monitor
            + [PRIME Render Offload в Arch и Manjaro Linux](https://mascloud.ru/prime-render-offload-v-arch-i-manjaro-linux/)    
            tl;dr /etc/X11/xorg.conf    
            ```
            Section "ServerLayout"
              Identifier     "Layout0"
                Option         "AllowNVIDIAGPUScreens"
                #Screen      0  "iGPU" 0 0
                Screen      0  "dGPU" 0 0
            EndSection
            Section "Device"
                Identifier     "iGPU"
                Driver         "modesetting"
                BusID          "PCI:6:0:0" #Проверить свой BusID
            EndSection
            Section "Device"
                Identifier     "dGPU"
                Driver         "nvidia"
                BusID          "PCI:1:0:0" #Проверить свой BusID
            EndSection
            #Section "Screen"
            #    Identifier     "iGPU"
            #    Device         "iGPU"
            #    DefaultDepth    24
            #    SubSection     "Display"
            #        Viewport    0 0
            #    EndSubSection
            #EndSection

            Section "Screen"
                Identifier     "dGPU"
                Device         "dGPU"
                DefaultDepth    24
                SubSection     "Display"
                    Viewport    0 0
                EndSubSection
            EndSection

            Section "OutputClass"
                Identifier "iGPU"
                MatchDriver "i915"
                Driver "modesetting"
            EndSection
 
            Section "OutputClass"
                Identifier "dGPU"
                MatchDriver "nvidia-drm"
                Driver "nvidia"
                Option "AllowEmptyInitialConfiguration"
                Option "PrimaryGPU" "yes"
                ModulePath "/usr/lib/nvidia/xorg"
                ModulePath "/usr/lib/xorg/modules"
            EndSection
            ```

            ```sh
            nvidia-settings
            xrandr --listproviders
            glxinfo | grep "OpenGL renderer"
            prime-run glxinfo | grep "OpenGL renderer
            __NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia glxinfo | grep OpenGL
            ```

            + [PRIME](https://wiki.archlinux.org/index.php/PRIME)
            + [Multihead](https://wiki.archlinux.org/index.php/multihead)
            + [Dual monitor setup](https://bbs.archlinux.org/viewtopic.php?id=146000)

        + [do nothing when laptop lid is closed](https://askubuntu.com/questions/15520/how-can-i-tell-ubuntu-to-do-nothing-when-i-close-my-laptop-lid)
        tl;dr edit `/etc/systemd/logind.conf`
        ```
        ...
        #HandleLidSwitch=suspend
        HandleLidSwitch=ignore
        #HandleLidSwitchExternalPower=suspend
        HandleLidSwitchExternalPower=ignore
        ...
        ```
        `sudo systemctl restart systemd-logind`

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

        + [What happened to LLVM 15?](https://www.reddit.com/r/archlinux/comments/yc68pp/what_happened_to_llvm_15/)
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

    + [How io_uring and eBPF Will Revolutionize Programming in Linux](https://thenewstack.io/how-io_uring-and-ebpf-will-revolutionize-programming-in-linux/)
    + [The Implementation of epoll (1)](https://idndx.com/the-implementation-of-epoll-1/)
    + [The Implementation of epoll (2)](https://idndx.com/the-implementation-of-epoll-2/)
    + [The Implementation of epoll (3)](https://idndx.com/the-implementation-of-epoll-3/)
    + [The Implementation of epoll (4)](https://idndx.com/the-implementation-of-epoll-4/)
        + [Реализация epoll, часть 4](https://habr.com/ru/company/ruvds/blog/527174/)

    + [LINUX FU: GLOBAL SEARCH AND REPLACE WITH RIPGREP](https://hackaday.com/2020/10/14/linux-fu-global-search-and-replace-with-ripgrep/)
        + [Кунг-фу стиля Linux: глобальный поиск и замена строк с помощью ripgrep](https://habr.com/ru/company/ruvds/blog/527242/)
    + [LINUX FU: MONITOR DISKS](https://hackaday.com/2020/11/05/linux-fu-monitor-disks/)
    tl;dr    
    ```sh
    yay -S duf
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

+ [The Linux Kernel Module Programming Guide](https://sysprog21.github.io/lkmpg/)
