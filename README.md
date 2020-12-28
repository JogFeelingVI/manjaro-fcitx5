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
