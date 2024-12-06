---
slug: 20241206
title: "在容器里部署clash"
date: 2024-12-06T21:33:01+08:00
description: "在容器里部署clash"
tags:
    - docker
    - clash
layoutBackgroundHeaderSpace: false
---


1. [下载 clash ](https://github.com/DustinWin/clash_singbox-tools/releases/tag/Clash-Premium)，解压， 将文件命名为 `clash`
    - 注：一般个人的64位电脑下载 `amd64` 的即可。
4. `chmod +x clash `
5. [下载 Country.mmdb ](https://github.com/Loyalsoldier/geoip/releases)
6. 下载配置文件 `wget -O config.yaml 订阅链接`
    - 默认监听的是 `127.0.0.1：7890`  
    - 修改 `allow-lan` 值为 `true` 后改为监听 `0.0.0.0`
    - **容器里执行clash的话必须修改上面的 `allow-lan`**
8. 将 `config.yaml `和 `country.mmdb` 都 copy 到 `config` 目录
9. `./clash` 即可运行
