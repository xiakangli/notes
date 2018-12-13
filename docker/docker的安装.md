# 1.安装依赖包
```
 $sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```
# 2.设置国内的docker源    (注意最后的链接也是命令的一部分)
```
$ sudoyum-config-manager \
    --add-repo \
http://mirrors.ustc.edu.cn/docker-ce/linux/centos/docker-ce.repo
```

# 3.安装docker
```
$ sudo yum makecachefast（这一步可能会出错，可以不用执行（我加的注释！！！））
$ sudoyum install docker-ce
```
# 4.设置加速
```
$curl -sSL https://get.daocloud.io/daotools/ set_mirror.sh|sh -s http://c3d2a40a.m.daocloud.io
```
# 5.其他操作
## 设置开机重启：
```
$ systemctl enable docker
```
## 重新加载配置并且重新启动
```
$sudo systemctl daemon-reload
$sudo systemctl restart docker
# 检查是否成功
sudo ps -ef | grep dockerd
```
# 6.ubuntu环境下的安装
参考链接：
https://blog.csdn.net/bingzhongdehuoyan/article/details/79411479





