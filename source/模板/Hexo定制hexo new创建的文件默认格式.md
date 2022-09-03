# Hexo定制hexo n创建的文件默认格式

每次写文章还要敲或者复制comments、category有点麻烦，最好执行hexo new “post name”的时候就默认生成。

脚手架在scaffolds文件夹下，里面默认有post.md、draft.md、page.md三个，分别为博文、草稿和page的脚手架

只需要修改post.md如下这样每次新建文章的时候就会自动添加category和comments为了方便我吧用来标记折叠的more也加入了，这样只需在想要折叠的地方换行就可以了。

```hexo
---
title: {{ title }}
date: {{ date }}
tags:
category:
comments: true
---
<!--more-->
```

备注：也可以在`scaffolds`下新建`tpx.md`作为模板，模板标题不能为大写，使用时不区分大小写`tpx`、`Tpx`、`TPX`都可以。

新建文章时
`hexo new tpx "文章名"`
