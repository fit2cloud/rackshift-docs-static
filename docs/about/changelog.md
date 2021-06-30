# 更新日志

v1.3.0
------------------------
2021年06月29日

!!! info "🌱 新功能 Features"
    - feat: CentOS 支持自定义 LVM
    - feat: 支持 WindowsServer 2019 安装
    - feat: 支持 Ubuntu20.04 LiveCD subiquity 安装
    - feat: 支持 H3C RAID
    - feat: 支持 SuperMicro 服务器的发现

!!! summary "🚀 性能优化 Optimization"
    - feat: 优化安装包大小
    - feat: 兼容无带外 Ip 机器发现
    - feat: 可以查看任务的执行参数

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 发现机器后有时候没有自动填入带外信息
    - fix: 裸金属侧边栏无法关闭


v1.2.0
------------------------
2021年05月25日

!!! info "🌱 新功能 Features"
    - feat: 华为交换机管理
    - feat: 支持 AK/SK 外部访问
    - feat: 重构 API 外部调用接口
    - feat: 对接 FIT2CLOUD CloudExplorer 3.0 物理机模块

!!! summary "🚀 性能优化 Optimization"
    - feat: 裸金属服务器发现速度

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 华三机器发现不了的问题

v1.1.0
------------------------
2021年04月29日

!!! info "🌱 新功能 Features"
    - feat: WindowsServer 2016 安装
    - feat: ESXi 6.7 安装
    - feat: CentOS Minimal 版本安装
    - feat: CentOS/RHEL 多网卡 IP/ VLAN 配置
    - feat: CentOS 多网卡链路聚合 BOND4 802.3ad / VLAN

!!! summary "🚀 性能优化 Optimization"
    - feat: 删除任务状态变化慢的问题
    - feat: 指定删除 Ubuntu 网卡的问题

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 插件选择物理机页面分页问题
    - fix: 任务列表查询显示重复问题
    - fix: 插件镜像问题
    - fix: Ubuntu 自定义分区报错问题


v1.0.1
------------------------
2021年04月08日

!!! info "🌱 新功能 Features"
    - feat: Ubuntu 18.04 安装
    - feat: 批量修改 IPMI 密码
    - feat: 装机支持外部 repo

!!! summary "🚀 性能优化 Optimization"
    - feat: 系统日志打印
    - feat: 后端国际化

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: DHCP 服务重启故障
    - fix: 自定义分区单位切换故障
