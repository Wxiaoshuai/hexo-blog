---
title: Hexo搭建博客
date: 2021-03-16 16:47:16
tags:
- Hexo
- 个人博客
---

## 准备工作

1. **创建GitHub仓库**
2. **安装Git客户端（[下载地址](https://git-scm.com/download/win)）**
3. **电脑绑定密钥**
4. **安装Node.js（[下载地址](https://nodejs.org/en/download/)）**
5. **安装Hexo**

npm命令安装

```powershell
npm install -g hexo-cli
```


![1615880707867](https://img30.360buyimg.com/pop/jfs/t1/169010/12/13034/7688/60515eacE36b528f5/0f31e5a2786540a2.png)

初始化博客

```powershell
hexo init blog
```

![1615880808159](https://img30.360buyimg.com/pop/jfs/t1/156211/27/16450/10007/60515eacE6e29da19/1763598c0dc5ea70.png)

## 常用命令

```powershell
# 安装Hexo
npm install hexo -g
# 升级
npm update hexo -g
```

```powershell
# 新建文章
hexo n "Acticle name"
hexo new "Acticle name"

# 创建路由
hexo new page '路由地址名'

# 生成静态文件
hexo g
hexo generate

# 启动本地服务
hexo s
hexo server 	# 热部署
hexo server -s 	# 冷部署
hexo server -p 5000	# 更改端口
hexo server -i 192.168.x.x	# 自定义IP

# 清除缓存
hexo clean

# 部署到git
hexo d
hexo deploy
```

## 部署博客

### **修改配置文件**

​	主目录下_config.yml

![1615882122979](https://img30.360buyimg.com/pop/jfs/t1/155581/16/16210/11840/60515eacE330d0d00/bc221512ebc374e3.png)

### 安装Git部署插件

```powershell
npm install hexo-deployer-git --save
```

### 部署到Github

```powershell
hexo clean
hexo g
hexo d
```

![1615882499650](https://img30.360buyimg.com/pop/jfs/t1/164788/13/13145/15522/60515eacE588a6fd1/8c6d0ae9e4bcdc96.png)

**访问地址：***用户名.github.io*

## 更换主题

**主题传送门：**[Themes](https://hexo.io/themes/)

**主题下载：**

根据主题git仓库下载或直接复制文件到: 主目录/themes/ 下

```po
git clone https://github.com/Bulandent/hexo-theme-bubuzou.git themes/bubuzou
```

**修改配置文件：** 

主目录/_config.yml 配置文件 `*theme: 主题名称*`

**根据主题下载依赖：**

不同主题需要的依赖不同，请根据主题对应文件下 readme.md 中提示下载安装

------

**参考资料：**

[GitHub+Hexo 搭建个人网站](https://zhuanlan.zhihu.com/p/26625249)
