# 准备工作
  以浪潮 5280M4 为例

## 部署 RackShift
- 通过 [快速开始](quick_start.md) 提供的方式部署 RackShift

## 配置 PXE 使用的 DHCP 网段
![runnob](./static/wizard/subnet.jpg) 

!!! warning "注意"
    - 此处配置的 IP 地址段必须是 RackShift 的网卡所在的 PXE 网卡所在的地址段
    - 如果配置安装时配置服务器 IP 错误可以使用 rsctl reconfig 命令重设 IP 地址
    - 用户部署的 RackShift 服务器至少有一张网卡与物理机 PXE 网卡是直连。并且配置开启 PXE 的 DHCP 网段必须和该网卡处于同一段。
    - 用于 PXE 的网络中不能存有其他 DHCP 服务器。
      
        
## 上传用于装机的 Centos7.X 镜像
![runnob](./static/wizard/image.jpg)

!!! warning "注意"
    等待镜像上传完毕之后点击“提交/确定”按钮
     

