---
title: Git 创建仓库
top: false
cover: false
toc: true
mathjax: true
categories:
  - Git
tags:
  - Git
date: 2024-02-19 00:53:25
---

# Git 创建仓库

## git init

Git 使用 **git init** 命令来初始化一个 Git 仓库，Git 的很多命令都需要在 Git 的仓库中运行，所以 **git init** 是使用 Git 的第一个命令。

在执行完成 **git init** 命令后，Git 仓库会生成一个 .git 目录，该目录包含了资源的所有元数据，其他的项目目录保持不变。

<!--more-->

### 使用方法

使用当前目录作为 Git 仓库，我们只需使它初始化。

```
git init
```

