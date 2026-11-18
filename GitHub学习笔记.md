# GitHub学习笔记

##  一、GitHub相关概念理解

### 1、GitHub是干什么的

GitHub 是基于 Git 的在线代码与文档托管平台，提供版本管理能力。既可以存放项目代码，也可以存放笔记文档，支持多人协作、开源项目交流。

### 2、Git、GitHub的核心区别

Git

• 本质：版本控制软件，安装在本地电脑

• 网络：大部分操作支持离线，仅远程同步需要联网

• 作用：记录文件改动、生成版本快照、分支管理、版本回退、合并代码

• 特点：独立软件，不需要 GitHub 也能单独使用

• 原生概念：commit、branch、merge

• 同类替代品：SVN、Mercurial

GitHub

• 本质：在线代码托管与协作平台，网页服务

• 网络：必须联网访问

• 作用：存放远程Git仓库，提供团队协作能力

• 特点：依赖Git，不能脱离Git单独运行

• 平台特有概念：PR(Pull Request)、fork、star、issue、GitHub Actions

• 同类替代品：Gitee、GitLab、Gitea

### 3、GitHub的基础概念

  Repository（仓库 / Repo）                                                                                                                                                                             GitHub 上的项目单元，存放代码、文件以及完整 Git 提交历史。分为Public（公开仓库）、Private（私有仓库）。

  README.md
  项目说明文档，一般放在仓库首页，用来介绍项目功能、安装步骤、使用方法，相当于项目说明书。

  Fork                                                                                                                                                                                                                                                     把别人的仓库复制一份到你自己账号下，你拥有这份副本的修改权限，不会改动原仓库。常用于给没有写权限的开源项目贡献代码，改完之后提交 PR。

  Pull Request（PR，合并请求）                                                                                                                                                                               GitHub 协作的核心。你修改完代码后，发起请求，邀请项目维护者查看、评审你的改动，评审通过后合并进原仓 库。原生 Git 没有 PR，它附带代码对比、在线评论、讨论流程。

  Issue
  任务管理面板，用来提交 bug、提需求、讨论想法、记录待办事项，可以分配负责人、打标签、关联提交和 PR。

  Star（标星）
  类似点赞 / 收藏，标记你感兴趣的项目；星标数量常用来衡量项目热度。

  Watch（关注）
  订阅项目动态，项目有 Issue、PR 更新时会收到通知。

  Clone
  把 GitHub 上的远程仓库下载到本地电脑，得到完整带历史的 Git 仓库（区别于直接下载 zip 包，zip 只有当前文件，没有版本历史）。

  Remote（远程仓库地址）
  本地 Git 绑定的线上仓库地址，分 HTTPS、SSH 两种连接方式，用来执行 push、pull 同步。
  
  GitHub Actions
  自动化工具，配置后自动执行测试、打包、部署等流水线任务（CI/CD）。

  GitHub Pages
  静态网页托管服务，可以直接从仓库部署网站。

  License（开源许可证）
  声明别人可以怎么使用、修改、分发你的代码，是开源项目必备文件。

## 二、Profile README的创建

### 1、创建步骤

1. 登录 GitHub，页面右上角点击加号 + → New repository（新建仓库）

2. 填写仓库信息

​     Repository name：粘贴你的 GitHub 用户名                                                                                                    

​     Description（描述）：选填，简单写个人介绍                                                                                                                                                 

4. 编辑README内容

​     打开仓库，点击 README.md 右上角铅笔图标，进入在线编辑

​     编写 Markdown 内容, 填写提交备注，点击 Commit changes 保存

 5.打开个人主页，刷新页面查看效果

### 2、生效条件

  1.仓库名字 = GitHub 用户名，大小写完全匹配

  2.仓库权限设置为 Public（公开），私有仓库不会在主页展示

  3.README.md 文件放在仓库根目录，不能放在子文件夹内

  4.README.md有内容，并且已经完成 commit 提交

## 三、 GitHub的常用指令

### 1、 基础

git init ：初始化一个仓库
git clone [git-url] ： 克隆一个已存在的仓库

### 2、配置

git config --global user.name "Your Name" ：设置用户名
git config --global user.email "youremail" ： 设置邮箱地址

### 3、暂存/提交

git add . ：暂存所有修改
git add [file_path] ： 暂存一个特定的文件
git commit -m "Commit message" ：提交暂存的修改

### 4、查看修改

git status ：查看状态
git log ：查看提交日志
git diff ： 比较修改的不同

### 5、管理分支

git branch： 列出所有分支
git branch [branch-name] ： 创建一个新分支
git checkout [branch-name] ：切换到一个指定分支
git checkout -b [branch-name] ： 创建并切换到一个新分支
git branch -d [branch-name] ： 删除一个指定分支

### 6、远程仓库

git remote add [git-url] ：添加一个远程仓库
git remote -v ：列出所有远程仓库
git pull [remote-name] [branch-name] ： 拉取一个远程分支到本地
git push [remote-name] [branch-name] ：Push本地修改到一个远程分支

### 7、取消修改

git reset --hard HEAD~1：撤销最近的提交
git reset ： 取消暂存的修改
git checkout -- [file-path]：丢弃工作目录中的修改

### 8、合并

git merge [branch-name]：合并指定的分支到当前分支
git rebase [branch-name]：把当前分支的修改基于指定分支重新应用(变基)
git tag [tag-name]：在当前提交上创建一个tag标签



