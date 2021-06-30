# 升级文档

!!! warning "更新前请一定要做好备份工作"

### 升级步骤

!!! tip "操作步骤"
    ```sh
    cd /opt
    yum -y install wget
    wget https://github.com/rackshift/rackshift-installer/releases/download/{{ rackshift.version }}/rackshift-installer-{{ rackshift.version }}.tar.gz
    tar -xf rackshift-installer-{{ rackshift.version }}.tar.gz
    cd rackshift-installer-{{ rackshift.version }}
    ```
    ```sh
    ./rsctl.sh upgrade
    ```
    ```nginx hl_lines="1 30 63"
    是否将版本更新至 {{ rackshift.version }} ? (y/n)  (默认为 n): y

    1. 检查配置文件
    配置文件位置: /opt/rackshift/config
    /opt/rackshift/config/config.txt  [ √ ]
    完成

    2. 备份配置文件
    正在备份 /opt/rackshift/config/backup/config.txt.2021-06-30_16-21-51
    完成

    3. 升级镜像文件
    x-lab/mysql:5.7.31                  [ OK ]
    x-lab/mongo:latest                  [ OK ]
    x-lab/rabbitmq:management           [ OK ]
    x-lab/isc-dhcp-server:latest        [ OK ]
    x-lab/ipmitool:latest               [ OK ]
    x-lab/racadm-docker:latest          [ OK ]
    x-lab/rackshift-files:v1.0.0        [ OK ]
    x-lab/on-dhcp-proxy:v1.0.0          [ OK ]
    x-lab/on-http:v1.0.0                [ OK ]
    x-lab/on-syslog:v1.0.0              [ OK ]
    x-lab/rackshift-taskgraph:{{ rackshift.version }}    [ OK ]
    x-lab/on-tftp:v1.0.0                [ OK ]
    x-lab/rackshift:{{ rackshift.version }}              [ OK ]
    x-lab/rackshift-proxy:v1.0.0        [ OK ]
    x-lab/rackshift-plugins:{{ rackshift.version }}      [ OK ]

    4. 备份数据库
    检测到 RackShift 正在运行, 是否需要关闭并继续升级? (y/n)  (默认为 n): y

    Stopping rs_mongo_1 ... done
    Stopping rs_rabbitmq_1 ... done
    Stopping rs_files_1 ... done
    Stopping rs_dhcp-proxy_1 ... done
    Stopping rs_http_1 ... done
    Stopping rs_syslog_1 ... done
    Stopping rs_taskgraph_1 ... done
    Stopping rs_tftp_1 ... done
    Stopping rs_rackshift_1 ... done
    Stopping rs_rackshift-proxy_1 ... done
    Stopping rs_rackshift-plugins_1 ... done
    Removing rs_mongo_1 ... done
    Removing rs_rabbitmq_1 ... done
    Removing rs_dhcp_1 ... done
    Removing rs_files_1 ... done
    Removing rs_dhcp-proxy_1 ... done
    Removing rs_http_1 ... done
    Removing rs_syslog_1 ... done
    Removing rs_taskgraph_1 ... done
    Removing rs_tftp_1 ... done
    Removing rs_rackshift_1 ... done
    Removing rs_rackshift-proxy_1 ... done
    Removing rs_rackshift-plugins_1 ... done
    Removing rs_ipmitool_1 ... done
    Removing rs_racadm_1 ... done

    正在备份...
    mysqldump: [Warning] Using a password on the command line interface can be insecure.
    [SUCCESS] 备份成功! 备份文件已存放至: /opt/rackshift/db_backup/rackshift-2021-03-19_08:32:39.sql

    5. 清理镜像
    是否需要清理旧版本镜像文件? (y/n)  (默认为 n): y

    Untagged: x-lab/rackshift:v1.2.0
    Deleted: sha256:6a4fbff00b55e77362f3bd575fb28966583ee6698b33844e2a22d0049734e9bb
    Deleted: sha256:40fc9ba04fd6acbcb946cbedd67f2f284f902c2f4a086bd1e7f3067c8e90987e
    Deleted: sha256:acaf5e05c1e3868acda3884ab90319da3f3b817000e5f66d4ff1a462decbc5f9
    Deleted: sha256:8c95b890f1cec4874740a39a1a946618a6937c249aa45870cff1da64eea21ab5

    完成

    6. 升级成功, 可以重启程序了
    ./rsctl.sh start
    ```
    ```sh
    ./rsctl.sh start
    ```
