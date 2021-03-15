# 欢迎来到 RackShift ！

RackShift 是开源的裸金属全生命周期管理平台，功能覆盖裸金属服务器的发现、带外管理、RAID 配置、固件更新、操作系统安装等。 RackShift 遵循 GPL v2 开源协议，使用 SpringBoot/Vue
进行开发，界面美观、用户体验好，集成并扩展 RackHD，支持的X86 服务器品牌包括浪潮、戴尔、华为、联想、惠普等。

## 已支持机型

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

<tr>
<td>华为</td>
<td></td>
</tr>

</tbody>
</table>

## 界面展示

* 物理机
  ![runnob](static/wizard/main.jpg)
* RAID
  ![runnob](static/wizard/raid.jpg)
* 装机
  ![runnob](static/wizard/centos.jpg)

## 技术栈

- 前端: [Vue.js](https://vuejs.org/)
- 后端: [Spring Boot](https://www.tutorialspoint.com/spring_boot/spring_boot_introduction.htm)
- 数据库: [MySQL](https://www.mysql.com/)

## 致谢

- [RackHD](https://rackhd.github.io/)：感谢 RackHD 提供的底层实现；
- [MAAS](https://maas.io/)：感谢 MAAS 提供的生命周期纳管思路；
- [Digital Rebar](https://rackn.com/rebar/)：感谢 Digital Rebar 提供的操作方式和 UI 参考；
- [Element](https://element.eleme.cn/#/)：感谢 Element 提供的优秀组件库。