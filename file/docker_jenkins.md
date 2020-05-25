#1.安装docker
```
yum update

curl -sSL https://get.docker.com/ | sh

systemctl start docker

docker --version

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
