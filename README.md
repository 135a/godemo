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

远程仓库是新建的,本来就没有任何分支,直接一次性绑定即可`git push --set-upstream origin main`
![img_5.png](img_5.png)

现在:
![img_6.png](img_6.png)
![img_7.png](img_7.png)
推送完成


# 如果你不喜欢命令行
idea提供了很多插件可以使用
点击提交相当于git add .+git commit -m "...",
点击提交并推送相当于:git add .+git commit -m "..."+git push
![img_8.png](img_8.png)

# commit 后的注释是必写的,如果懒得写,可以自己找个插件，接入ai,自动生成

![img_9.png](img_9.png)

# 关于分支
在仓库新建一个分支:
点击branch再点击New,
![img_10.png](img_10.png)
创建选项有个main,是在问你，你的新分支的初始代码从哪个分支拉，我们暂时只有一个分支不用管
![img_11.png](img_11.png)
创建完成
![img_12.png](img_12.png)
# 我们测试一下分支
新建一个文件并推到远程仓库
![img_13.png](img_13.png)

# 我们切换到dev分支
先执行git fetch 把远程最新信息拉下来
git switch dev
