# 安装文档

!!! info "说明"
    全新安装的 Linux(x64)  
    需要连接 互联网  
    使用 root 用户执行

## 安装方式

!!! info "外置环境要求"
    - 推荐使用外置 数据库, 方便日后扩展升级

| DB      | Version |
| :------ | :------ |
| MySQL   | >= 5.7  |
| MariaDB | >= 10.2 |


=== "自动部署"
    !!! tip ""
        ```sh
        curl -sSL https://github.com/rackshift/rackshift/releases/download/{{ rackshift.version }}/quick_start.sh | bash
        ```

=== "手动部署"
    !!! tip ""
        ```sh
        cd /opt
        wget https://github.com/rackshift/rackshift-installer/releases/download/{{ rackshift.version }}/rackshift-installer-{{ rackshift.version }}.tar.gz
        tar -xf rackshift-installer-{{ rackshift.version }}.tar.gz
        cd rackshift-installer-{{ rackshift.version }}
        cat config-example.txt
        ```

    ???+ info "配置文件说明"
        ```vim
        # 以下设置如果为空系统会自动生成随机字符串填入

        ## 安装配置, RACKSHIFT_IP 填写用作 PXE 的网卡 IP
        DOCKER_IMAGE_PREFIX=registry.cn-qingdao.aliyuncs.com
        VOLUME_DIR=/opt/rackshift
        DOCKER_DIR=/var/lib/docker
        RACKSHIFT_IP=

        ## Compose 项目设置
        COMPOSE_PROJECT_NAME=rs
        COMPOSE_HTTP_TIMEOUT=3600
        DOCKER_CLIENT_TIMEOUT=3600

        ##  MySQL 配置, USE_EXTERNAL_MYSQL=1 表示使用外置数据库, 请输入正确的 MySQL 信息
        USE_EXTERNAL_MYSQL=0
        DB_HOST=mysql
        DB_PORT=3306
        DB_USER=root
        DB_PASSWORD=
        DB_NAME=rackshift

        ## Service 端口
        HTTP_PORT=80

        # 额外的配置
        CURRENT_VERSION=
        ```

=== "离线部署"

    | 下载地址                                                                                                                                                | 密码 |
    | :----------------------------------------------------------------------------------------------------------------------------------------------------- | :--- |
    | [百度云盘](https://pan.baidu.com/s/1P-R4U2zTw9xfsRshfEqd3A)                                                                                             | nmbz |
    | [阿里云 OSS](https://fit2cloud2-offline-installer.oss-cn-beijing.aliyuncs.com/rackshift/rackshift-release-{{ rackshift.version }}-offline.zip) |      |

    下载完成后，上传到 linux 服务器 /opt 目录进行解压

    !!! tip ""
        ```bash
        unzip rackshift-release-{{ rackshift.version }}-offline.zip
        cd rackshift-release-{{ rackshift.version }}-offline
        ./rsctl.sh install
        ```

## 使用方式

- 安装目录 /opt/rackshift-installer-{{ rackshift.version }}
- 配置文件 /opt/rackshift/config/config.txt

!!! tip "安装"
    ```sh
    ./rsctl.sh install
    ```

!!! tip "启动"
    ```sh
    ./rsctl.sh start
    ```

!!! tip "关闭"
    ```sh
    ./rsctl.sh down
    ```

!!! tip "帮助"
    ```sh
    ./rsctl.sh -h
    ```
