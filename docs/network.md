# 网络结构

![runnob](./static/wizard/rs-network.png)

!!! info "RackShift 网卡说明"
    - 管理：与 BMC 管理网络三层通信，通过该网络 RackShift 能控制物理机的 PXE 启动等行为
    - PXE ： 与 物理机 PXE 网口直连，通过该网络 RackShift 能下发 PXE 过程中需要的文件