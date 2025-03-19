---
title: "Astro 从安装到部署"
description: "astro-installation-and-deployment-guide"
pubDate: "March 18 2025"
heroImage: "/blog-placeholder-3.jpg"
---

## 1 前置环境

安装 Node.js，官网链接：https://nodejs.org/en

建议下载左侧的 LTS 版本

## 2 常用命令
	
| 命令   | 说明     |
| --------- | -------- |
| npm install | 安装依赖项 |
| npm run dev | 启动本地开发服务器 localhost:4321 |
| npm run build | 构建生产站点 ./dist/ |
| npm run preview | 在部署之前在本地预览生成 |


CMD 进入项目文件夹，运行 npm install 等待依赖安装完毕。

继续运行 npm run dev 即可本地运行。

## 3 CloudFlare Pages 部署设置

- Framework preset（框架预设）: Astro
- Build command（构建命令）: npm run build
- Build output directory（构建输出目录）: dist
- Environment variables (advanced) （环境变量：进阶）: Cloudflare Pages 默认使用 Node.js 12.18.0，但是 Astro 需要一个更高的版本。
添加一个变量名称为 NODE_VERSION 且值为 v16.13.0 或更高的环境变量，以告诉 Cloudflare 使用兼容的 Node.js 版本。
或者，将 .nvmrc 文件添加到你的项目更目录以指定 Node.js 版本。