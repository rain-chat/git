# git使用教程

## 1. 初始化
```
git init
```
使用该命令，得到以下.git目录

![image](https://user-images.githubusercontent.com/75610421/187200121-fc02b3ec-a12e-4256-b48a-bc9b3f21c61c.png)

## 2. 添加文件 
#### 1. 添加所有文件,文件与.git目录同级
```
git add .
```
#### 2. 添加指定文件
```
git add fileName
```
例如：
```
git add C++学习笔记.md
```

## 3. 提交文件到暂存区
```
git commit -m "text"
```
text用于描述本次提交。

## 4. push至远程分支
#### 1. 首先，添加远程分支
```
git remote add name ssh_url
```
name任意即可，建议和远程仓库同名，ssh_url为上传目标仓库的SSH地址。

例如:添加rainchat 远程分支 其SSH为 git@github.com:rain-chat/rainchat.git，则指令为
```
git remote rainchat git@github.com:rain-chat/rainchat.git
```

#### 2. 上传至远程仓库
```
git push name master
```
name依然是远程仓库名，master是本地分支，使用git init 默认创建的就是master分支。如果想使用
其他分支，可以使用以下指令创建新分支
```
git branch branchName(分支名)
```
使用以下指令切换分支
```
git checkout branchName
```
#### 3. push出错的处理
如果上传失败可以尝试执行该指令，name依然是远程仓库名，master是本地分支
```
git pull --rebase name master
```


## 5. 其他指令
##### 常用指令
用于git add后查看暂存区状态。
```
git status
```


1. 当前本地分支，-v可选，-v为详细内容
```
git branch -v
```
2. 远程分支,-v可选，-v为详细内容
```
git remote -v
```
3. 显示提交日志信息
```
git log
```
4. 查看git配置信息
```
git config --list
```
例如以下信息：
```
user.name=NAME
user.email=QQ@qq.com
```
5. 查看远程分支信息
```
 git remote show remoteBranchName
```
6. 克隆项目
```
git clone remoteBranchSSH                         # 例如git clone https://github.com/regsi/rainchat.git
```
