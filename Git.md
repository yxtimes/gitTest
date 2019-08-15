## 安装Git

安装完成后，输入自己的名称和邮箱地址

``` shell
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

## 创建版本库

1. 选择合适的目录

   ``` shell
   $ mkdir learngit
   ```

2. **git init**创建版本库

   ``` shell
   $ git init
   Initialized empty Git repository in /Users/michael/learngit/.git/
   ```

## 添加跟踪(add)及提交(commit)

1. **git add**添加变动文件

   git add <file>

2. **git commit**提交到版本库

   git commit -m <message>

   ``` shell
   $ git commit -m "提交说明"
   [master (root-commit) eaadf4e] wrote a readme file
    1 file changed, 2 insertions(+)
    create mode 100644 readme.txt
   ```

3. **git log**查看提交记录
4. 再次修改后,可继续使用**git add**以及**git commit**提交变更
   - 一个**git commit**可以对应多个**git add**
   - 未做add的新文件不会被**git diff**识别
   - add后修改的内容,不会被commit提交(除非再次add)

## 一些小说明

### 获取(fetch)和拉取(pull)的区别

- git fetch 相当于是从远程获取最新到本地，不会自动merge，如下指令：

``` shell
git fetch orgin master //将远程仓库的master分支下载到本地当前branch中
git log -p master  ..origin/master //比较本地的master分支和origin/master分支的差别
git merge origin/master //进行合并
```

也可以用以下指令：

``` shell
git fetch origin master:tmp //从远程仓库master分支获取最新，在本地建立tmp分支
git diff tmp //將當前分支和tmp進行對比
git merge tmp //合并tmp分支到当前分支
```


- git pull：相当于是从远程获取最新版本并merge到本地

``` shell
git pull origin master
```

