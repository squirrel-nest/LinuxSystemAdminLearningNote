# 网络管理
## 防火墙
   * 命令帮助
      - firewall-cmd --help
      - man firewall-cmd
   * 端口管理
      + 查询命令
         - 查询区域(zone)相关信息
            * 方法 - 命令帮助 --> Zone Options
               + --get-default-zone   Print default zone for connections and interfaces
               + --get-active-zones   Print currently active zones
               + --get-zones          Print predefined zones [P]
               + --list-all-zones     List everything added for or enabled in all zones [P]
               + 用来切换默认zone的命令
                  -  --zone=<zone>        Use this zone to set or query options, else default zone
                       Usable for options marked with [Z]
         ```
              firewall-cmd --list-all
         ```
         - 查询已设置的端口 - 非管理账号,需要 sudo
         ```
             [sudo] firewall-cmd --list-ports
         ```
      + 添加端口命令
         - 临时端口的添加
         ```
            firewall-cmd --add-port=443/tcp
         ```
         - 永久端口的添加
         ```
            firewall-cmd --permanent --add-port=443/tcp
         ```
         - 不同点
            1. 临时端口添加完, 立即生效, 永久端口添加后,不会立即生效,需要reload或防火墙服务要重启...
            ```shell
               firewall-cmd --reload
            ```
            2. ...
# 文件和文件夹的基本操作
   * 文件或文件夹的创建
      + 文件夹的创建
      + 文件的创建
   * 更改拥有者
   * 更改权限
