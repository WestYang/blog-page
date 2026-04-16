---
layout: post
title: 网络代理配置指南
date: 2026-04-16 10:00:00 +0800
categories: 技术
---

# 网络代理配置指南

本文介绍在不同环境下配置代理的方法，包括yum、docker和pip的代理设置。

## 1、yum配置代理

编辑yum配置文件：

```bash
# vim /etc/yum.conf
# 加入下面一行代理配置
proxy= http://10.33.49.191:10809
```

## 2、docker 配置代理

创建docker服务目录并配置代理：

```bash
sudo mkdir -p /etc/systemd/system/docker.service.d
vim /etc/systemd/system/docker.service.d/http-proxy.conf    
#添加代理配置
[Service]
Environment="HTTP_PROXY=http://your-proxy-server:port/"
Environment="HTTPS_PROXY=https://your-proxy-server:port/"
Environment="NO_PROXY=localhost,127.0.0.1,.example.com"
```

## 3、pip配置代理和源

设置pip的代理和镜像源：

```bash
pip config set global.proxy http://10.100.28.114:3180
pip config set global.index-url https://mirrors.ustc.edu.cn/pypi/simple
pip config set global.trusted-host mirrors.ustc.edu.cn
```

## 总结

以上配置方法可以帮助您在不同的环境中设置代理，确保网络访问的顺畅。根据您的实际网络环境，替换相应的代理服务器地址和端口即可。