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

3. **git add**添加变动文件

   git add <file>

4. **git commit**提交到版本库

   git commit -m <message>

   ``` shell
   $ git commit -m "提交说明"
   [master (root-commit) eaadf4e] wrote a readme file
    1 file changed, 2 insertions(+)
    create mode 100644 readme.txt
   ```


5. **git log**查看提交记录
6. 再次修改后,可继续使用**git add**以及**git commit**提交变更

* 一个**git commit**可以对应多个**git add**
* 未做add的新文件不会被**git diff**识别
* add后修改的内容,不会被commit提交(除非再次add)