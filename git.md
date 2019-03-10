# GIT学习
## GIT工作流程
- 克隆Git资源作为工作目录
- 在克隆的资源上添加或修改文件
- 如果其他人修改了，你可以更新资源
- 在提交前查看修改
- 提交修改
- 在修改完成后，如果发现错误，可以撤回提交并再次修改并提交
![Git工作流程](http://www.runoob.com/wp-content/uploads/2015/02/git-process.png)
## Git工作区、暂存区和版本区
> * **工作区：** 就是你在电脑里能看到的目录。
> * **暂存区：** 英文叫tage，或index。一般存放在“.git”目录下的index（.git/index）中，所以我们把暂存区有时也叫作索引（index）。
> * **版本区：** 工作区有一个隐藏目录`.git`，这个不算工作区，而是Git的版本库。
![工作区、版本库中的暂存区和版本库之间的关系](http://www.runoob.com/wp-content/uploads/2015/02/1352126739_7909.jpg)
## Git创建仓库
### git init

Git 使用 git init 命令来初始化一个 Git 仓库，Git 的很多命令都需要在 Git 的仓库中运行，所以 git init 是使用 Git 的第一个命令。在执行完成 git init 命令后，Git 仓库会生成一个 .git 目录，该目录包含了资源的所有元数据，其他的项目目录保持不变（不像 SVN 会在每个子目录生成 .svn 目录，Git 只在仓库的根目录生成 .git 目录）。

----

使用当前目录作为Git仓库，我们只需使它初始化。
```
git init 
```

该命令执行完后会在当前目录生成一个 .git 目录。

---

使用我们指定目录作为Git仓库。
```
git init newrepo
```

初始化后，会在 newrepo 目录下会出现一个名为 .git 的目录，所有 Git 需要的数据和资源都存放在这个目录中。

---

如果当前目录下有几个文件想要纳入版本控制，需要先用 git add 命令告诉 Git 开始对这些文件进行跟踪，然后提交：
```
$ git add *.c
$ git add README
$ git commit -m '初始化项目版本'
```

以上命令将目录下以 .c 结尾及 README 文件提交到仓库中。

---
### git clone


