---
title: Docker基础学习
date: 2021-03-15 16:45:44
tags: 
- Docker
- 服务器
---

## Docker是什么？

Docker是一个虚拟环境容器，可以将你的开发环境、代码、配置等一并打包到这个容器中，并发布和应用到任意平台上。

## 三大概念

1. **镜像（Image）：**类似于虚拟机中的镜像，是一个包含有文件系统的面向Docker引擎的只读模板。任何应用程序运行都需要环境，而镜像就是用来提供这种运行环境的。例如一个Ubuntu镜像就是一个包含Ubuntu操作系统环境的模板，同理在该镜像上装上Apache软件，就可以称为Apache镜像
2. **容器（Container）：**类似于一个轻量级的沙盒，可以将其看作一个极简的Linux系统环境（包括root权限、进程空间、用户空间和网络空间等），以及运行在其中的应用程序。Docker引擎利用容器来运行、隔离各个应用。容器是镜像创建的应用实例，可以创建、启动、停止、删除容器，各个容器之间是是相互隔离的，互不影响。注意：镜像本身是只读的，容器从镜像启动时，Docker在镜像的上层创建一个可写层，镜像本身不变
3. **仓库（Repository）：**类似于代码仓库，这里是镜像仓库，是Docker用来集中存放镜像文件的地方。注意与注册服务器（Registry）的区别：注册服务器是存放仓库的地方，一般会有多个仓库；而仓库是存放镜像的地方，一般每个仓库存放一类镜像，每个镜像利用tag进行区分，比如Ubuntu仓库存放有多个版本（12.04、14.04等）的Ubuntu镜像

## Windows下安装

### 安装步骤

1. 系统要求windows 10企业版

2. 开启Hyper-V

3. 下载[Docker Desktop forWindows](https://hub.docker.com/editions/community/docker-ce-desktop-windows)

4. 使用exe安装

5. 测试安装是否成功

   ```powershell
   # docker run hello-world
   # docker version
   ```

### 安装问题汇总

启动因WSL 2报错，需要安装WSL 2。（适用于 Linux 的 Windows 子系统安装指南）



**参考资料:**

1. [只要一小时，零基础入门Docker](https://zhuanlan.zhihu.com/p/23599229)
2. [菜鸟教程-Windows Docker 安装](https://www.runoob.com/docker/windows-docker-install.html)