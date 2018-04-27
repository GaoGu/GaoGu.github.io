---
title: 使用 Hexo 基于 GitHub Pages 搭建个人博客
categories:
- hexo 
---
# Hexo 安装
	npm install hexo-cli -g	
# 建站
	hexo init <folder>
	cd <folder>
	npm install
# 编译生成博文
	hexo generate
# 启动Hexo服务器
	hexo server
调试
	
	hexo server --debug	
打开浏览器输入 http://localhost:4000/ 便可以看到最原始的博客了
# 新建一篇博客文章
	hexo new "开始blog，哈哈"
打开 Hexo 目录下的 source\_posts 目录就可以看见创建的文章
# 主题安装
[Next 主题 GitHub 地址](https://github.com/iissnan/hexo-theme-next)

拷贝至站点目录的 themes 目录下，一般命名为 next，打开站点配置文件， 找到 theme 字段，并将其值更改为 next 即可

clone下来删了.git，防止和项目的.git冲突


# 创建分类
在博客根目录输入

	hexo new page categories
打开category/index.md，改为：

	title: 分类
	date: 日期
	type: "categories"
	comments: false
再文章前添加

	---
	title: 分类测试
	categories:
	- 分类测试 
	---
主题展示分类图标，修改`主题配置文件`

	menu：
		categories: /categories/ || th
		
