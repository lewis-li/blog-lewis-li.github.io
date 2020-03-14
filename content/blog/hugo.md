+++
Title = "使用Hugo搭建网站"
Date = 2019-12-07T15:27:43+08:00
Categories = ["program"]
# Keywords
Tags = ["hugo"]
Description = "以本网站 https://xianjun.me 为例，用hugo从头搭建一个网站"
Draft = false
+++

## 概述

以本网站 <https://xianjun.me> 为例，用hugo从头搭建一个网站

## 安装及预览

安装（以mac为例，其他系统请看官方文档）
```
brew new Hugo
```

创建网站： mysite替换成你自己的网站名
```
hugo new site mysite
```

目录说明:
- archetypes：包括内容类型，在创建新内容时自动生成内容的配置
- content：包括网站内容，全部使用markdown格式
- layouts：包括了网站的模版，决定内容如何呈现
- static：包括了css, js, fonts, media等，决定网站的外观

**重点：此时预览是一片空白，需要指定一个外观主题，请看下面的【主题及外观定制】**

## 主题

到 <https://themes.gohugo.io/> 挑选一个主题，为了让你思维不飘走，我们先随意选定一个主题，让你继续熟悉所有配置后，你再回头挑一个自己喜好的主题吧。我们以 <https://github.com/spf13/hyde> 模板为例吧：

```
cd themes
git clone https://github.com/spf13/hyde.git
```
然后，启动本地服务：
```
hugo server --theme=hyde --buildDrafts --watch
```
打开浏览器，输入 <http://127.0.0.1:1313> 预览

### 多主题

查找次序：

文件内容合并：

## 内容及分类

理解内容组织与链接的对应方式

概念:

section
slug
path
url
type

索引页: _index.md

### 分类：内容间的逻辑关系

taxonomy > term > content

页面划分及模板查找顺序：
- 分类下的术语列表：/taxonomy/terms.html
- 术语下的内容列表：/taxonomy/list.html


## 配置

### 基本配置
```
baseURL = "http://xianjun.me" # 你的域名
languageCode = "zh-Hans" # 语言类型
defaultContentLanguage = "zh-Hans" # 文章默认的语言类型
title = "贤军的博客" # 网站标题
theme = "docsy" #  主题
```

### 配置导航

主导航
```
[[menu.main]]
name="博文"
url="/blog"
weight="1"
[[menu.main]]
name="关于"
url="/about"
weight="2"
```

## 外观定制

## 模板

TODO:

```
# kind:
#     single: 页面
#     list: 列表
#     partial: 被引用
# 
# /
# |- _index.md //首页
# |- <section>
#     |- <page>.md
#     |- _index.md
```

查找规则：TODO

## 函数

常用函数
```
anchorize
humanize
deafult
jsonify
```
