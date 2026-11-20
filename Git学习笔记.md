# Git学习笔记

## 一.Git基本详细流程

Git 存在四个核心区域：远程仓库、工作区、暂存区、本地仓库，文件改动会在这四个区域之间流转。

#### 1.远程仓库（GitHub）
存放项目所有版本的云端仓库，团队所有人都可以访问这个仓库。

#### 2.git clone [仓库地址] —— 克隆仓库
作用：把GitHub上的远程仓库完整下载到本地电脑，在本地生成一份项目副本（包含所有历史版本）。执行后，本地会出现Tasks项目文件夹，这个文件夹就是工作区。

#### 3.工作区
就是我们电脑上看得见的项目文件夹，可以新建、删除、修改文件。

#### 4.git add 文件名 —— 添加到暂存区
作用：挑选需要提交的文件，将改动放到暂存区，相当于“准备打包”，告诉Git：这个文件的改动我要保存版本。

#### 5.git commit -m "提交说明" —— 提交到本地仓库
作用：把暂存区里所有改动打包，生成一个版本快照，永久保存到本地Git仓库。
-m 后面填写本次修改的描述，方便后续查看历史。

#### 6.git push —— 推送到远程仓库
作用：将本地仓库中新生成的版本，上传同步到GitHub远程仓库，远程仓库就可以看到本次修改。

### 完整提交流程

远程仓库(GitHub)
 ↓ git clone
工作区（本地文件夹，修改文件）
 ↓ git add
暂存区
 ↓ git commit
本地仓库（生成本地版本快照）
 ↓ git push
远程仓库(GitHub，同步更新)

https://private-user-images.githubusercontent.com/357843703/713665539-d63e4585-7f6b-4c4e-8994-2f0bda36240d.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTUxODY0MDUsIm5iZiI6MTc5NTE4NjEwNSwicGF0aCI6Ii8zNTc4NDM3MDMvNzEzNjY1NTM5LWQ2M2U0NTg1LTdmNmItNGM0ZS04OTk0LTJmMGJkYTM2MjQwZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjYxMTIwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI2MTEyMFQxNDQ4MjVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wMTExNDBkMjM5M2I1NjU5NjI3YzgxODc5OTM1MjI3MTMzN2IzMWQyMGEyZjhlYTUxOTY5MGQzM2ZhMmNmOWQ3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZyZXNwb25zZS1jb250ZW50LXR5cGU9aW1hZ2UlMkZwbmcifQ.xjIzo_m9__GRrRMze_Q7UeOrSPz2Nbx1qNf8akmDxNY

#### 配套常用命令说明

• git status：查看仓库当前状态，查看文件是否修改、是否加入暂存区

• git log：查看所有提交记录，查看每一次版本的提交信息

# 二.与Git Bash相比更便捷的提交方式

#### 1.Typora
Typora 作为 Markdown 编辑器，可以用来编写、预览 hello.md 这类文档，写完文件保存后，再配合 Git 工具完成提交推送。Typora 本身不自带Git版本控制功能，负责文档撰写，搭配Git一起使用，方便编辑Markdown笔记。

#### 2.VS Code 内置 Git 工具
VS Code 自带可视化 Git 面板，可以直接查看文件改动、一键暂存、填写提交信息、提交、推送代码。操作简单、无需切换软件，适合日常学习和开发。

#### 3.GitHub Desktop
专门为新手设计的 Git 图形化软件，界面简洁直观。所有版本操作可视化，零基础也能轻松完成提交、推送、拉取、分支管理。

#### 4.各类编程软件内置 Git 工具
IDEA、WebStorm 等开发工具都内置 Git 功能，写代码的同时可直接完成版本提交与推送，一体化开发，效率最高。

