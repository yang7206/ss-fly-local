# ss-fly-local
使用本地文件 进行安装，预防依赖的文件被删

自动部署到vultr

在vultr的Startup Scripts 脚本下 新增boot脚本：
#!/bin/sh

cd /root
git clone https://github.com/yang7206/ss-fly-local.git
ss-fly-local/ss-fly.sh -ssr


使用ubuntu 18.04 安装完成后将会自动部署ssr服务器 ,大约需要等2 -3 分钟才能完成