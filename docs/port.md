# 端口释义
| 端口 | 协议|运行的容器 | 服务说明 |
| :-----| :---- |:---- | :---- |
| 8082 | TCP | rackshift | WEB 界面 |
| 9030 | TCP | rackshift | 与装机有关的 Http 接口，用于和 PXE 引导之后运行的 Agent 通信 |
| 9090| TCP | http | 用于下载镜像和静态文件的服务,默认的挂载路径是宿主机的 /opt/rackshift/rackhd/files/mount/common|
| 4011 | UDP | dhcp-proxy-new | 用 netty 写的 DHCP 代理服务，监听 4011 UDP 端口，PXE 客户机将从此请求引导文件 |
| 69 | TFTP | tftp | 用于下载 PXE 过程中的 ipxe 固件 |
