#### manjaro-fcitx5
> manjaro-fcitx5 install guide

```shell
sudo pacman -S fcitx5 fcitx5-gtk fcitx5-qt fcitx5-rime
fcitx5-material-color
```
```shell
KDE install fcitx5-configtool
```

#### nano add ~/.pam_environment
> GTK_IM_MODULE=fcitx5
QT_IM_MODULE=fcitx5
XMODIFIERS="@im=fcitx5"

```shell
echo ${XDG_SESSION_TYPE}
x11
```
#### nano classicui.conf
1. Vertical Candidate List=True
2. PerScreenDPI=False
3. Font="Droid Sans Regular 16"
4. Theme=Material-Color-Pink

#### python pypi china DNA
```shell
mkdir ~/.pip
touch ~/.pip/pip.conf
nano ~/.pip/pip.conf
[global]
index-url = http://pypi.douban.com/simple
[install]
trusted-host=pypi.douban.com
```
1. 阿里云 http://mirrors.aliyun.com/pypi/simple/
2. 中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple/
3. 豆瓣(douban) http://pypi.douban.com/simple/
4. 清华大学 https://pypi.tuna.tsinghua.edu.cn/simple/

#### grub confg
```shell
↪ sudo update-grub
[sudo] bilier 的密码：
正在生成 grub 配置文件 ...
找到主题：/usr/share/grub/themes/manjaro/theme.txt
找到 Linux 镜像：/boot/vmlinuz-5.8-x86_64
找到 initrd 镜像：/boot/intel-ucode.img /boot/initramfs-5.8-x86_64.img
Found initrd fallback image: /boot/initramfs-5.8-x86_64-fallback.img
Adding boot menu entry for UEFI Firmware Settings ...
Found memtest86+ image: /boot/memtest86+/memtest.bin
完成
```

#### delete driver
```shell
list xf86-video
sudo pacman -Ss xf86-video
extra/xf86-video-amdgpu 19.1.0-2 (xorg-drivers) [已安装]
    X.org amdgpu video driver
extra/xf86-video-ati 1:19.1.0-2 (xorg-drivers) [已安装]
    X.org ati video driver
extra/xf86-video-dummy 0.3.8-4 (xorg-drivers)
    X.org dummy video driver
extra/xf86-video-fbdev 0.5.0-2 (xorg-drivers)
    X.org framebuffer video driver
extra/xf86-video-intel 1:2.99.917+913+g9236c582-1 (xorg-drivers) [已安装]
    X.org Intel i810/i830/i915/945G/G965+ video drivers
extra/xf86-video-nouveau 1.0.16-2 (xorg-drivers) [已安装]
    Open Source 3D acceleration driver for nVidia cards
extra/xf86-video-openchrome 0.6.0-4 (xorg-drivers)
    X.Org Openchrome drivers
extra/xf86-video-sisusb 0.9.7-3
    X.org SiS USB video driver
extra/xf86-video-vesa 2.5.0-1 (xorg-drivers xorg)
    X.org vesa video driver
extra/xf86-video-vmware 13.3.0-2 (xorg-drivers)
    X.org vmware video driver
extra/xf86-video-voodoo 1.2.5-11 (xorg-drivers)
    X.org 3dfx Voodoo1/Voodoo2 2D video driver
community/xf86-video-qxl 0.1.5-8 (xorg-drivers)
    Xorg X11 qxl video driver
```

#### Fix Bcm WIFI
```shell
uname -r
show 5.8.18-1-MANJARO
sudo pacman -S linux58-broadcom-wl
reboot
```