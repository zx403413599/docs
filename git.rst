
----

安装
====

sudo apt-get install git

----

:data-scale: 2

:data-rotate-z: -90

:data-x: r2000

:data-y: r2000

创建版本库
===========

* mkdir learngit创建文件夹

* cd learngit

* git init  把这个目录变成Git可以管理的仓库

* git add readme.txt  添加文件

* git commit -m "wrote a readme file" 告诉git 发生了什么变化

* git status 掌握git工作间状态

* git diff readme.txt  查看修改情况

* git rm ––cached file删除暂存区的文件

* 创建.gitignore   每一行写上需要忽略的文件  可以使用通配符。

----

:data-scale: 2

:data-rotate-y: -90

:data-x: r2000

:data-y: r2000

版本回退
========

* git log 命令显示从最近到最远的提交日志

* git log --pretty=oneline 以行来显示

* git re set --hard HEAD^  往上两个版本^^三个以上可以使用HEAD~20

* cat readme.txt查看txt

* git re set --hard 3628164 回到将来版本  后面数字为git log 时提交的号码  选前几位就行。

* 后悔药   git reflog  查看每一次的输入的指令

* git checkout -- readme.txt撤销修改

* git rm test.txt  删除某个文件 并commit 如果删错了  git checkout -- test.txt 可以恢复。

----

:data-scale: 2

:data-rotate-x: -90

:data-x: r3000

:data-y: r3000

远程仓库
=========

* git remote add origin https://github.com/zx403413599/docs.git

* git push -u origin master  这是第一次  以后用这个就行 git push origin master

* git clone http://git.oschina.net/xxxxxx/xxxxxx.git

* git fetch之后  git log --oneline --decorate--graph --all  然后git merge origin/master 
  或者git pull 一下，这等于gitfetch加git merge

* git push origin :feature 删除远程的feature分支

* gir remote --V显示远程仓库信息

----

:data-scale: 2

:data-rotate-x: -90

:data-z: r2000

:data-y: r2000

分支管理
=========

* git checkout -b dev   git checkout 命令加上 -b 参数表示创建并切换

* git branch 命令查看当前分支

* git branch <name> 创建分支

* git checkout <name>切换分支

* git checkout master  分支完成后切回master

* git merge dev分支和master 合并

* git branch -d dev合并后可以删除 dev了

* git log --graph 命令可以看到分支合并图
  Git还提供了一个 stash 功能，可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作

* git stash pop ，恢复的同时把stash内容也删了

* git branch -D <name> 强行删除没合并的分支

* git push origin master  推送指定分支 

* git clone git @github . com: michaelliao/learngit.git  克隆

----

:data-scale: 3

:data-rotate-z: -60

:data-x: r2000

:data-y: r2000

标签管理
========

* git tag  v1.0  打标签 

* git tag 查看标签

* git tag  commit num 为历史操作打标签

* git tag -a v 0 . 1 -m "version 0.1 released" 3628164  -a增加名字  -m增加说明 

* git push --tag才会把标签上传到远程仓库

* git tag -d v 0 . 1 删除标签 

* git push origin v1. 0 标签推送到 远程

* git push origin :refs/tags/<tagname> 删除远程标签  （先删除本地标签）

----

:data-scale: 0.5

:data-rotate-y: -90

:data-x: r2000

:data-y: r2000

SSH key 
=========

* ssh-keygen -t rsa -C "your_email@example.com"

* 添加你的 SSH key 到 github上面去

     + 首先你需要拷贝 id_rsa.pub 文件的内容，你可以用编辑器打开文件复制，也可以用git命令复制该文件的内容，如：
       clip < ~/.ssh/id_rsa.pub

     + 登录你的github账号，从又上角的设置（ Account Settings ）进入，然后点击菜单栏的 SSH key 进入页面添加 SSH key。

     + 点击 Add SSH key 按钮添加一个 SSH key 。把你复制的 SSH key 代码粘贴到 key 所对应的输入框中，记得 SSH key 
       代码的前后不要留有空格或者回车。当然，上面的 Title 所对应的输入框你也可以输入一个该 SSH key 显示在 github 上的一个别名。默认的会使用你的邮件名称.

* Add your key to the ssh-agent

	 + ssh-agent -s
	 
     + eval $(ssh-agent -s)
	 
     + ssh-add ~/.ssh/id_rsa

* 测试 ssh -T git@github.com


