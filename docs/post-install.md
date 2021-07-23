# Post-Install 脚本

## 定义

* The %post script is a post-installation script that is run after the installation is complete, but before the system
  is rebooted for the first time.
* You can add multiple %post install scripts in a Kickstart
* All the Kickstart post install script must start with %post and end with %end line
* All Kickstart post install scripts by default execute in chroot environment

## 示例

* 设置 yum 源

````
    cd /etc/yum.repos.d
    rm -rf *
    echo -e "[base]" > centos.repo
    echo -e "baseurl=ftp://192.168.100.10/centos7" >> centos.repo
    echo -e "gpgcheck=0" >> centos.repo
````

* 设置 DNS

````
    echo -e "nameserver=192.168.1.1" >> /etc/resolv.conf
````

* 基线脚本

```
    wget -O /tmp/bl.sh http://192.168.1.1/common/base_line.sh
    echo "/bin/bash /tmp/bl.sh" >> /etc/rc.d/rc.local
    chmod +x /etc/rc.d/rc.local
```

!!! warn "注意"
  RackShift Post-Install 脚本默认不带 --nochroot 参数