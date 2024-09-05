## 概要
git コマンドのエイリアス

## 使用方法
システム全体に適用する
1.  `~/.gitconfig` に記載
```
[alias]
	b = branch
	s = status
	f = fetch
	pl = pull
	co = checkout
	cof = !git branch -a | fzf | xargs git checkout
 	logo = log --online
	delete-feature = "!git branch | grep 'feature' | sed 's/^[* ] //' | xargs -n 1 git branch -d"
        delete-fix = "!git branch | grep 'fix' | sed 's/^[* ] //' | xargs -n 1 git branch -d"
        delete-hotfix = "!git branch | grep 'hotfix' | sed 's/^[* ] //' | xargs -n 1 git branch -d"
```
