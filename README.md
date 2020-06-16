# Nemo

<img src="docs/nemo.jpg" alt="nemo" align="left"/>

Nemo（尼莫）是《海底总动员》中的一只可爱的小丑鱼。

Nemo的初衷是用来进行自动化信息收集的一个简单平台，实现对内网及互联网资产信息的自动收集。

## 


## 功能

主要实现了以下功能（代码目前在完善和优化中...）

- 采用Nmap进行端口扫描（需本地nmap）
- 端口标题查询
- 通过第三方接口查询IP归属地
- 调用Sublist3r实现子域名收集
- 调用Fofa的API接口对IP和域名信息收集（需要Fofa的KEY）
- 调用WhatWeb收集端口和域名的指纹（需本地whatweb）
- Celery实现分布式任务
- Docker部署和运行



## Docker运行

```shell
git clone https://github.com/hanc00l/nemo
cd nemo
docker build  -t nemo/app:v1 .
docker run -it -d --name nemo_app -p 5000:5000 nemo/app:v1
```

浏览器输入 [http://localhost:5000](http://localhost:5000)，默认用户名密码：**nemo/nemo**


<img src="docs/login.jpg" alt="login" />

<img src="docs/dashbord.jpg" alt="dashbord"  />



[开发环境配置](docs/config.md)



## 目标

最终做成像FOFA一样的信息收集平台。



## 参考

jeffzh3ng：https://github.com/jeffzh3ng/fuxi

TideSec：https://github.com/TideSec/Mars