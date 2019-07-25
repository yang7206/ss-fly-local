### 自动部署到vultr

```# ss-fly-local```
使用本地文件进行安装部署，预防依赖的文件被删

在vultr的Startup Scripts 脚本下 新增boot脚本：
```
#!/bin/sh

cd /root
git clone https://github.com/yang7206/ss-fly-local.git
ss-fly-local/ss-fly.sh -ssr
```

使用ubuntu 18.04 安装完成后将会自动部署ssr服务器 ,大约需要等2 -3 分钟才能完成


### 修改配置
修改shadowsocksR.sh 文件下面的：
 pre_install方法中的 
 
 ```
 shadowsockspwd=密码
 shadowsocksport=端口号
 pick = 加密类型索引号
 protocol = 加密协议索引号
 shadowsockobfs = 混淆类型索引号
 ```
 
 
 ### 工具
 
 ssr工具 https://github.com/yang7206/ssr-file
