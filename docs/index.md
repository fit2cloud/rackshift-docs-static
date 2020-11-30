# 欢迎来到 RackShift ！

  RackShift 是一款开源的裸金属服务器全生命周期平台，功能覆盖裸金属（物理机）的上架、RAID 配置、固件升级、操作系统安装、中间件部署等。  
 

## 初心和使命
    实现大批量裸金属服务器自动化装机，RAID，固件刷新
        
## 项目的起源
    在对比国内外开源的 RackHD，MAAS，RackN，CloudBoot 等一系列开源软件之后，我们可以感受
    到每种工具的优势与不足，我们决定基于工程质量最高和功能完整度最全的 RackHD 进行一定的“魔改”
    以使得其适配更多的机型（官网支持机型只有DELL EMC, Cisco， White Box 等几个有限的型号 ）
    ，于是 RackShift 诞生了！ 
    
## 已经支持 RAID，装机的机型
<table>
<thead>
<tr><td>品牌</td><td>型号</td></tr>
</thead>
<tbody>
<tr>
<td>DELL EMC</td>
<td>Power Edge R630 R640 R720 R730 R740 R910 R920 R930系列</td>
</tr>
<tr>
<td>HPE</td>
<td>Proliant 380 580 Gen8 Gen 9 Gen 10 系列</td>
</tr>

<tr>
<td>Inspur</td>
<td>5280 8480 M4 M5 系列</td>
</tr>

<tr>
<td>IBM</td>
<td>X3550 X3650 M4 系列</td>
</tr>

<tr>
<td>H3C</td>
<td>R4900 G3 系列</td>
</tr>

<tr>
<td>ZTE</td>
<td>R5300 G4 系列</td>
</tr>

</tbody>
</table>

## 准备支持的机型

<table>
<thead>
<tr><td>品牌</td><td>型号</td></tr>
</thead>
<tbody>
<tr>
<td>DELL EMC</td>
<td>Power Edge T 系列</td>
</tr>

<tr>
<td>华为</td>
<td>2280 V5系列</td>
</tr>

<tr>
<td>其他国产品牌</td>
<td>飞腾，龙芯等 UEFI 引导装机</td>
</tr>

<tr>
<td>ARM</td>
<td>国产 ARM 系列机型</td>
</tr>

</tbody>
</table>

### 随着项目的开源，后续还会支持越来越多的机型

## 界面展示
1. 物理机
![runnob](static/wizard/pm1.jpg)
2. 做 RAID
![runnob](static/wizard/raid.jpg)
3. 装机
![runnob](static/wizard/centos.jpg)

## 技术栈

- 前端: [Vue.js](https://vuejs.org/)
- 后端: [Spring Boot](https://www.tutorialspoint.com/spring_boot/spring_boot_introduction.htm)
- 数据库: [MySQL](https://www.mysql.com/)

## 致谢

-  [RackHD](https://rackhd.github.io/)：感谢 RackHD 提供的底层实现；
-  [MAAS](https://maas.io/)：感谢 MAAS 提供的生命周期纳管思路；
-  [Digital Rebar](https://rackn.com/rebar/)：感谢 Digital Rebar 提供的操作方式和 UI 参考；
-  [Element](https://element.eleme.cn/#/)：感谢 Element 提供的优秀组件库。