---
layout:     post
random-img: true
title:      pycharm使用matplotlib报错
subtitle:   
date:       2017-6-29
author:     LiChaoyang
description: 
keywords: pycharm
tags:
    - pycharm
---

报错信息：

``` stylus
Backend Qt5Agg is interactive backend. Turning interactive mode on. ModuleNotFoundError: No module named 'PyQt4'
```


修改anaconda 配置文件 matplotlibrc
将配置修改为

``` stylus
#backend      : Qt5Agg
backend.qt4 : PyQt4 
```
