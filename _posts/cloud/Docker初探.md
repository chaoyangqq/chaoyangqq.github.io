---
layout:     post
random-img: true
title:      Docker初探
subtitle:   Docker初探
date:       2018-2-26
author:     LiChaoyang
description: Docker初探，安装，使用
keywords: Docker
tags:
    - Docker
---
## 安装

 1. 卸载旧版本Docker
 2. 安装基础环境
 3. 添加Docker’s official GPG key
 4. 打印验证文件完整性
 5. 增加repository
 6. 更新apt缓存
 7. 安装最新版
 8. 查看docker-ce可得到软件版本，安装指定版本
 9. 验证安装是否成功
 10. 删除不用软件，慎用会误删

``` shell?linenums
apt-get remove docker docker-engine docker.io

sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88

add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
apt-get update

apt-get install docker-ce

apt-cache madison docker-ce
apt-get install docker-ce=17.12.0~ce-0~ubuntu

docker run hello-world
apt autoremove 
```

