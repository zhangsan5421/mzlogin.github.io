yout: post
title: git 常用命令
categories: git
description: git 常用命令
keywords: git , GitHub
---
## Git 常用命令

1. git add filename
2. git commit -m "comment"
3. git push
4. git status
5. git diff filename
6. git log (show logs)
7. git reset --hard HEAD^( ^ mean last. ^^ mean last of last. HEAD mean curent )
8. git reset --hard ID#
9. git checkout --filename. (改乱了工作区的文件不要了，就是让这个文件回到最近一次 git commit 或者 git add 时的状态。)
10. git reset HEAD file (把暂存区的修改放弃掉，使用工作区的最新版本)
11. git rm + git commit (在版本库中删除文件)
12. git remote add origin git@server-name:path/repo-name.git (关联远程库)
13. git push origin master (在本地提交 push 到远程库)
14. git clone git@github.com:path (clone 远程库到本地)
15. git checkout -b dev (创建 dev 分支并切换到 dev)
16. git branch name 创建分支
17. git branch 查看分支
18. git checkout branch-name 切换分支
19. git merge branch-name 合并某分支到当前分支
20. git branche -d branch-name 删除分支
21. git log --graph --pretty=oneline --abbrev-commit 仅展示 commit 信息的图形化分支
22. git merge --no-ff -m "merge with no-ff" dev (用不消除分支的方式 来merge dev)
23. git stash - 将尚未完成需要保存的工作暂存到stash 中
24. git stash list - 查看stash中有哪些内容
25. git stash apply - 恢复stash内容到工作区，但是并不删除stash中的内容
26. git stash drop - 删除stash中的内容
27. git stash pop - 恢复stash内容到工作区，并删除stash中的内容
28. git branch -D <name> - 强行删除某个分支，即使没有合并过
29. 多人协作工作模式
	- 试图用 git push origin branchname 推送本地更新
	- 如果推送失败，则因为远程分支比本地分支新，要先 git pull 试图合并
	- 如果合并有冲突，则解决冲突，并在本地提交
	- 没有冲突或者冲突解决后，在用 git push origin branch-name 提交
30. git remote -v 查看远程库信息
31. git push origin branch-name 从本地推送分支
32. git checkout -b branch-name origin/branch-name 从本地创建和远程对应的分支
33. git branch --set-upstream branch-name origin/branch-name 建立本地分支和远程分支的关联
34. git pull 从远程抓取分支
35. git tag v0.9 6224937 (版本号） 针对某个版本号打上标签
36. git tag - 查看标签
37. it tag -a v0.1 -m "version 0.1 released" 3628164 - 给标签加上说明
38. git show <tagname, v0.1 e.g.> - 查看标签说明
39. git tag -s <tagname> -m "blablabla..."可以用PGP签名标签；

