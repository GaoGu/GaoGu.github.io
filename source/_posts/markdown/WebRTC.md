---
title: 基于socket.io和webRTC实现视频通话
date: 2018-05-11 15:35:12
categories:
- node
---
# WebRTC是什么
WebRTC是一个开源项目，旨在使得浏览器能为实时通信（RTC）提供简单的JavaScript接口。说的简单明了一点就是让浏览器提供JS的即时通信接口。这个接口所创立的信道并不是像WebSocket一样，打通一个浏览器与WebSocket服务器之间的通信，而是通过一系列的信令，建立一个浏览器与浏览器之间（peer-to-peer）的信道，这个信道可以发送任何数据，而不需要经过服务器。并且WebRTC通过实现MediaStream，通过浏览器调用设备的摄像头、话筒，使得浏览器之间可以传递音频和视频
# 参考文档
[WebRTC学习之一：开篇](https://blog.csdn.net/caoshangpa/article/details/53306992)

[WebRTC基于node的实例](https://blog.csdn.net/qq_24949727/article/details/68927202)

[WebRTC官网](https://webrtc.org/)