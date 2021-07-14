---
title: ともだち
description: 嘿，靓仔
date: 2021-07-14T09:43:04+08:00
cover: https://cloud.miiiku.xyz/src/images/banner-3.jpg-compress
layout: link
---

添加友链页面需要先执行`hugo new link.md`然后编辑`link.md`在`Front Matter`中添加`layout: link`

在`/data/`目录下新建一个`link.yml`，HUGO支持三种格式`yml`,`json`,`toml`，保证名称为link即可

添加友链，编辑`link.yml`添加如下数据:

```yml
- { "name": "", "link": "", "description": "", "avatar": "" }
```

**name** 站点名称(必填)

**link** 站点地址(必填)

**description** 站点描述

**avatar** 站点头像