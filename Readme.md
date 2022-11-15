## 参考链接
[Git教程](https://www.yiibai.com/git)

## 学习git操作

### 最简单的一个操作
1. 首先在github创建一个空项目
2. 本地git clone https://github.com/xyxdaily/learngit.git
3. cd到learngit项目内
4. 写一个Readme.md
5. git add --all
6. git commit -m "first commit Readme.md"
```
[main (root-commit) 9681c0f] first commit Readme.md
 Committer: xxxxxxxxxxxxxxxxxxxx
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 13 insertions(+)
 create mode 100644 Readme.md
```
这里可以选择配置或者不配置
7. git push
第一次push的时候会要登录github，然后就可以顺利成功的push了。后续有文件更新的话就只要三步就ok.
```
git add --all
git commit -m "message content"
git push
```

### help命令
可以先直接运行git查看有哪些命令，然后可以通过git help command就会自动弹出本地的帮助页面了。
比如`git help clone`
本地的地址为`file:///C:/Users/amdin/AppData/Local/Programs/Git/mingw64/share/doc/git-doc/git-clone.html`

### 分支学习
[Git管理分支](https://www.yiibai.com/git/git_managing_branches.html)
分支操作允许创建另一路线/方向上开发。我们可以使用这个操作将开发过程分为两个不同的方向。

#### 默认分支
默认分支为main
使用`git branch`即可查看所有分支

#### 创建分支
使用`git branch name`即可创建分支，分支名字为name
比如创建分支new_main，使用命令`git branch new_main`

#### 查看分支
```
git branch 
git branch -a
```

#### 删除分支
先创建一个测试分支`git branch for_delete`
查看所有分支`git branch`为
```
  for_delete
* main
  new_main
```
然后删除分支`git branch -D for_delete`
```
Deleted branch for_delete (was 3f17be6).
```

查看分支
```
* main
  new_main
```

#### 切换分支
使用命令checkout即可切换分支
`git checkout new_main`
切换完毕后
```
  main
* new_main
```

使用-b命令，如果没有该分支则会先创建再切换分支
`git checkout -b new_main2`
```
  main
  new_main
* new_main2
```

### 分支小例子
这里我们选择new_main，然后把新的Readme.md同步到该分支
要推送分支的话，需要使用`git push --set-upstream origin new_main`,当然可以先git push看看报错与提示
```
fatal: The current branch new_main has no upstream branch.
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin new_main
```
```
git add -all
git commit -m "update new_main Readme.md"
git push --set-upstream origin new_main
```

### 合并分支到main
使用命令`git merge origin/new_main`
