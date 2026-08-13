# Emcas

![emacs](https://www.gnu.org/software/emacs/images/emacs.png)

[官方文档](https://www.gnu.org/software/emacs/manual/emacs.html)

[官网](https://www.gnu.org/software/emacs/)

**Emacs的配置文件位于`~/.emacs.d/`或`~/.config/emacs`(更老的Emacs版本使用`~/.emacs`作为配置目录),其名称为init.el,使用Elisp作为配置语言**

## 梗概

Emacs是一个[自由](https://www.gnu.org/philosophy/free-sw.html)的编辑器,采用[GPL-v3](https://www.gnu.org/licenses/gpl-3.0.en.html)发布,采用Elisp作为配置语言,Emacs功能强大(包括但不限于发邮件,使用irc聊天,阅读新闻和RSS订阅,玩俄罗斯方块),常被与vim/nvim比较,最早由Richard Stallman编写发布,Emacs是[自由软件运动](https://www.gnu.org/)的一部分

**注:本文档使用Emacs编辑**

## 安装

- Debian系: `sudo apt install emacs`
- 红帽系: `sudo dnf install emacs`
- Arch系: `sudo pacman -S emacs`

## 使用(默认快捷键)

**Emacs的使用高度依赖C键(及Control键)和Meta键(及Alt键),下文用C与M代替**

**由于Emacs的功能关于繁杂无法将所有快捷键列出,强烈建议您阅读官方文档**

- C-x C-c 退出Emacs
- M-x 输入命令
- C-x C-s 保存文件
- C-s 搜索关键词
- C-p/n/b/f 使光标上下左右的移动
- C-a/e 移动到行头或行尾
- M-</> 移动到文件头或文件尾
- C-k 删除光标后面的所有文本
- C-/ 撤销操作(C-x u和C-_也可已,详情见官方文档9.4)
- C-x C-f 跳转到另一个文件(旧文件会被放入一个buffer中)
- C-x b 切换到另一个Buffer
- C-x C-b 打开Buffer列表(?获得帮助)
- C-x o 切换到另一个Window
- C-x 0 关闭Window
- C-x k 关闭一个Buffer
- C-h C-f Emacs常见问题解答
- C-h r 官方手册(需要安装info)
- C-h t 官方快速指南 
## 配置

**Emacs的配置文件位于~/.emacs.d/或~/.config/emacs(更老的Emacs版本使用~/.emacs作为配置目录),其名称为init.el,使用Elisp作为配置语言**

**由于Emacs的配置过于纷杂繁复,不适合Linux新手,所以只做文档与视频的推荐**

1.[Emacs轻奢之路](https://www.bilibili.com/video/BV1T64y1R7EL/)
2.[21天学会Emacs 2022年版本](https://www.bilibili.com/video/BV12P4y1j7EL/)
3.[Emacs高手修炼手册](https://www.bilibili.com/video/BV13g4y167Zn/)
4.[专业 Emacs 入门教程](https://www.zhihu.com/column/c_1440829147212279808)

## 尾言

Emacs的上手并不简单,但当您上手并习惯它后它将是您最好的编程伙伴,在您上手后我推荐您尝试使用[Org-mode](https://orgmode.org/)编写文档管理日程安排,也推荐您使用Emacs的更多功能,愿Emacs可以成为您一生的编辑器。

## Emacs相关网站

- [Emacs-china](https://emacs-china.org/)
- [Emacs官网](https://www.gnu.org/software/emacs/)