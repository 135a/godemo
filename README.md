# 这是一个没有git初始化的项目

git不需要ai,它和ai没有任何关系,它比ai要早几十年,和linux是同一个作者


# 首选需要git初始化项目,这个项目才能被git管理
git init
注意该命令执行的目录,就是项目根目录
![/img/img.png](img.png)

# git主要命令:
## git add .
该命令将你的修改保存到git缓存区

## git commit -m "本次修改的内容"
该命令正式提交了你的修改,执行了此操作后,如果以后发现代码出现了严重错误需要立刻恢复,

可以直接回退到该位置(是团队任何人都可以回退到该位置)
![/img/img_1.png](img_1.png)


## git push
该命令可以将你的代码推送到远程仓库,即github仓库,任何人(主要是你团队的人可以拉下来,可以设置为代码权限,阅读、修改之类的)
其实也不一定是github,github只是最经典的,大部分人都在用的,你也可以推送到其它地方,比如Gitee,比如你自己的服务器上等等

![img.png](img.png)
这里报错了,因为远程仓库根本没有你这个项目

所以我们需要到远程仓库建一个:
点击new
![img_1.png](img_1.png)

仓库名称、可见性自己设置
![img_2.png](img_2.png)

建好了
![img_3.png](img_3.png)


# git remote add origin https://github.com/135a/godemo.git

把自己的项目和远程仓库关联起来

![img_4.png](img_4.png)

# git branch -M main
重命名本地分支,可选,
一个项目有很多分支,供不同团队开发
比如大厂规范:
dev开发分支
main线上分支,客户正在使用的、正在运行的分支、不能动、一般情况下你也没有权限动
fix修改bug分支
...

# 再次提交push

注意:如果你有尚未保留在git缓存的东西,必须先add、commit再Push


