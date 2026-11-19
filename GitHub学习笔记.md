# GitHub学习笔记

> 冯艺凡

## 学习背景

本次课程主要学习Git与GitHub的基础使用知识，了解本地版本控制工具与云端代码托管平台的区别与联系。通过学习，掌握GitHub个人主页搭建、仓库使用方法以及常用Git命令。

## 学习内容的目录

• 一、GitHub相关概念理解

• 二、Profile README的创建

• 三、GitHub的常用指令

## 学习内容

### A GitHub相关概念理解

Git是安装在本地电脑上的版本控制软件，大部分操作可以离线执行，只在同步远程仓库的时候需要联网。它主要用来记录文件改动，保存每一次修改的版本快照，支持分支管理、版本回退和代码合并，就算不使用GitHub，Git本身也可以独立工作。

GitHub则是在线的代码托管网页平台，必须联网访问，依赖Git才可以运行。它可以存放远程Git仓库，提供多人协作的能力，拥有PR、fork、star、issue等平台独有的功能。

仓库Repo是GitHub里的项目单元，用来存放代码、文档还有完整的提交历史，分为公开仓库和私有仓库。                                             README.md放在仓库首页，相当于项目说明书。
Fork可以复制别人的仓库副本到自己账号，修改副本不会影响原仓库。                                                                                                                        PR也就是合并请求，是GitHub协作的核心，修改完代码之后发起请求，等待维护者审核并入原仓库。                                                                        Issue相当于任务面板，可以提交bug、提出需求。
Star类似收藏，标记感兴趣项目。                                                                                                                                                                                    Watch用来订阅项目动态，收到更新通知。                                                                                                                                                                          Clone可以下载带完整版本历史的仓库，区别于zip压缩包，zip包没有版本记录。

感想：之前一直混淆Git和GitHub，学习之后理清了二者关系：Git是本地版本管理工具，GitHub是云端托管协作平台。开源项目依靠Fork+PR实现多人共同开发，Issue用来沟通问题，这套协作方式很适合团队开发。

### B Profile README的创建

Profile README可以自定义GitHub个人主页，相当于在线个人名片。想要生效有4个条件：仓库名称必须和GitHub用户名完全一致；仓库权限设置为公开；README.md放在仓库根目录；文件有内容并且完成commit提交。

创建步骤：登录GitHub，点击右上角加号新建仓库；仓库名填写自己的GitHub用户名，按需填写描述；进入仓库在线编辑README，使用Markdown编写内容，填写提交备注，commit保存；刷新个人主页查看效果。

感想：Profile README是展示自己的好方式，只需要满足对应的条件，就可以利用Markdown自由排版主页，展示学习记录、项目作品，打造属于自己的GitHub个人主页。

### C GitHub的常用指令

git init用来初始化本地仓库；git clone克隆远程仓库到本地。
git config --global配置全局用户名和邮箱，标记提交者信息。
git add将文件修改放到暂存区；git commit把暂存内容保存成版本快照。
git status查看文件当前状态；git log查看所有提交历史。
git branch管理分支，可以查看、新建、删除分支。                                                                                                                                                                     git checkout切换分支，开发新功能可以新建分支，不会破坏主分支代码。
git remote关联远程仓库；git pull拉取远程仓库更新；git push将本地版本上传到远程GitHub仓库。                                                                          git merge用来合并分支，git rebase实现变基，git tag给版本打标签。

