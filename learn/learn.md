#                         架构学习

[toc]

## redis备份恢复

redis架构：高并发，高可用，海量数据，备份，随时可恢复，缓存架构；首先redis就得支撑

## centos集群

### 环境配置

1.  winscp 主机与虚拟机交互

2. 配置网络

   vi /etc/sysconfig/network-scripts/ifcfg-eth0

   DEVICE=eth0
   TYPE=Ethernet
   ONBOOT=yes
   BOOTPROTO=dhcp
   service network restart
   ifconfig

   BOOTPROTO=static
   IPADDR=192.168.0.X
   NETMASK=255.255.255.0
   GATEWAY=192.168.0.1
   service network restart

3. 配置Hosts

​		vi /etc/hosts
​		配置本机的hostname到ip地址的映射

### perl

### CentOS为ssh免密码互相通信

1. 首先在三台机器上配置对本机的ssh免密码登录
   ssh-keygen -t rsa
   生成本机的公钥，过程中不断敲回车即可，ssh-keygen命令默认会将公钥放在/root/.ssh目录下
   cd /root/.ssh
   cp id_rsa.pub authorized_keys
   将公钥复制为authorized_keys文件，此时使用ssh连接本机就不需要输入密码了

2. 接着配置三台机器互相之间的ssh免密码登录
   使用ssh-copy-id -i hostname命令将本机的公钥拷贝到指定机器的authorized_keys文件中





