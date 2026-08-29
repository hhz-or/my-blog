---
title: OpenListNext部署教程
published: 2026-08-29
description: '将OpenListNext部署到Cloudflare Workers'
image: './pic/openlistnext1.png'
tags: ['教程','OpenListNext','Cloudflare','水']
category: '教程'
draft: false 
lang: ''
---
纯水  

## 准备事项   
1.[git](https://git-scm.com)    
2.[Node.js 20+](https://nodejs.org)  
3.一个[Github](https://github.com)账号  
4.一个[Cloudflare](https://cloudflare.com)账号  

## 开始  
1.Fork `OpenListNext`的仓库,名字随便取  
::github{repo="Polonium-salts/openlistnext"}  
2.用 `git` 克隆刚才那个你fork的仓库到本地：`git clone 你的仓库链接`  
`cd` 到仓库根目录，运行`npm install`或`pnpm install`，等待完成。  
3.运行`npx wrangler login`，绑定你的Cloudflare账号，然后运行`npm run deploy`，脚本会自动完成部署。  
## 设置自动部署  
4.打开[Clouflare Dashboard](https://dash.cloudflare.com)，登录你的账号，进入刚才那个worker的设置界面，往下翻找到`连接Git存储库`  
绑定你的`github`账号，选择刚才fork的那个仓库   
构建命令就是`pnpm run build`，其他默认即可（如是第一次使用可能需要你安装`Cloudflare`的`github app`，照着提示走就行）  
以后`OpenListNext`更新了去你fork的那个仓库点下`Sync fork`同步就行了（设置等数据存在`Worker KV`数据库中，更新正常来说不会造成任何影响）  
##  
5.默认用户名是`admin`，密码是`admin`，部署后请务必在`用户管理`中修改密码。  
6.剩下设置什么的就可以直接照着`OpenList`的[官方文档](https://doc.oplist.org)了  
##  
其他平台部署在项目[README.md](https://github.com/Polonium-salts/openlistnext)里也有，可以自行查看  



