git is a version control system
and also git is a free software.
git is a software distributed under the GPL

 ssh-keygen -t rsa -C "username"
 cat /c/Users/Administrators/ssh.pub file

 entering the settings and add this rsa.

git status


 git commit -m "git tracks changes"
 git remote add origin git@github.com:someone/learngit.git
 git push -u origin master





$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit

$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/

$ git add readme.txt
$ git commit -m "wrote a readme file"

$ git add readme.txt
$ git commit -m "append GPL"
[master 1094adb] append GPL
 1 file changed, 1 insertion(+), 1 deletion(-)


for the second time to update this file, should add this modified file and then sumbmit
then have a try



 $ git log
 $ git log --pretty=oneline

 $ git reset --hard HEAD^
 $ cat readme.txt
 $ git log