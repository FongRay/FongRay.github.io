---
layout: post
title: Git 错误使用导致的工作失误
list_title: Git 错误使用导致的工作失误
tags: [Git, 踩坑]
categories: Coding
---

最近因为 Git 误操作坑了一把！

![](https://fangr-cc-image.oss-cn-beijing.aliyuncs.com/18-8-16/9699135.jpg)

<!-- more -->

如上图所示。

准备发 5.7.5 的时候，提交错了分支！！

我感觉整个过程有多个地方可以规避这个问题：

* 本地新建了一个分支，而不是直接拉远程分支
```
$ git branch featur_5.7.5 ❌
$ git checkout -b feature_5.7.5 origin/feature_5.7.5 ⭕️
```

* 本地提交的时候，遇到 git 报错，要重视，不要随便加 `--force`

* 提交完之后，看下终端是不是提示新建了一个分支！

* 打包的时候，可以看到最新的工程包中，代码的变更！可以看到是否是自己刚提交的代码

---
总结下来，

- 急中生乱！
- 对代码保持敬畏之心，特别是临上线的时候，任何变动都要仔细！
- 拼写错误要重视，特别是敏感操作！

> 这个错误操作，直接导致了线上 crash 率上升了几个点！

😒😒😒
