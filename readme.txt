


Git is a version control system.
Git is free software.

Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes.

创建版本库：
mkdir learngit 
如果你使用Windows系统，为了避免遇到各种莫名其妙的问题，请确保目录名（包括父目录）不包含中文
第二步，通过git init命令把这个目录变成Git可以管理的仓库：

添加文件到Git仓库，分两步：
第一步，用命令git add告诉Git，把文件添加到仓库：
第二步，用命令git commit告诉Git，把文件提交到仓库
简单解释一下git commit命令，-m后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。
嫌麻烦不想输入-m "xxx"行不行？确实有办法可以这么干，但是强烈不建议你这么干，因为输入说明对自己对别人阅读都很重要。实在不想输入说明的童鞋请自行Google，我不告诉你这个参数。


版本回退：
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。



管理修改
先用git status查看一下状态：
git diff HEAD -- readme.txt命令可以查看工作区和版本库里面最新版本的区别：


--撤销修改
命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销


