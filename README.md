## 安装配置

### 安装：[链接](https://git-scm.com/)

### 配置

- 设置用户签名

```shell
git config --global user.name（用户名）
git config --global user.email（邮箱）

# 说明：签名的作用是区分不同操作者身份；
# 用户的签名信息在每一个版本的提交信息中能够看到，以此确认本次提交是谁做的；
# Git首次安装必须设置用户签名，否则无法提交代码。
```

## Bash – CMD – GUI 区别

### Git CMD

- 命令行提示符（CMD）是 Windows 操作系统上的命令行解释程序；
- 当你在 Windows 上安装 git 并且习惯使用命令行时，可以使用 cmd 来运行 git 命令；

### Git GUI

- 基本上针对那些不喜欢黑屏（即命令行）编码的人；
- 它提供了一个图形用户界面来运行 git 命令；

### Git Bash

- Unix shell 的一种，Linux 与 Mac OS X 都将它作为默认 shell
- Git Bash 就是一个 shell，是 Windows 下的命令行工具，可以执行 Linux命令；
- Git Bash 是基于 CMD 的，在 CMD 的基础上增添一些新的命令与功能；
- 所以建议在使用的时候，用 Bash 更加方便；

### Git FAQs

### Git Release Notes

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

## 验证

控制面板   用户账户

ssh密钥

## Git 忽略文件

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

- github
  - 代码托管中心是基于网络服务器的远程代码仓库，一般我们简单称为远程库
- gitee
- gitlab

## 学习资源

- 尚硅谷
- 黑马程序员
- Git官方网站
- [简明指南](https://github.com/rogerdudler/git-guide)

## 贡献指南

## 联系方式

- 作者：安振辉
- 邮箱：<2744599315@qq.com>
