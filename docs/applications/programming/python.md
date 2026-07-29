# Python

## 安装 Python

Linux 上装Python还是非常轻松的，因为不用装，大部分发行版自带。

Linux 里面一般都是 `python3`。
如果你想要用 `python` 这个命令， 可以装一个 `python-is-python3`, 来用软链接骗过操作系统(开个玩笑)。

- Debian: `sudo apt install python-is-python3 -y`
- Fedora: `sudo dnf install python-is-python3 -y`

## 编写第一个脚本

- 创建一个脚本

```bash
touch hello.py
```

- 写入内容

```bash
echo "print('hello python')" > hello.py
```

- 查看内容

```bash
cat hello.py

# 会输出
# print('hello python')
```

## 运行

有很多Windows来的同志不知道怎么运行，但实际上非常简单。

用法:

```bash
# python <要运行的脚本路径>

python hello.py
```

这样你就成功运行起 Python 脚本了。
实际上就是给 Python 指定需要运行的文件， 就这么简单。

恭喜你在Linux上成功运行了Python脚本。

## 编辑器

- 如果你使用WSL, 推荐使用 VSCode 的 WSL 插件来连接写代码, 当然勇敢牛牛可以尝试 LazyVim 写代码
- 如果你使用原生 Linux, 还是这两种推荐haha

VSCode 资料很多， 我也用的比较少，可以直接上Bilibili搜索VSCode Python环境搭建
[LazyVim入坑视频](https://www.bilibili.com/video/BV1TJCvYFE2T?t=286.5)

## 库

Python拥有规模庞大的PyPi库。通常，我们使用`pip`进行安装。但在Linux下，`pip`不一定会随着Python预装，因此需要使用包管理器安装。

- Debian: `sudo apt install python3-pip`
- Fedora: `sudo dnf install python3-pip`
- Arch: `sudo pacman -S python-pip`

!!! warning "系统依赖"
    使用Pip安装部分库时，可能会出现如下警告:
    ```
    error: externally-managed-environment

    × This environment is externally managed
    ╰─> To install Python packages system-wide, try 'pacman -S
        python-xyz', where xyz is the package you are trying to
        install.
        
        If you wish to install a non-Arch-packaged Python package,
        create a virtual environment using 'python -m venv path/to/venv'.
        Then use path/to/venv/bin/python and path/to/venv/bin/pip.
        
        If you wish to install a non-Arch packaged Python application,
        it may be easiest to use 'pipx install xyz', which will manage a
        virtual environment for you. Make sure you have python-pipx
        installed via pacman.

    note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
    hint: See PEP 668 for the detailed specification.
    ```
    由于系统的部分组件依赖Python的依赖，因而外来库可能破坏系统本身的依赖关系。
    
    这个时候，我们建议您使用`venv`创建虚拟环境，或者寻找发行版的软件源是否有对应的库可供安装（一般包名为`python3-库`或`python-库`）。