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