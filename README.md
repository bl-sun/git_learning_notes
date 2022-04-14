# git学习笔记

git一般只能添加数据，所以我们可以放心大胆的操作git

## git常用操作

> 基本的git工作流程如下：
> 1. 在工作区中修改文件
> 2. 将你想要下次提交的更改选择性地暂存，这样只会将更改的部分添加到暂存区。
> 3. 提交更新，找到暂存区的文件，将快照永久性存储到Git目录

### 配置文件

```git-bash
$ git config --list --show-origin # 查看所有配置以及它们所在的文件
$ # 使用下面的两条命令配置用户信息
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

> 每一个 Git 提交都会使用这些用户信息，它们会写入到你的每一次提交中，不可更改

```git-bash
$ git config --list # 列出所有git现在的配置
```

### 获取Git仓库

通常有两种获取Git项目仓库的方式：

1. 将尚未进行版本控制的本地目录转换为Git仓库；
2. 从其他服务器**克隆**一个已存在的Git仓库；

####### 本地目录创建

```git-bash
$ cd ~/my_project
$ git init
```

####### 克隆远程仓库

```git-bash
$ # git <url> [new-forder-name]
$ # 使用url克隆一个远程仓库，并指定本地名称
$ git clone https://github.com/libgit2/libgit2 mylibgit
```


### 查看状态

```git-bash
$ git status
$ # 显示简短状态
$ git status -s
$ git status --short
 M README
MM Rakefile
A  lib/git.rb
M  lib/simplegit.rb
?? LICENSE.txt
```

- `??` 未追踪的文件
- `A ` 新添加到暂存区的文件
- `M ` 已修改且已暂存
- ` M` 已修改未暂存
- `MM` 修改后暂存，又修改了的

其中左侧字符是最后一次提交与暂存区中对比
右侧字符是工作区对比暂存区


### 提交更新

```git-bash
$ git commit
```


## 分支

### 创建分支

```git-bash
$ git branch testing # 创建testing分支
$ git checkout testing # 切换到testing分支
```

## 测试

一些测试内容