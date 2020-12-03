# 欢迎来到 RackShift ！

  RackShift 是一款开源的裸金属服务器全生命周期平台，功能覆盖裸金属（物理机）的上架、RAID 配置、固件升级、操作系统安装、中间件部署等。  
 
## 项目的起源
    在作者的一次项目中需要实现大批量物理机的自助装机，对比了 「RackN」，「MAAS」，「cloudboot」
    等多款国内外优秀开源装机项目后，我们选型 「RackHD」 并且在现有的基础之上增加了更多机型
    支持以及开发了基于带外特定品牌机型的爬虫用于爬取硬件信息。RackShift 就在各种机缘之中诞生了。
    
## 机型支持情况
<table>
<thead>
<tr><td>品牌</td><td>已支持型号</td><td>将支持型号</td></tr>
</thead>
<tbody>
<tr>
<td>DELL EMC</td>
<td>Power Edge R630 R640 R720 R730 R740 R910 R920 R930系列</td>
<td>Power Edge T 系列</td>
</tr>
<tr>
<td>HPE</td>
<td>Proliant 380 580 Gen8 Gen 9 Gen 10 系列</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>Inspur</td>
<td>5280 8480 M4 M5 系列</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>IBM</td>
<td>X3550 X3650 M4 系列</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>H3C</td>
<td>R4900 G3 系列</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>ZTE</td>
<td>R5300 G4 系列</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>华为</td>
<td></td>
<td>2280 V5系列</td>
</tr>

</tbody>
</table>

## 界面展示
* 物理机
![runnob](static/wizard/pm1.jpg)
* RAID
![runnob](static/wizard/raid.jpg)
* 装机
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