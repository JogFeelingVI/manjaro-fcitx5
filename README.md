# manjaro-fcitx5
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

# python pypi china DNA
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
