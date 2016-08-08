yout: post
title: template page
categories: [cate1, cate2]
description: some word here
keywords: keyword1, keyword2
---
## Git 常用命令


git add filename
git commit -m'comment'
git push
git status (check status)
git diff filename
git log (show logs)
git reset --hard HEAD^ (^ means last, ^^ means last of last, HEAD means current)
git reset --hard ID#
git checkout -- filename (乱改了工作区的文件不要了，就是让这个文件回到最近一次git commit或git add时的状态。)
git reset HEAD file (把暂存区的修改放弃掉，使用工作区的最新版本）
git rm + git commit （在版本库中删除文件）
git remote add origin git@server-name:path/repo-name.git （关联远程库）
git push origin master （将本地提交push 到远程库）
git clone git@github.com: 路径 ( clone 远程库到本地）
git checkout -b dev (创建dev 分支并切换到dev)
git branch (查看分支）
git branch name （创建分支）
git checkout name （切换分支）
git merge name (合并某分支到当前分支）
git branch -d name (删除分支）
git log --graph --pretty=oneline --abbrev-commit （仅展示commit信息的图形化分支）
git merge --no-ff -m "merge with no-ff" dev (用不消除分支的方式 来merge dev)
git stash - 将尚未完成需要保存的工作暂存到stash 中
git stash list - 查看stash中有哪些内容
git stash apply - 恢复stash内容到工作区，但是并不删除stash中的内容
git stash drop - 删除stash中的内容
git stash pop - 恢复stash内容到工作区，并删除stash中的内容
git branch -D <name> - 强行删除某个分支，即使没有合并过
多人协作工作模式
试图用 git push origin branchname 推送本地更新
如果推送失败，则因为远程分支比本地分支新，要先 git pull 试图合并
如果合并有冲突，则解决冲突，并在本地提交
没有冲突或者冲突解决后，在用 git push origin branch-name 提交
git remote -v 查看远程库信息
git push origin branch-name 从本地推送分支
git checkout -b branch-name origin/branch-name 从本地创建和远程对应的分支
git branch --set-upstream branch-name origin/branch-name 建立本地分支和远程分支的关联
git pull 从远程抓取分支
git tag v0.9 6224937 (版本号） 针对某个版本号打上标签
git tag - 查看标签
git tag -a v0.1 -m "version 0.1 released" 3628164 - 给标签加上说明
git show <tagname, v0.1 e.g.> - 查看标签说明
git tag -s <tagname> -m "blablabla..."可以用PGP签名标签；：
