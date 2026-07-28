# 在 Linux 上运行第一个 Python 程序

## 安装 Python

Linux 上装Python还是非常轻松的
因为不用装，自带

Linux 里面一般都是 python3
如果你想要用 python 这个命令， 可以装一个 python-is-python3, 来用软链接骗过操作系统(开个玩笑)

```bash
sudo apt install python-is-python3 -y

# 如果你是 rhel 系列
# sudo dnf install python-is-python3 -y
```

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

有很多windows来的同志不知道怎么运行，但实际上非常简单

用法:

```bash
# python <要运行的脚本路径>

python hello.py
```

这样你就成功运行起python脚本了
实际上就是给 python 指定需要运行的文件， 就这么简单

恭喜你在linux上成功运行了 python 脚本

## 编辑器

- 如果你使用wsl, 推荐使用vscode 的 wsl 插件来连接写代码, 当然勇敢牛牛可以尝试 lazyvim 写代码
- 如果你使用原生 Linux, 还是这两种推荐haha

vscode 资料很多， 我也用的比较少，可以直接上bilibili搜索vscode python环境搭建
[lazyvim入坑视频](https://www.bilibili.com/video/BV1TJCvYFE2T?t=286.5)
