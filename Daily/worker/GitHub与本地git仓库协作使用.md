# GitHub 与 本地 git 仓库协作使用

- - - -

## 配置

1. 创建SSH Key

如果有 `~/.ssh` 目录，以及 `～/.ssh/id_rsa` (私钥) 和 `~/.ssh/id_rsa.pub` (公钥) 就说明这步以及完成了，若没有：

```
$ ssh-keygen -t rsa -C "youremail@example.com"
```

2. 配置GitHub上的SSH Keys

GitHub —> Account settings —> SSH and GPG Keys —> New SSH Key —> 填写Title —> 把 `id_res.pub` 文件内容粘贴到Key

3. 使用GitHub提供的如下两条命令：

```
$ git remote add origin .*?github.com.*?
$ git push -u origin master
```

然后要输入GitHub的用户名和密码

- - - -

## 使用

#### 查看远程库的信息

```
$ git remote		 # 看远程仓库的名称
$ git remote -v		# 更详细一些的信息
```

1. 把本地仓库推送到GitHub

```
$ git push origin master		# 把本地的master分支的最新修改推送到GitHub

 # When we run this the first time, Git will show a Warning, which is because you are wanted to make sure whether the SSH Key of GitHub is really from GitHub.com. Here we enter ‘Yes’ to continue.

 # 在没有冲突的情况下，直接 master 到 master
$ git push
```


2. 从远程仓库克隆

It’s better to click ‘Use SSH’ for faster and safer.

在工作目录下使用：

```
$ git clone <粘贴>
 # git 会在当前目录下新建一个名为hello-world的目录（git仓库）
```

3. 与远程仓库同步（pull）

```
$ git pull 
```

4. 从远程仓库获取更新的版本（fetch）

在本地新建一个temp分支，并将远程origin仓库的master分支代码下载到本地temp分支：

```
$ git fetch origin master:temp
```

直接 fetch 远程的 master 覆盖本地的 master：

```
$ git fetch
```
