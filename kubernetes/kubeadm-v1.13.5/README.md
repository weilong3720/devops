# 配置集群信息cluster-info

``` shell
# 创建集群信息文件
$ cat ./cluster-info
CP0_IP=10.3.78.180
CP1_IP=10.3.78.181
CP2_IP=10.3.78.182
VIP=10.3.78.180
NET_IF=eth0
CIDR=172.18.0.0/16

```

## 初始化主机,每台主机都需运行

``` shell
./init_host.sh
```

## 运行

``` shell
./kubeadm-ha.sh
```

## 生成token

``` shell
kubeadm token create --print-join-command
```

