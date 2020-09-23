git is a version control system
and also git is a free software.
git is a software distributed under the GPL

 ssh-keygen -t rsa -C "username"
 cat /c/Users/Administrators/ssh.pub file

 entering the settings and add this rsa.

git status


 git commit -m "git tracks changes"



创建新路径
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit

创建新仓库
$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/

$ git add readme.txt
$ git commit -m "wrote a readme file"


 在GitHub上创建repository，然后根据创建的路径上传
 git remote add origin git@github.com:someone/learngit.git
 git push -u origin master


$ git add readme.txt
$ git commit -m "append GPL"
[master 1094adb] append GPL
 1 file changed, 1 insertion(+), 1 deletion(-)

Notice： 1. for the second time to update this file, should add this modified file and then sumbmit then have a try
         2. 在完成了这些修改内容之后，在提交之前需要先完成一下pull,然后提交



 $ git log
 $ git log --pretty=oneline

 $ git reset --hard HEAD^
 $ cat readme.txt
 $ git log


/*****************************************   补充完成教程内容   *****************************************/

完成git的安装之后 的配置信息
用户信息
git config --global user.name "test"
git confit --global user.email test@hotmail.com
如果使用了 --global 选项，该命令只需要运行一次，因为之后在该系统上做任何事情，git都会使用这些信息，当想要
针对特定项目使用不同的用户名和邮件地址时候，可以在那个项目目录下运行不适用 --global 选项来配置，很多GUI工具都会
在第一次运行时候帮助你配置这些信息

选择使用不同的文本编辑器，可以使用如下命令：
$git config --global core.editor emacs

检查配置信息
想要检查配置信息，可以使用 git config --list 命令来列出所有git当时能找到的配置
$git config --list,
如果列出重复的变量名，因为git会从不同的文件中读取同一配置，这种情况下， git会使用它找到的每一个变量的最后一个配置

git获取帮助
git help <version>
git <verb> --help
man git-<verb>

config命令的手册
git help config

检出仓库
git clone /path/to/repository
git clone username@host:/path/to/repository

工作流
你的本地仓库由 git 维护的三棵“树”组成。
第一个是你的 工作目录，它持有实际文件；
第二个是 暂存区（Index），它像个缓存区域，临时保存你的改动；
最后是 HEAD，它指向你最后一次提交的结果。


添加和提交
git add <filename>
git add *
这是 git 基本工作流程的第一步；使用如下命令以实际提交改动：

git commit -m "代码提交信息"
现在，你的改动已经提交到了 HEAD，但是还没到你的远端仓库。

推送改动
你的改动现在已经在本地仓库的 HEAD 中了。执行如下命令以将这些改动提交到远端仓库：
git push origin master
可以把 master 换成你想要推送的任何分支。

如果你还没有克隆现有仓库，并欲将你的仓库连接到某个远程服务器，你可以使用如下命令添加：
git remote add origin <server>


创建一个叫做“feature_x”的分支，并切换过去：
git checkout -b feature_x
切换回主分支：
git checkout master
再把新建的分支删掉：
git branch -d feature_x
除非你将分支推送到远端仓库，不然该分支就是 不为他人所见的：
git push origin <branch>


更新与合并
要更新你的本地仓库至最新改动，执行：
git pull
以在你的工作目录中 获取（fetch） 并 合并（merge） 远端的改动。
要合并其他分支到你的当前分支（例如 master），执行：
git merge <branch>
在这两种情况下，git 都会尝试去自动合并改动。遗憾的是，这可能并非每次都成功，并可能出现冲突（conflicts）。 这时候就需要你修改这些文件来手动合并这些冲突（conflicts）。改完之后，你需要执行如下命令以将它们标记为合并成功：
git add <filename>
在合并改动之前，你可以使用如下命令预览差异：
git diff <source_branch> <target_branch>


标签
为软件发布创建标签是推荐的。这个概念早已存在，在 SVN 中也有。你可以执行如下命令创建一个叫做 1.0.0 的标签：
git tag 1.0.0 1b2e1d63ff
1b2e1d63ff 是你想要标记的提交 ID 的前 10 位字符。可以使用下列命令获取提交 ID：
git log
你也可以使用少一点的提交 ID 前几位，只要它的指向具有唯一性。


替换本地改动
假如你操作失误（当然，这最好永远不要发生），你可以使用如下命令替换掉本地改动：
git checkout -- <filename>
此命令会使用 HEAD 中的最新内容替换掉你的工作目录中的文件。已添加到暂存区的改动以及新文件都不会受到影响。

假如你想丢弃你在本地的所有改动与提交，可以到服务器上获取最新的版本历史，并将你本地主分支指向它：
git fetch origin
git reset --hard origin/master


实用小贴士
内建的图形化 git：
gitk
彩色的 git 输出：
git config color.ui true
显示历史记录时，每个提交的信息只显示一行：
git config format.pretty oneline
交互式添加文件到暂存区：
git add -i

教程链接地址：http://www.runoob.com/manual/git-guide/


ssh-keygen -t rsa
find the user.ssh pub key
update the website
ssh -T git@github.com
