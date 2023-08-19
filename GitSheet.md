## 创建仓库 

### 语法

```shell
git init
```

### 说明

```shell
# 初始化本地库 创建版本库（廖雪峰） （获取GIT仓库）(创建新仓库)
# 创建新文件夹，打开，然后执行git init以创建新的 git 仓库。
```

## 克隆仓库

```shell
git clone

# 检出仓库
# 执行如下命令以创建一个本地仓库的克隆版本：
# git clone /path/to/repository
# 如果是远端服务器上的仓库，你的命令会是这个样子：
# git clone username@host:/path/to/repository
```

## 将文件添加到仓库（添加暂存区）

```shell
git add 文件名
```
你可以提出更改（把它们添加到暂存区），使用如下命令：
git add <filename>
git add *
这是 git 基本工作流程的第一步；使用如下命令以实际提交改动：
git commit -m "代码提交信息"
现在，你的改动已经提交到了 HEAD，但是还没到你的远端仓库。

## 将文件提交到仓库（提交本地库）

```shell
git commit -m "日志信息"
```

本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。
嫌麻烦不想输入-m "xxx"亦行

## 查看仓库状态（查看本地库状态）

```shell
git status
```

## 查看文件修改内容

```shell
git diff
```

使用"q"退出

（版本回退）（历史版本）

## 查看历史记录（查看历史版本）

```shell
git log（详细）
git reflog（简介）
```

log
如果你想了解本地仓库的历史记录，最简单的命令就是使用:
git log
你可以添加一些参数来修改他的输出，从而得到自己想要的结果。 只看某一个人的提交记录:
git log --author=bob
一个压缩后的每一条提交记录只占一行的输出:
git log --pretty=oneline
或者你想通过 ASCII 艺术的树形结构来展示所有的分支, 每个分支都标示了他的名字和标签:
git log --graph --oneline --decorate --all
看看哪些文件改变了:
git log --name-status
这些只是你可以使用的参数中很小的一部分。更多的信息，参考：
git log --help
该命令可以告诉我们历史记录

## 版本回退（版本穿梭）

```shell
git reset --hard HEAD^（或版本号）

# 在Git中，用HEAD表示当前版本
```

回退版本后，亦可使用该命令回到未来版本

## 命令记录

```shell
git reflog
```

## 撤销修改

```shell
git checkout -- file
```

## 删除文件

```shell
git rm 
```

## 克隆文件

```shell
git clone
```

## 分支

在版本控制过程中，同时推进多个任务，为每个任务，我们就可以创建每个任务的单独分支。使得分支意味着程序员可以把自己的工作从主线任务上分离开来，开发自己分支的时候，不会影响主线分支的运行。

分支是用来将特性开发绝缘开来的。在你创建仓库的时候，master 是“默认的”分支。在其他分支上进行开发，完成后再将它们合并到主分支上。

好处

同时并行推进多个功能开发，提高开发效率

各个分支在开发过程中，如果某一个分支开发失败，不会对其他分支有任何影响。失败的分支删除重新开始即可。

创建一个叫做“feature_x”的分支，并切换过去：
git checkout -b feature_x
切换回主分支：
git checkout master
再把新建的分支删掉：
git branch -d feature_x
除非你将分支推送到远端仓库，不然该分支就是 不为他人所见的：
git push origin <branch>

更新与合并
要更新你的本地仓库至最新改动，执行：
git pull
以在你的工作目录中 获取（fetch） 并 合并（merge） 远端的改动。
要合并其他分支到你的当前分支（例如 master），执行：
git merge <branch>
在这两种情况下，git 都会尝试去自动合并改动。遗憾的是，这可能并非每次都成功，并可能出现冲突（conflicts）。 这时候就需要你修改这些文件来手动合并这些冲突（conflicts）。改完之后，你需要执行如下命令以将它们标记为合并成功：
git add <filename>
在合并改动之前，你可以使用如下命令预览差异：
git diff <source_branch> <target_branch>

## 创建分支

```shell
git branch 分支名
```

## 查看分支

```linux
git branch -v
```

## 切换分支

```linux
git checkout 分支名
```

## 把指定的分支合并到当前分支上（合并分支）

```linux
git merge 分支名
```

## 冲突合并

冲突产生的原因

合并分支时，两个分支在同一个文件的同一个位置有两个完全不同的修改。git无法替代我们决定使用哪一个，必须人为决定新代码内容。

合并后，当前分支改变，指定分支不变

## 团队协作机制（团队内协作）（团队外协作）

推送改动
你的改动现在已经在本地仓库的 HEAD 中了。执行如下命令以将这些改动提交到远端仓库：
git push origin master
可以把 master 换成你想要推送的任何分支。

如果你还没有克隆现有仓库，并欲将你的仓库连接到某个远程服务器，你可以使用如下命令添加：
git remote add origin <server>
如此你就能够将你的改动推送到所添加的服务器上去了。

## 创建远程仓库别名(Remote Repository)

```linux
git remote -v 查看当前所有远程地址别名
```

```linux
git remote add 别名 远程地址
```

## 推送本地分支上的内容到远程仓库

```linux
git push 别名 分支
```

## 将远程仓库的内容克隆到本地

```linux
git clone 远程地址
```

## 将远程仓库对于分支最新内容拉下来后与当前本地分支直接合并

```linux
git pull 远程库地址别名 远程分支名
```

git branch -M main
git push -u origin main

## 标签

为软件发布创建标签是推荐的。这个概念早已存在，在 SVN 中也有。你可以执行如下命令创建一个叫做 1.0.0 的标签：
git tag 1.0.0 1b2e1d63ff
1b2e1d63ff 是你想要标记的提交 ID 的前 10 位字符。可以使用下列命令获取提交 ID：
git log
你也可以使用少一点的提交 ID 前几位，只要它的指向具有唯一性。

```Linux
git tag
```

创建

```Linux

```

删除

```Linux

```

## 替换本地改动

假如你操作失误（当然，这最好永远不要发生），你可以使用如下命令替换掉本地改动：
git checkout -- <filename>
此命令会使用 HEAD 中的最新内容替换掉你的工作目录中的文件。已添加到暂存区的改动以及新文件都不会受到影响。

假如你想丢弃你在本地的所有改动与提交，可以到服务器上获取最新的版本历史，并将你本地主分支指向它：
git fetch origin
git reset --hard origin/master