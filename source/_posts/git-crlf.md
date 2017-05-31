---
title: git crlf
tags:
  - self
categories:
  - git
date: 2017-05-31 21:17:38
---
git 提交文件后行尾 crlf 变化
<!--more-->
 
# [参考](http://blog.csdn.net/ccfxue/article/details/52625806)

# 解决
1. git config --global core.autocrlf false

# why
1. If core.autocrlf is set to true, that means that any time you add a file to the git repo that git thinks is a text file, it will turn all CRLF line endings to just LF before it stores it in the commit.。
设置为true，添加文件到git仓库时，git将其视为文本文件。他将把crlf变成lf。
2.  If core.autocrlf is set to false, no line-ending conversion is ever performed, so text files are checked in as-is. This usually works ok。
设置为false时，line-endings将不做转换操作。文本文件保持原来的样子。