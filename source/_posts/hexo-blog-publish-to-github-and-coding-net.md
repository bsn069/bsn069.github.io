---
title: hexo blog publish to github and coding.net
tags:
  - unknown
categories:
  - unknown
date: 2017-05-22 13:31:36
---
### hexo blog 自动发布到 github coding.net(gitcafe)
<!--more-->

> .travis.yml

    language: node_js
    node_js:
    - "stable"  # nodejs的版本
    branches:
      only:
      - hexo  # 设置自动化部署的源码分支
    cache:
      directories:
        - node_modules
    before_install:
    - export TZ='Asia/Shanghai'  # 设置时区
    # 设置github账户信息
    - git config --global user.name "bsn_travis" #设置github用户名
    - git config --global user.email 513026809@qq.com #设置github用户邮箱
    #- npm install -g hexo
    - npm install -g hexo-cli
    # 安装依赖组件
    install:
    - npm install
    # 执行的命令
    script:
    - hexo clean
    - hexo generate
    # 执行的成功后执行 
    after_success:
    - cd ./public
    - git init
    - git add --all .
    - git commit -m "travis ci auto builder"

    # github
    - git push --quiet --force https://$github_tokenN@github.com/$github_user/$github_user.github.io.git master
    # gitcafe coding.net
    - git push --quiet --force https://$gitcafe_user:$gitcafe_pwd@git.coding.net/$gitcafe_user/$gitcafe_user.git master
