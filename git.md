# 一 本地仓库

* git 只能跟踪文本文件的改动, 而图片、视频这些二进制文件，虽然也能由版本控制系统管理，但没法跟踪文件的变化，只能把二进制文件每次改动串起来
* Microsoft的Word格式是二进制格式，因此，版本控制系统是没法跟踪Word文件的改动的
* 用`HEAD`表示当前版本,上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个`^`比较容易数不过来，所以写成`HEAD~100`

* ![image-20230610170102740](./git.assets/image-20230610170102740.png)

     * Changes not staged for commit:  //改之后未add
     * Untracked files:               //新加的文件未add    
     





`.gitignore` 文件使用简单的语法规则来指定要忽略的文件和目录。下面是一些常见的语法规则：

1. 使用 `#` 开头的行将被视为注释，并被忽略。
2. 可以使用斜杠 `/` 来指定文件或目录的路径。例如，`build/` 表示要忽略根目录下的 `build` 目录及其所有内容。
3. 使用 `*` 来匹配零个或多个字符。例如，`*.txt` 表示匹配任何以 `.txt` 结尾的文件。
4. 使用 `!` 来否定排除规则，允许包含特定文件或目录。例如，`!config.ini` 表示不忽略根目录下的 `config.ini` 文件。
5. 使用 `/` 开头的斜杠表示匹配根目录，否则将匹配任何位置。例如，`/build/` 表示匹配根目录下的 `build` 目录，而 `build/` 则会匹配任何位置的 `build` 目录。
6. 可以使用 `**` 模式匹配任意层级的目录。例如，`logs/**/*.log` 表示匹配任意层级的 `logs` 目录下的所有 `.log` 文件。
7. 使用问号 `?` 来匹配单个字符。例如，`log?.txt` 表示匹配 `log1.txt`、`log2.txt` 等文件。
8. 可以使用方括号 `[ ]` 来匹配指定字符范围内的任意一个字符。例如，`[abc].txt` 表示匹配 `a.txt`、`b.txt` 或 `c.txt` 文件。
9. 使用叹号 `!` 来排除特定模式。例如，`*.txt` 表示忽略所有 `.txt` 文件，而 `!important.txt` 表示除了 `important.txt` 文件外，其他 `.txt` 文件将被忽略。













## 1 git init 

初始化一个仓库

## 2 git add .

将修改从工作区提交到暂存区

## 3 git commit -m ""

暂存区到本地仓库，提交一次是一个版本

 1 file changed, 2 insertions(+)   //  1个文件被改动；`2 insertions`：插入了两行内容 。 

## 4 git status

查看工作，暂存区的状态  ,  列出变动的且未提交的 

## 5 gitlog 
查看提交记录

## 6 git reset --hard commitID
版本回退，切换到指定版本

## 7 git reflog
可以查看删除的提交记录，防止回退之后找不到比较新的提交

## 8 touch .gitignore 
添加忽视规则（不纳入git管理的文件）



## 9  git diff

查看具体修改了什么内容   ， 不用git add



## 10 git checkout -- file  

让这个文件回到最近一次`git commit`或`git add`时的状态。

11 git rm test.txt

rm test.txt  之后想在版本库里面也删了 ，删除版本库中的文件





# 二  分支
## 1 git branch
查看本地分支

## 2 git branch dev01
新建本地分支

## 3 git checkout dev01  
切换分支



``` 
git checkout -b dev 创建并切换
相当于
git branch dev
git checkout dev

///
git switch -c dev  创建并切换到新的dev分支
git switch master  切换到已有的master分支
```

## 4 git mergin dev01
将dev01 合并到当前分支 如果当前是master，则将dev01合并到master 

``` 
Fast-forward 快进模式  直接把master指向dev的当前提交
```


## 5 git branch -d dev01 
删除分支（删除前，检查改动是否提交）
git branch -D dev01
删除分支（强制删除，不做任何检查）

## 6 冲突
合并两个分支的时候，如果两分支修改了同一行，则冲突，需要手动去除冲突
之后add commit





## 7--no-ff`方式的`git merge   // 禁用Fast forward

## git merge --no-ff -m "merge with no-ff" dev

因为本次合并要创建一个新的commit，所以加上`-m`参数，把commit描述写进去。

```
*   e1e9c68 (HEAD -> master) merge with no-ff
|\  
| * f52c633 (dev) add merge
|/  
*   cf810e4 conflict fixed
```

合并分支时，加上`--no-ff`参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而`fast forward`合并就看不出来曾经做过合并。



# 三 远程仓库



## 1 git  remote  add 远端名称 远端地址
比如 git  remote add  origin git@gitee:rzk/test.git    origin 远端名称



## 2 git remote 
查看远程仓库

## 3 git push -f --set-upstream 远端名称 本地分支名：远端分支名
如 git push -f --set-upstream origin master:master 

​     git push  -u origin master:main

## 4 git branch -vv 
查看本地与远程的绑定关系

 ## 4 git remote rm origin

如果添加的时候地址写错了，或者就是想删除远程库，可以用`git remote rm <name>`命令。

## 5 git clone 仓库路径 本地路径

## 6 git fetch [remote name] [branch name ]
git fetch origin master , 并且只是抓取到本地，不与本地合并，要与git mergin 配合

## 7 git pull [remote name] [branch name ]
抓取+合并

## 8 冲突
A　B两用户同时修改同一文件同一位置，Ａ推到远程之后，Ｂ也想推远程
解决：１　 Ｂ先拉取 pull ,解决冲突（冲突在B本地解决）
            2       B 往上推
            3       A 也要再次拉取合并

