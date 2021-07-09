---
title: "播放音频与视频，shortcode使用说明"
date: 2021-05-26T11:32:04+08:00
categories: ['doc']
tags: ['video', 'music']
aplayer: true
dplayer: true
grow: large
---

Hugo ships with several [Built-in Shortcodes](https://gohugo.io/content-management/shortcodes/#use-hugo-s-built-in-shortcodes) for rich content, along with a [Privacy Config](https://gohugo.io/about/hugo-and-gdpr/) and a set of Simple Shortcodes that enable static and no-JS versions of various social media embeds.


Hugo默认支付播放YouTube，Vimeo等视频格式，所有支持的类型见: [Hugo/templates/shortcodes](https://github.com/gohugoio/hugo/tree/master/tpl/tplimpl/embedded/templates/shortcodes)

使用方式见官方文档: [shortcode-templates](https://gohugo.io/templates/shortcode-templates/)

如添加一个YouTube视频:

## YouTube Privacy Enhanced Shortcode

```md
<!-- 实际写的时候 '['替换为 '{' ']'替换为'}' -->
[[< youtube hDy9BrB9_VU >]]
```

{{< youtube hDy9BrB9_VU >}}


    
**除了官方已有的`shortcode`模版，`kagome`目前有两个自定义的shortcode，分别是`aplayer`和`dplayer`，如下:**

[aplayer文档地址](https://aplayer.js.org/#/)

[dplayer文档地址](https://dplayer.js.org/#/)
    

## aPlayer Shortcode

**如果需要使用aplayer需要在`Front Matter`中添加`aplayer: true`**

```md
<!-- 实际写的时候 '['替换为 '{' ']'替换为'}' -->
[[< aplayer
    url="https://qiniu.sukoshi.xyz/public/music/鹿乃 - アイロニ.mp3"
    name="アイロニ"
    artist="鹿乃"
    cover="https://qiniu.sukoshi.xyz/public/music/鹿乃 - アイロニ.jpg"
    lrc="https://qiniu.sukoshi.xyz/public/music/鹿乃 - アイロニ.lrc"
    lrcType="3"
>]]
```

{{< aplayer
    url="https://qiniu.sukoshi.xyz/public/music/鹿乃 - アイロニ.mp3"
    name="アイロニ"
    artist="鹿乃"
    cover="https://qiniu.sukoshi.xyz/public/music/鹿乃 - アイロニ.jpg"
    lrc="https://qiniu.sukoshi.xyz/public/music/鹿乃 - アイロニ.lrc"
    lrcType="3"
>}}


## dPlayer Shortcode

**如果需要使用dplayer需要在`Front Matter`中添加`dplayer: true`**

```md
<!-- 实际写的时候 '['替换为 '{' ']'替换为'}' -->
[[< dplayer
    url="https://qiniu.sukoshi.xyz/video/%E7%BE%8E.mp4"
    pic="https://qiniu.sukoshi.xyz/video/%E7%BE%8E.mp4?vframe/jpg/offset/10"
>]]
```

{{< dplayer
    url="https://qiniu.sukoshi.xyz/video/%E7%BE%8E.mp4"
    pic="https://qiniu.sukoshi.xyz/video/%E7%BE%8E.mp4?vframe/jpg/offset/10"
>}}
