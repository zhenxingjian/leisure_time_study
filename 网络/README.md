# 网络

最开始想要研究网络相关的各种东西，主要是三个想法吧。

1. 在奥运期间，发现美国这边转播的和我想看的都不重合（比如羽毛球，美国这边就不怎么播），那个时候想看的奥运的话，只能依赖 [穿梭](https://www.transocks.com). 
但是由于大家都在用，（并且没有买会员），导致网速嘛，只能说看1080都卡。
2. 刷 [B站](https://www.bilibili.com/anime/) 番的时候，好多时候提醒版权限制。虽然这个可以通过别的方式解决（比如某些国内墙的网站，或者pt站下载），但是不能同步看弹幕还是一大损失的。
比如 [间谍过家家](https://www.bilibili.com/bangumi/play/ep511580?from_spmid=666.25.episode.0) 阿妮亚名场面 \doge
3. 在国内，科学访问互联网已经是刚需了，没有 [google scholar](https://scholar.google.com)，大写加粗的 **GG**

综合以上考量，最早在研究VPN相关的。但是一是听说VPN会被墙的厉害，再有就是之前在国内尝试访问纯自建自用VPN的时候，网速特别卡顿
（可能主要是因为从synology 走了 quickconnect 服务器，导致网速本来就受限制，但是当时不懂）。
在某一次瞎翻youtube视频的时候，看到了有人在讲 
[v2ray](https://www.v2ray.com)， [shadowsocks(SS)](https://github.com/shadowsocks)，
[小火箭](https://apps.apple.com/us/app/shadowrocket/id932747118)， 
[小狮子](https://merlinblog.xyz/wiki/clash-for-windows-for-mac.html)，之类的东西，瞬间感兴趣。

但是这些依赖一个前提，拥有一个外网服务器（买/租），或者用别人已经搭建好的 [机场](https://www.jingyanpal.com/what-is-jichang-ss-ssr-is-it-the-same-as-vpn-service-an-explainer/)。
租一个海外服务器，对于肉身翻墙的人来说没什么吸引力，而在国内租个轻量化服务器（腾讯云/阿里云）之类的，带宽又极其受限制（通常在2M-6M，而同样的云服务，在香港平台就是30M-50M，简直坑）。
用别人的“机场”又担心隐私安全问题，所以想着不如自己研究研究能不能自己搭一个服务器。

一拖再拖之后，某次契机，开始在NAS上运行docker，突然意识到，我可以在docker里装一个v2ray服务器，远程访问自己的NAS。
同时，（并不是广告）发现腾讯云的活动，一年6M的轻量化服务器120RMB，想着可以试一下，一顿饭钱用一年，体验一下。
于是开始了进阶的折腾。

## 端口转发
### 起因
研究端口转发的原因，是在covid-19疫情开始之后，恰逢实验室新购置了两个台式机（我和我室友各一个），老板又允许我们暂时把主机搬回公寓方便工作，所以公寓里多了两台ubuntu主机，并一直持续了2年+。
但是由于偶尔出门，需要远程访问自己的主机，最开始用 [TeamViewer](https://www.teamviewer.com/en-us/)，用过的人都知道有多卡，根本没法用来coding。
当时的解决方案是 [ngrok](https://ngrok.com)，最后可以用ngrok ssh 远程访问主机，有点延时但是可以接受，并且直接操作命令行也比较习惯，所以用了一阵子。ngrok的痛点在于，要定期重新运行ngrok程序，并且每次重启电脑的话要重新运行，每次运行的时候，参数又不一样，只能每次先TeamViewer看一眼/打开ngrok，再ssh。

### 设置

## 软路由
## 自建代理服务器
## 代理客户端
