# 系统架构

## 软件分层
![runnob](https://f2c-south.oss-cn-shenzhen.aliyuncs.com/RackHD-dont-del/RackShift/rackshift-struc.jpg)

组件说明：

- RackShift-WEB： 基于 VUE2.6.11 开发的单页应用
- RackShift-Server： 基于 SSM 的 SpringBoot 应用，对 RackHD 的操作进行更高的抽象并且控制与 RackHD API的交互，控制 RackShift-Proxy 节点，与 RackShift-WEB 一并打包成一个应用部署
- RackShift-Proxy： 可单独与 RackHD 模块部署，主要用于主节点控制客户节点进行注入镜像下发，DHCP 配置，远程 KVM 等等
- RackHD： DELL EMC 开源的裸金属供应软件，现已停止维护
- Mysql：RackShift-Server 主要运行数据的存储区
- Mongo：RackHD 与RackShift-Server 的运行数据存储区
- RabbitMQ： 各组件之间通信的中间件
- DockerEngine：各组件都是以 Docker 容器运行在节点计算机

## 组件调用关系
![runoob](https://f2c-south.oss-cn-shenzhen.aliyuncs.com/RackHD-dont-del/RackShift/rs-call2.jpg)
