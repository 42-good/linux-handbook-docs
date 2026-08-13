# C++

## Windows 的配置灾难

众所周知，在windows上安装VSCode并配置好mingw编译器对于很多新手来说都是一件非常曲折的事情。
因为 Windows 的主要受众是普通人，所以软件管理，编译器配置方面都不如Linux便利。

如果你选择了 Linux ，那么恭喜你将获得一个非常便利而自然的开发环境。
接下来我简单介绍一下如何在 Linux 上跑通一个 简单的 Hello World 以及多文件编译。

## g++ 安装

g++ 编译器是专门用于编译 cpp 代码的(也就是让你写的东西能用机器跑起来)。
安装非常简单，取决于你使用什么包管理器。

- Debian 系(Ubuntu, Mint, Debian)

```bash
sudo apt install g++ -y
```

- 红帽系(Fedora, rhel, rocky)

```bash
sudo dnf install g++ -y
```

- Arch系

```bash
sudo pacman -S g++ -y
```

- 查看版本

```bash
g++ -v
```

参考输出:
❯ g++ -v

```shell
Using built-in specs.
COLLECT_GCC=g++
COLLECT_LTO_WRAPPER=/usr/lib/gcc/x86_64-pc-linux-gnu/16/lto-wrapper
Target: x86_64-pc-linux-gnu
Configured with: ../gcc/configure --enable-languages=ada,c,c++,d,fortran,go,lto,m2,objc,obj-c++,rust,cobol --enable-bootstrap --prefix=/usr --libdir=/usr/lib --libexecdir=/usr/lib --mandir=/usr/share/man --infodi
r=/usr/share/info --with-bugurl=https://gitlab.archlinux.org/archlinux/packaging/packages/gcc/-/issues --with-build-config=bootstrap-lto --with-gcc-major-version-only --with-linker-hash-style=gnu --with-system-zl
ib --enable-cet=auto --enable-checking=release --enable-clocale=gnu --enable-default-pie --enable-default-ssp --enable-gnu-indirect-function --enable-gnu-unique-object --enable-libstdcxx-backtrace --enable-link-s
erialization=1 --enable-linker-build-id --enable-lto --enable-multilib --enable-plugin --enable-shared --enable-threads=posix --disable-fixincludes --disable-libssp --disable-libstdcxx-pch --disable-werror
Thread model: posix
Supported LTO compression algorithms: zlib zstd
gcc version 16.1.1 20260725 (GCC)
```


## 编写一个程序

- 创建一个cpp文件(以cpp为后缀)

```bash
touch hello.cpp
```

- 使用你喜欢的编辑器打开

```bash
vim hello.cpp
# 如果你不会用 vim 就用nano
# nano hello.cpp
```

- 写入下面的内容

```cpp
#include <iostream>

int main() {
    std::cout << "hello world" << std::endl;
    return 0;
}
```

- 保存并退出

- 编译成二进制文件

```bash
g++ hello.cpp -o hello
```

> -o <file>                Place the output into <file>.
这里 -o 表示 output(输出的二进制文件), 后面跟上你起的二进制文件名， 随便叫啥，一般会叫main或者你的程序名。

写法是 g++ 源文件路径 -o 二进制文件。

- 运行程序

```bash
./hello # ./ 表示当前目录， 后面直接跟上文件名， 表示运行该二进制文件
```

这个时候终端会打印 hello world， 恭喜你成功用命令行成功编写并运行了一个C++程序。

现在你已经学会如何使用命令行编译cpp程序了，当然还有各种的编译方式，有各种编译工具，但是入门的话现在这些知识就够了。
祝贺你。
