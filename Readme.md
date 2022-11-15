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
7. git push