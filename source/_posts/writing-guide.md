---
title: 写作指导
date: 2019-08-08 04:10:05
tags:
    - 模板
    - 案例
category:
    - hexo
---

写作指导，如何创建模板，分类、tags。
<!------------- more -------------->
#### 写作模板

```
---
title: 文章标题
date: 2019-01-13 03:51:35
tags: [tag88, tag89, tag90]
category:
    - category88
    - category89
    - category90
---
```

`tags` 和 `category`均可使用数组或者列表形式添加。分类是包含层级关系的，由大到小。
####  添加新分类

* 指令

```
hexo new page categories
```

* 在categories文件夹下`index.md`添加`type`

```
---
title: 文章分类
date: 2017-05-27 13:47:40
type: "categories"
comments: false
---
```

此外还可以添加`tags`、

#### 添加新的文章

```
hexo new "文章标题"
```

#### 添加简介

`more`以上部分为简介
```
<!------------- more -------------->
```

#### 设置不转换文件
修改Hexo根目录下的_config.yml文件，将skip_render参数的值设置为README.md
```
skip_render: README.md
//  为什么需要设置这一步呢？
//  因为你执行hexo g命令时，hexo会默认将source文件里的所有md文件渲染为html文件放到public中，
//  同时README.md会被渲染为README.html文件放到public文件里
//  加上这段设置，就是告诉hexo的解析器，你在渲染source文件里的md文件时，跳过README.md文件
```