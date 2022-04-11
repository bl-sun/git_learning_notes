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

