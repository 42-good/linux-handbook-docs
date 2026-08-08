# Pacman

全称：Package Manager
包格式：pacman

## 解释

pacman是大部分Arch系的软件包管理器。

!!! warning "警告"
    Arch 严禁“部分升级”（Partial Upgrade）。请勿在未同步升级全系统的情况下单独安装或更新某个软件，否则极易导致系统依赖断裂造成所谓的 **“滚挂”** ！此外，推荐配置 **AUR (Arch User Repository)** 并配合 yay 或 paru 等助手使用，可以提升使用体验。

???+ note "多选题"
    在安装软件时，您可能见到类似如下的选项:
    ```
    :: There are 2 providers available for jack:
    :: Repository extra
    1) jack2  2) pipewire-jack
    ```
    这时，我们推荐您选择带有如下字样的选项：

    - `pipewire`: 音频服务
    - `ffmpeg`: 多媒体后端
    - `NetworkManager`: 网络链接管理
    - `cups`: 打印
    - `systemd-resolved`: DNS解析
    
    以上列表无法覆盖所有选项，若遇到未列出的情况，您可以寻求AI的帮助。

???+ note "软件组"
    在安装软件组时，遇到这样的情况，我们建议您直接回车:
    ```
    :: There are 58 members in group gnome:
    :: Repository extra
    1) baobab  2) decibels  3) epiphany  4) gdm  5) gnome-backgrounds  6) gnome-calculator  7) gnome-calendar  8) gnome-characters  9) gnome-clocks  10) gnome-color-manager  11) gnome-connections
    12) gnome-console  13) gnome-contacts  14) gnome-control-center  15) gnome-disk-utility  16) gnome-font-viewer  17) gnome-keyring  18) gnome-logs  19) gnome-maps  20) gnome-menus  21) gnome-music
    22) gnome-remote-desktop  23) gnome-session  24) gnome-settings-daemon  25) gnome-shell  26) gnome-software  27) gnome-system-monitor  28) gnome-text-editor  29) gnome-tour  30) gnome-user-docs
    31) gnome-user-share  32) gnome-weather  33) grilo-plugins  34) gst-thumbnailers  35) gvfs  36) gvfs-afc  37) gvfs-dnssd  38) gvfs-goa  39) gvfs-gphoto2  40) gvfs-mtp  41) gvfs-nfs  42) gvfs-onedrive
    43) gvfs-smb  44) gvfs-wsdd  45) loupe  46) malcontent  47) nautilus  48) orca  49) papers  50) rygel  51) showtime  52) simple-scan  53) snapshot  54) sushi  55) tecla  56) xdg-desktop-portal-gnome
    57) xdg-user-dirs-gtk  58) yelp

    Enter a selection (default=all): 
    ```

## 实践

以下是一些较为常见的pacman指令。

1. `sudo pacman -S` 安装某个软件包（可列举多个）
2. `sudo pacman -Rs` 卸载某个软件包及其依赖（可列举多个）
3. `sudo pacman -Syu` 升级系统软件包（请不要颠倒参数顺序！）
4. `sudo pacman -Scc` 清空包缓存

???+ question "-S, -Syu，这些都是什么意思？"
    在Pacman中，`-S`（Sync，同步）、`-R`（Remove，移除）这些代表的是选项(Options)，可以看作“主操作模式”，而不同的选项后可能会存在不同的“辅助开关”。例如，`-S`的变体`-Syu`或`-S -y -u`中，`-y`代表Refresh（刷新），`-u`代表Sysupgrade（更新所有包），意为：刷新软件源并更新所有包。而在`-R`的变体`-Rus`中 ，`-u`代表的就是Unneeded（跳过仍然被其他包所依赖的软件包），`-s`代表Recursive（递归删除目标包与依赖），意为：递归删除目标包与依赖，并忽略那些被其他软件依赖的包。
    
    并且，部分“辅助开关”被重复时会有不同作用，例如`-Syyuu`，此处的`-yy`表示强制刷新软件源，`-uu`表示在更新的同时允许降级。

    同时，各个“辅助开关”也存在操作顺序的差异。

    要查看各选项含义，您可以运行`sudo pacman --help`，而要查看对应选项下的其他选项，您可以运行`sudo pacman -选项 --help`。

---

不常用指令

1. `sudo pacman -Ss` 搜索某软件包

更详细可以参考[Linux命令手册](https://www.linux-man.cn/linux/command/pacman/)。