# 1.安装docker
```
#更新yum工具包
yum update

#下载docker
curl -sSL https://get.docker.com/ | sh

#启动docker
systemctl start docker

#查看docker版本
docker --version

#设置开机自启动
systemctl enable docker

#配置docker加速器
cp /lib/systemd/system/docker.service /etc/systemd/system/docker.service
chmod 777 /etc/systemd/system/docker.service
vim /etc/systemd/system/docker.service
ExecStart=/usr/bin/dockerd --registry-mirror=https://kfp63jaj.mirror.aliyuncs.com
systemctl daemon-reload
systemctl restart docker
ps -ef | grep docker

```
