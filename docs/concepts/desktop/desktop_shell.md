# 桌面外壳

英文: Desktop Shell

## 概述

狭义来看，桌面外壳是指在**平铺窗口管理器**中，提供用户界面的应用套件。

???+ note "常见的桌面外壳"
    - DMS (Dank Material Shell): 目前最广为人知的桌面外壳，采用Material You设计理念，现代而优雅。
    ![DMS](https://danklinux.com/img/desktoplight.png)
    ??? info "安装教程"
        我们建议您使用[DankInstall](https://danklinux.com/docs/dankinstall)，即其一键脚本。该脚本不仅提供了桌面外壳的安装，还内置了Hyprland/Niri的安装功能，省心省力。

        ```bash
        sudo -v && curl -fsSL https://install.danklinux.com | sh -s -- \
        -c hyprland -t kitty --include-deps dms-greeter --replace-configs-all -y
        ```

    - Noctalia: 操作顺滑，可自定义性高。
    ![Noctalia](https://noctalia.dev/_app/immutable/assets/lemmy.D-o_kYQM.webp)
        [安装教程（英文）](https://docs.noctalia.dev/v5/getting-started/installation)
    ...