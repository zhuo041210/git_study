# git常见指令 📝
> 学习日期：2026-07-08

## 1.init命令
> 用于初始化项目，在当前文件夹下创建.git文件夹（默认隐藏），相当于是一个空的git仓库，让项目开始被git管理
> 
```bash
git init
```

## 2.clone命令
> 用于第一次复制公司项目代码，把github/gitlab代码拉到本地
```bash
git clone HTTP/SSH-address
```

## 3.config命令
> 用于首次接管项目配置用户信息
```bash
git config --global user.name/email '名字'/'邮箱'  --表示当前电脑用户的全局使用
git config --system user.name '名字'  --表示当前电脑所有用户的全局使用 
git config user.name '名字' --表示当前项目独自使用
```

## 4.重要的普通指令
> 用于提交代码
```bash
git add <文件名>   ---添加文件到暂存区
git commit -m "message"   ---提交到本地仓库
git push   ---推送到远程仓库
```
> 用于查看当前状态:包括当前分支，未被跟踪文件，未提交到暂存区的文件，未提交到本地仓库的文件
```bash
git status
```

> 用于拉取当前分支的最新代码
```bash
git pull
```

## 5.分支相关指令
> 查看分支
```bash
git branch          ---查看本地分支
git branch -r       ---查看远程分支
git branch -a       ---查看所有分支
git branch -vv      ---查看分支的跟踪关系
```

> 切换分支
```bash
git checkout <分支>     ---旧版切换到已有分支
git checkout -b <分支>  ---旧版创建并切换到新分支
git switch <分支>       ---新版切换到已有分支
git switch -c <分支>    ---新版创建并切换到新分支
```

> 融合分支
```bash
git merge <分支>        ---合并分支到当前分支
```

## 6.远程仓库相关指令
> 添加远程仓库
```bash
    git remote add origin <地址>    ---添加远程仓库的地址并起名origin
```

> 首次push代码
```bash
    git push --set-upstream origin <本地分支>:<远程分支>   ---把本地分支推送到远程仓库origin的某一分支上
```

## 7.其他重要指令
> 暂存代码&&取回暂存代码
```bash
git stash       ---因为可能要临时切到别的分支去修bug，切换分支代码丢失，所以stash
git stash pop   ---切回当前分支后恢复代码
```

> 打印提交信息
```bash
git log --oneline   ---看看每次的提交信息是什么
```

> 查看远程仓库信息
```bash
git remote -v   ---掌握远程仓库地址信息
```

> 查看具体修改
```bash
git diff    ---add前确认自己更改的文件内容
```