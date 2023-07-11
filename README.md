# 学习指南

欢迎来到学习Git的仓库！这个仓库旨在帮助您掌握Git版本控制系统的基本概念和常用操作。无论您是初学者还是有一些经验的开发者，这里都有一些资源和示例可以帮助您深入学习和应用Git。

## 背景介绍

- **Git** 作为免费的开源分布式版本控制系统，旨在高效地处理各种或大或小的项目；

- **Git** 易于学习，占地面积小，性能极快。它具有廉价的本地库，方便的暂存区域和多个工作流分支等特性。其性能优于      等版本控制工具；

- **Git** 已成为开源和商业软件开发中最受欢迎的版本控制系统之一。它具有强大的功能和灵活性，可以适应各种规模和类型的项目。同时，Git的学习曲线可能有些陡峭，但一旦掌握了基本概念和常用命令，它将成为您日常开发工作中的有力工具。

- **Git** 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持。

- 目前在公司开发中我们都是使用Git来管理项目的，所以接下来我们会重点学习Git的各种用法；

## 版本控制

- 版本控制是一种记录一个或若干文件内容变化，以便将来查阅特定版本修订情况的系统。

- 其最重要的是可以记录文件修改历史记录，从而让用户查看历史版本，方便版本切换。

- 简单来说，版本控制在软件开发中，可以帮助程序员进行代码的追踪、维护、控制等系列操作。

## 类型（版本控制工具）

- 本地版本控制系统
- 集中化的版本控制系统（集中式版本控制 工具）
- 分布式版本控制系统 工具

## 安装

- Windows
  - <https://git-scm.com/download/win>
- macOS
  - <https://git-scm.com/download/mac>
- Linux/Unix
  - <https://git-scm.com/download/linux>

## Bash – CMD – GUI 区别

- Bash，Unix shell 的一种，Linux 与 Mac OS X 都将它作为默认 shell。
  - Git Bash 就是一个 shell，是 Windows 下的命令行工具，可以执行 Linux命令；
  - Git Bash 是基于 CMD 的，在 CMD 的基础上增添一些新的命令与功能；
  - 所以建议在使用的时候，用 Bash 更加方便；
- Git CMD
  - 命令行提示符（CMD）是 Windows 操作系统上的命令行解释程序；
  - 当你在 Windows 上安装 git 并且习惯使用命令行时，可以使用 cmd 来运行 git 命令；
- Git GUI
  - 基本上针对那些不喜欢黑屏（即命令行）编码的人；
  - 它提供了一个图形用户界面来运行 git 命令；

## 工作机制

- 版本库（仓库repository）
- 工作区（Working Directory）
- 暂存区（stage/index）
- 本地库（）

## 文件状态

- 已提交
- 已修改
- 已暂存

## 工作流

你的本地仓库由 git 维护的三棵“树”组成。第一个是你的 工作目录，它持有实际文件；第二个是 暂存区（Index），它像个缓存区域，临时保存你的改动；最后是 HEAD，它指向你最后一次提交的结果。

![Alt text](trees.png)

## 安装配置

- 设置用户签名

```shell
git config --global user.name （用户名）
git config --global user.email （邮箱）
```

说明：签名的作用是区分不同操作者身份。用户的签名信息在每一个版本的提交信息中能够看到，以此确认本次提交是谁做的。git首次安装必须设置用户签名，否则无法提交代码。

## 验证

控制面板   用户账户

ssh密钥

## git忽略文件

- 一般我们总会有些文件无需纳入 Git 的管理，也不希望它们总出现在未跟踪文件列表。

  - 通常都是些自动生成的文件，比如日志文件，或者编译过程中创建的临时文件等；
  - 我们可以创建一个名为 .gitignore 的文件，列出要忽略的文件的模式；

- 在实际开发中，这个文件通常不需要手动创建，在必须的时候添加自己的忽略内容即可；

- 比如右侧是创建的Vue项目自动创建的忽略文件：

  - 包括一些不需要提交的文件、文件夹；
  - 包括本地环境变量文件；
  - 包括一些日志文件；
  - 包括一些编辑器自动生成的文件；

## 远程仓库

代码托管中心是基于网络服务器的远程代码仓库，一般我们简单称为远程库

github

gitee

gitlab

## 实用小贴士

内建的图形化 git：
gitk
彩色的 git 输出：
git config color.ui true
显示历史记录时，每个提交的信息只显示一行：
git config format.pretty oneline
交互式添加文件到暂存区：
git add -i

## 链接与资源

图形化客户端
GitX (L) (OSX, 开源软件)
Tower (OSX)
Source Tree (OSX, 免费)
GitHub for Mac (OSX, 免费)
GitBox (OSX, App Store)
指南和手册
Git 社区参考书
专业 Git
像 git 那样思考
GitHub 帮助
图解 Git

尚硅谷

黑马程序员

Git官方网站

<https://github.com/rogerdudler/git-guide>

## 作者

- 👀 I’m interested in ...
- 💞️ I’m looking to collaborate on ...

- 👋 Hi, I’m Pursion
- 🌱 I’m currently learning Git
- 📫 How to reach me 2744599315
