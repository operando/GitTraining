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

HEADを含めた２つまでのCommitを対象
rebase -i HEAD~2

pick hash Commit comment
↓
fixup hash Commit comment

Create feature-D branch

リモートリポジトリのbranchも含んで表示
git branch -a

checout元のbrunchを指定「origin/feature-D」
git checkout -b feature-D origin/feature-D

改行コードを無視して比較する

git diff -w

リモートブランチとローカルブランチの差分を表示する

git diff remotes/origin/master

## リモートブランチを含めたブランチ一覧表示

git branch -a

## リモートブランチのユーザ名と時間を含めたブランチ一覧を表示する

git for-each-ref --format='%(committerdate) %09 %(authorname) %09 %(refname)'

## remote originからブランチを切る

git checkout -b [branch_name] [remoto_branch_name]

## ブランチを強制削除する

git branch -D [branch_name]

## コミットしたあとにそのコミットに変更を追加する

git add README.md

git commit --amend

## remoteにbranshをPushする

git push origin [branch_name]

## remoteのbranshを削除する

git push -u origin :[branch_name]

## 自身のCommit Logを表示する

git log --author="`git config --get user.name`"

## Tagの作成

git tag -a [tag name] -m "comment"

## 過去の状態のTagの作成

git tag -a [tag name] -m "comment" [commit hash]

## Tagの削除

git tag -d [tag name]

## TagのPush

git push origin [tag name]

## Tagのチェックアウト

git checkout -b [branch name] [tag name]

## Tagの表示

git tag -l