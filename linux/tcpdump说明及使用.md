# 1.tcpdump简介
tcpdump用于抓取网络包，可以过滤网络层（网卡）、协议、主机、网络或端口，并且可以使用and,or,not进行逻辑过滤
# 2.常用命令行式
```
tcpdump #抓取第一个网卡，一般为eth0上的所有包
```
```
tcpdump -i eth0 # -i用于指定网卡eth0 
```
```
# 这里的ip指的是IP协议，and表示抓两个主机
tcpdump -n ip host 192.168.51.188 and 192.168.51.164
# 扩展：获取51.188与51.164或者51.165主机之间的IP协议通信
tcpdump -n ip host 192.168.51.188 and \(192.168.51.164 or 192.168.51.165\)
```


```
tcpdump 
```
