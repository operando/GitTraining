# Git Training

git log -p

git log -p [file]

git diff HEAD

Create feature-A branch
$ git checkout -b feature-A

or

$ git branch feature-A
$ git checkout feature-A

一つ前のbrunchに切り替える
git checkout -

git merge --no-ff feature-A

git log --graph

Create fix-B branch

git reset -hard [hash]

git reflog

直前のコミットメッセージの修正	
git commit --amend

Create feature-C branch

git commit -am "comment"