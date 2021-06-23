---
title: "config.toml配置"
date: 2021-06-09T11:32:04+08:00
categories: ['doc']
tags: ['hugo', 'config']
description: "config.toml在kagome中的配置项"
toc: true
cover: "https://cloud.miiiku.xyz/src/images/cover/cover-12.jpg?x-oss-process=style/webp"
---

config配置文件中配置可参考Hugo官方文档: [Configure Hugo](https://gohugo.io/getting-started/configuration/)

这里主要补充`kagome`中所需要的一些配置项:

`kagome`所需的配置项都在`config.toml`中的`[params]`中。

## 基本配置项:

| key          	| type   	| describe                       	| example           	|
|--------------	|--------	|--------------------------------	|-------------------	|
| keywords     	| array  	| 站点关键词                     	| ["hugo", "theme"] 	|
| description  	| string 	| 站点描述                       	| 一个新的站点      	|
| mainSections 	| array  	| 主要内容sections               	| ["posts"]         	|
| beian        	| string 	| 备案信息                       	| xxxxxx            	|
| toc_show_len 	| number 	| 指定内容长度以后出现目录widget 	| 200               	|

**其中如果没有配置`mainSections`，那么则会默认获取`posts`下的文章，所以如果没有配置`mainSections`请确保在`content/posts`下有内容**


## widget

widget小部件相关配置项在`[params]`下的`[params.widget]`中:

其中`author`小部件数据来源与`config.toml`下的`author`，它需要`name`，`description`，`avatar`这三个字段，如:

```toml
[author]
  name = "Sukoshi"
  email = "guanquanhong@163.com"
  description = "梅花鹿的角叫鹿角"
  avatar = "https://s.gravatar.com/avatar/7b5a0b07a98895278cfa862b1f32ae8f?s=200&r=g&d=retro"
```

其中`articles`小部件内容是根据当前文章`Front Matter`中的`categories`来查找最新的文章。

如果当前文章没有`categories`或者没有相关文章，则会去查找`tags`的相关文章。

如果也没有相关数据最终会去找当前文章`sections`下的最新文章。

| key              	| type   	| default 	| describe             	|
|------------------	|--------	|---------	|----------------------	|
| articles_count   	| number 	| 6       	| 相关文章widget条目数 	|
| categories_count 	| number 	| 6       	| 分类widget条目数     	|
| tags_count       	| number 	| 12      	| 标签widget条目数     	|


## social 社交图标

social相关配置项在`[params]`下的`[params.social]`中:

注: 一般需要的值只是社交平台中你账号的唯一标识符，并不是一个网页URL链接。

| key       	| describe  	| example      	|
|-----------	|-----------	|--------------	|
| github    	| github    	| miiiku       	|
| twitter   	| 推特      	| guanquanhong 	|
| weibo     	| 微博      	| 5561168966   	|
| zhihu     	| 知乎      	| miku-84      	|
| instagram 	| instagram 	|              	|

## aplayer 音乐播放器

aplayer相关配置项在`[params]`下的`[params.aplayer]`中:

具体的配置项描述可以查阅aplayer官方文档 [aplayer文档地址](https://aplayer.js.org/#/)

目前支持的相关参数如下

| key      	| default   	| describe                                                     	|
|----------	|-----------	|--------------------------------------------------------------	|
| theme    	| '#b7daff' 	| 主题色                                                       	|
| autoplay 	| false     	| 音频自动播放                                                 	|
| loop     	| 'all'     	| 音频循环播放, 可选值: 'all', 'one', 'none'                   	|
| mutex    	| true      	| 互斥，阻止多个播放器同时播放，当前播放器播放时暂停其他播放器 	|


## dplayer 音乐播放器

dplayer相关配置项在`[params]`下的`[params.dplayer]`中:

具体的配置项描述可以查阅dplayer官方文档 [dplayer文档地址](https://dplayer.js.org/#/)

目前支持的相关参数如下

| key      	| default   	| describe                                                     	|
|----------	|-----------	|--------------------------------------------------------------	|
| theme    	| '#b7daff' 	| 主题色                                                       	|
| autoplay 	| false     	| 视频自动播放                                                 	|
| loop     	| false     	| 视频循环播放                                                 	|
| mutex    	| true      	| 互斥，阻止多个播放器同时播放，当前播放器播放时暂停其他播放器 	|