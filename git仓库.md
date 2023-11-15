# Git

## 环境配置

git gui：git提供的图形界面工具

git bash：git提供的命令行工具

#### ①基本配置

1.打开git bash

2.设置用户信息

   git config--global user.name"yu"

   git config--global user.email"1977624121@qq.com"

#### ②设置别名

有些常用指令参数多 可设置别名

1.用户目录中创建.bashrc文件

2.在bashrc文件下输入

```shell
#用于输出git提交日志
alias git-log='git log --pretty=oneline --a11 --graph --abbrev-commit'
#用于输出当前目录所有文件信息
alias 11='1s -a1'
```

3.打开git bash,执行source ~/.bashrc

#### ③解决乱码

1.打开git bash执行

```
git config --global core.quotepath false
```

2.${git_home}/etc/bash.bashrc  文件最后加入以下两行

```
export LANG="zh_CN.UTF-8"
export LC_ALL="zh_CN.UTF-8"
```

## 获取本地仓库

1.在电脑任意位置创建空目录作为本地git仓库

2.进入目录，打开git bash窗口

3.执行命令git init

4.出现.git即为成功

#### 基础操作指令

git工作目录下对文件修改会随着执行git命令而发生变化

1.git add          (工作区-->暂存区)

2.git commit   (暂存区-->本地仓库)

ps.unstaged未暂存(修改已有文件)；untracked未跟踪(新创建一个文件)

```shell
git init//初始化git仓库
touch (文件名)//创建文件
git status//查看文件修改状态
ls//列出文件夹下面所有文件
git log//查看提交日志
vi (文件名)//修改已有文件
git add .//将所有文件放入暂存区
git commit -m//提交暂存区到常用仓库
git log[option]
①--all 显示所有分支
②--pretty=oneline  将提交信息显示为一行
③--abbrev-commit  使得输出的commitID更简短
④--graph  以图的形式显示
git reset --hard commitID//版本回退
ps.commitID可以使用git-log或git log查看
git reflog//查看删除记录
```

3. 添加文件至忽略列表 可创建后标为. gitignore的文件，并进行修改

### 分支

##### 查看分支

git branch

##### 创建分支

git branch 分支名

##### 切换分支 

git checkout 分支名 (切换到新的git checkout -b 分支名)

##### 将一个分支上的提交合并到另一个分支 

git merge

(Esc+ :wq保存并退出；:q直接退出；:w保存)

##### 删除分支(不能删除当前分支，只能删除其他分支)

git branch -d b1 删除分支时，需要做各种检查

git branch -D b1 不做任何检查，强制删除

##### 解决冲突

1.处理文件冲突的地方

2.git add .

3.git commit

##### 原则和流程

1.master(生产)分支

  线上分支，主分支，中小规模项目

2.develop(开发)分支

  主要开发分支 一般需合并到master

3.feature/xxxx分支

  合并到develop 后可删除

4.hotfix/xxxx分支

  修复bug后合并

## Git远程仓库

1.生成SSH公钥

   ssh-keygen-t rsa

   不断回车（若公钥已存在，则自动覆盖）

2.获取公钥

   cat~/.ssh/id_rsa.pub

   贴在ssh公钥中

   验证是否成功:ssh-T git@gitee.com

##### 添加远程仓库

  git remote add <远端名称> <仓库路径>

​     远端名称：默认origin

​     仓库路径：从远端服务器获取此URL

##### 查看远端仓库

   git remote

##### 推送到远程仓库

   git push [-f] [--set-upstream] [远端名称[本地分支名] [:远端分支名] ]

​     如果远程分支名与本地分支名相同，可只写本地分支

​       · git push orgin master

​     -f表示强制覆盖

​     --set-upstream  推送到远端的同时并且建立起和远端分支的关联关系

​      · git push --set-upstream orgin master(可省略成-u)

​      ·若已建立 则可省略分支名和远端名 直接用git push

##### 查看关联关系

   git branch -vv

##### 从远程仓库克隆

   若已经有远程仓库，可以克隆到本地

   git clone<仓库路径>[本地目录]

​     ·本地目录可省略，会自动生成一个目录

##### 从远程仓库抓取和拉取

   抓取: git fetch [remote name] [branch name]

​     仅将更新的抓取到本地，不合并

   拉取: git pull [remote name] [branch name]

​     抓取到本地并合并(=merge)

##### 解决合并冲突

   先拉取后等同于分支中解决冲突方法
