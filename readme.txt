$ git config --global user.name "andyGit"
$ git config --global user.email "andy@usey.cn"

[创建版本库]
cd /d/gitStore/first
$ git init (.git隐藏目录)

[增加并提交版本库]
$ git add readme.txt
$ git add file2.txt file3.txt
$ git commit -m "wrote a readme file"

$ git status (查看状态)
$ git diff readme.txt (查看差异)

$ git log --pretty=oneline (查看日志，SHA1计算的16进制位版本号)

$ git reset --hard HEAD^ (版本回撤一次，回撤100次:git reset --hard HEAD~100)
$ git reset --hard e0764bcc81(回撤后再返回最后的版本：版本号没必要写全，会自动查找补齐)
$ git checkout -- readme.txt (在工作区的修改全部撤销)

[开始远程github仓库]
$ ssh-keygen -t rsa -C "fibiger@who.com" (将~/.ssh/id_rsa.pub提交到github中)
$ git remote add origin git@github.com:fibiger/start.git (关联到远程仓库)
$ git push -u origin master (第一次推送到远程库)
$ git push origin master

[clone]
$ git clone git@github.com:fibiger/start.git

[分支]
$ git checkout -b dev (-b表示创建并切换==git branch dev+git checkout dev)
$ git branch (查看分支)

$ git checkout master (切换回master)
$ git merge dev (合并指定分支到当前分支)
$ git branch -d dev (删除分支) --rm
