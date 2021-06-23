---
title: "插入公式，图片与Widget目录显示"
date: 2021-05-25T16:59:09+08:00
categories: ['doc', 'test']
tags: ['hugo', 'toc', 'markup', 'image']
description: "测试hugo主题kagome中插入公式，插入图片和TOC目录显示"
keywords: ['unit test', 'hugo']
markup: md
toc: true
cover: "https://cloud.miiiku.xyz/src/images/cover/cover-10.jpg?x-oss-process=style/webp"
---

## 公式显示

如果需要显示公式，需要在*Front Matter*中添加`markup: md`，详见: [front-matter](https://gohugo.io/content-management/front-matter/)

When $$a \ne 0$$, there are two solutions to $$ax^2 + bx + c = 0$$ and they are:

$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$

$$
x \href{why-equal.html}{=} y^2 + 1
$$

## 带图片说明的IMAGE

```md
![测试图片](https://qiniu.sukoshi.xyz/attach/2019/06/BA98379B-EA0F-48DB-B6E1-D475D6BC4AB2.jpg@webp "中和街道")
```

![测试图片](https://qiniu.sukoshi.xyz/attach/2019/06/BA98379B-EA0F-48DB-B6E1-D475D6BC4AB2.jpg@webp "中和街道")

## 不带图片说明的IMAGE

```md
![测试图片](https://qiniu.sukoshi.xyz/attach/2019/06/IMG_4786.jpg@webp)
```

![测试图片](https://qiniu.sukoshi.xyz/attach/2019/06/IMG_4786.jpg@webp)


## TOC 功能测试

如需要显示 *TOC* Widget，需要在 *Front Matter* 中添加`toc: true`，默认设置了以后就会展示.

如需要根据长度显示，需要在 *config.toml* 中的 *params.toc_show_len* 设置具体值，如300，这样以后只有开启了toc并且文章字数超过300才会显示TOC目录.

**需要注意的是字数获取用的是`WordCount`这个属性，如果你的内容是中，日，韩等，需要在`config.toml`中配置`hasCJKLanguage = true`**

默认只显示h2-h3的标签，如需要调整，详情查看：[Hugo文档 ｜ Configure Markup](https://gohugo.io/getting-started/configuration-markup#table-of-contents)

## Introduction

One morning, when Gregor Samsa woke from troubled dreams, he found himself transformed in his bed into a horrible vermin.

## My Heading

He lay on his armour-like back, and if he lifted his head a little he could see his brown belly, slightly domed and divided by arches into stiff sections. The bedding was hardly able to cover it and seemed ready to slide off any moment.

### My Subheading

A collection of textile samples lay spread out on the table - Samsa was a travelling salesman - and above it there hung a picture that he had recently cut out of an illustrated magazine and housed in a nice, gilded frame. It showed a lady fitted out with a fur hat and fur boa who sat upright, raising a heavy fur muff that covered the whole of her lower arm towards the viewer. Gregor then turned to look out the window at the dull weather. Drops

#### My Subsubheading

hhh, self is My Heading go to My Subheading, my is My Subsubheading.

## My Bodying

He lay on his bodying display, and if it he could see his brown, what good title and housed in a nice.