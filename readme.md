# about learnGit

LearnGit is a project where I learn how to use git.
Here I will make bunch of notes.

## about git bash

Git bash uses commands which is used in linux system

### directory

`mkdir example`	make a directory named "example"

### file

`touch example.md`	a new file named example.md
`vi example.md`		edit the file named example.md

# git bash commands

## 简明版

Git管理的文件分为：工作区，版本库
版本库又分为暂存区stage和暂存区分支master(仓库)

工作区>>>>暂存区>>>>仓库

git add把文件从工作区>>>>暂存区，git commit把文件从暂存区>>>>仓库，

git diff查看工作区和暂存区差异，

git diff --cached查看暂存区和仓库差异，

git diff HEAD 查看工作区和仓库的差异，

git add的反向命令git checkout，撤销工作区修改，即把暂存区最新版本转移到工作区，

git commit的反向命令git reset HEAD，就是把仓库最新版本转移到暂存区。

### basics

`git init`
`git add <file>`
`git commit -m <message>`
`git status`
`git diff`	show the different between commits

### 版本回退

`git log`	查看最近到最远的三个commit

`git reset --hard HEAD^`	硬回退到上一个
`git reset --hard HEAD^^^`	硬回退到上上上个
`git reset --hard HEAD~100`	退100个
`git reset --hard 1094ad`	恢复到序号所在commit

`git reflog`	refer log 展示日志

### 撤销修改

`git checkout -- <file>`	暂存区覆盖工作区

`git restore --worktree <file>`	暂存区覆盖工作区
`git restore --staged <file>`	master覆盖暂存区
