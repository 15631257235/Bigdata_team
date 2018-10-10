##  111
与传统的代码版本控制工具（集中式）不同，git是“分布式版本控制系统”

##### Git  and   SVN

SVN就是传统的集中式版本控制

![1539052071740](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\1539052071740.png)

可以看到，开发者都是通过连接中央服务器来进行代码获取或者代码提交，开发人员之间，必须通过中央服务器来合作开发。中央服务器里面保存着完整的版本库，开发者如果想要进行版本空值，就需要连接网络，如果服务器宕机，或者网络中断，开发工作将无法开展。

git分布式版本控制系统

![1539052302296](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\1539052302296.png)

由于分布式的版本控制器，每个人电脑都可以保存一份完整的版本库。从remote pull（远程牵引）下来的最新的代码，如果网络中断，开发人员完全可以在本地做版本回滚和修改提交，再在联网状态时推送到远程仓库。如果两名开发人员合作开发一个功能，可以不通过远端服务器就可以相互之间推送修改，合并冲突后由一人推送代码，大大提高开发效率。如果服务器损坏，数据丢失，也没有关系，每个人都有完整的版本库，从其他人那里克隆一份就好。但这样也存在信息安全问题。

##### Git常用指令

==git help==：git指令帮助手册

查看其他指令的做法：git help 其他指令

==git init==：初始化本地仓库

==git config==：git的配置信息相关

配置用户名：git config user.name 用户名（用于跟踪修改记录）

配置邮箱：git config user.email 邮箱（用于多人开发之间的沟通）

查看配置邮箱：git config - I

编辑配置信息：git config - e（用vim编辑，： wq是退出vim编辑器）

设置指令的别名：git config alias.别名”原指令名称 参数“

将此设置应用到整个系统中：git config - - gloabal

==git status==：查文件的状态

查看某个文件的状态：git status 文件名

查看当前路径所有文件的状态：git status

==git log==：查看文件的修改日志

查看某个文件的修改日志：git log 文件名

查看当前路径所有文件的修改日志：git log

用一行的方式查看简单的日志信息：git log - - pretty=oneline

查看最近的N次修改：git log - N（N是一个整数）

==git diff==：查看文件最新改动的地方

查看某个文件最新改动的地方：git diff 文件名

查看当前路径所有文件最新改动的地方：git diff

==git init==：出书画一个空的本地仓库，生成一个.git目录，用于维护版本信息

在当前路径初始化仓库：git init

在其他路径初始化仓库：git init 仓库路径

==git add==：将工作区的文件保存到暂缓区

保存某个文件到暂缓区：git add 文件名

保存当前路径的所有文件到暂缓区：git add .

==git commit==：将暂缓区的文件提交到当前分支

提交某个文件到分支：git commit - m“注释” 文件名

保存当前路径的所有文件到分支：git commit - m “注释”

==git reset==：版本回退（建议机上--hard参数，git支持无限次回退）

回退到上一个版本：git reset -- hard HEAD^

回退到上上个版本：git reset -- hard HEAD^^0

回退到N个版本：git reset -- hard HEAD~N（N是一个整数）

回退到任意一个版本：git reset -- hard 版本号（版本号用七位即可）

==git reflog==：查看指令使用记录（能够查看所有的版本号）

==git rm==：删除文件（删完之后要进行commit操作，才能同步到版本库）

==git clone==：下载远程仓库到本地

下载远程仓库到当前路径：git clone 仓库的URL

下载远程仓库到特定路径：git clone 仓库到URL存放仓库到路径

==git pull==：下载远程仓库的最新版本到本地仓库

==git push==：将本地的仓库信息推送到远程仓库

##### 环境搭建

https://git-scm.com/download/win 下载地址



##### 




