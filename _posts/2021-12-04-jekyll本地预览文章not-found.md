---
layout: post
title: "jekyll本地预览文章not found"
category: 疑难杂症
tags: [疑难杂症]
---

jekyll 本地预览文件找不到文章

网上搜索得知是编码的问题, 然后按照文章中提供的解决方案,修改ruby安装路径下的C:\Ruby25-x64\lib\ruby\2.5.0\webrick\httpservlet,在文件中分别插入下列语句,强制使用utf-8解码。

```
path = req.path_info.dup.force_encoding(Encoding.find("filesystem"))
path.force_encoding("UTF-8")             #新插入的行，插入到第286行，或根据上下文定位
if trailing_pathsep?(req.path_info)
```

```
path = req.path_info.dup.force_encoding(Encoding.find("filesystem"))
path.force_encoding("UTF-8")             #新插入的行，插入到第286行，或根据上下文定位
if trailing_pathsep?(req.path_info)
```

