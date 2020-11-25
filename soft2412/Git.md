## Config
to change "git commit" to "git cmt"
`git config --global allias.<the new command> <origin command>`
for example
`git config --global allias.cmt commit`

## Log
show the history
`git log`
"n" is a number, show the n previous commits
`git log -n`
"p" is used to show the more specific detail.
`git log -n -p`
show the history with the graph of branch
`git log --graph`

## Reflog
git reflog 可以查看所有分支的所有操作记录（包括（包括commit和reset的操作），包括已经被删除的commit记录，git log则不能察看已经删除了的commit记录，而且跟进结果可以回退道某一个修改
`git reflog`

## Commit
Change the previous commit message
`git commit --amend -m "Update log message"`

## Undo
To undo into a previous commit
change the header point
`git checkout <previous commit>`
jump to the target commit and remove the commit after previous commit
`git reset <previous commit>`
change the workspace to the previous commit.
`git revert <previous commit>`

## Stash
本地存档
`git stash`
读取stash 并删掉
`git stash pop`
保存并留言
`git stash save "comments"`
列出stash
`git stash list`
列出指定stash的细节
`git stash show <stashID>`

## Branch
创建一个branch
`git branch`
跳转branch : checkout or switch
`git checkout <branch name>`

![[Pasted image 20201125155603.png]]
