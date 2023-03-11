# go-environment
基于docker的go-zero 本地运行环境
## 使用
1.根据需要修改env配置
~~~env
    #__ 网络设置
    NETWORKS_DRIVER=bridge
    
    #__ 时区设置
    TZ = Asia/Shanghai
    
    #__ PATHS 本机路径映射 #########################
    # 代码路径
    CODE_PATH =./../app
    # 数据库缓存等存储路径
    DATA_PATH_HOST=./data
    
    #__ mysql 本机映射 ##################################
    MYSQL_PORT=3306
    MYSQL_USERNAME=admin
    MYSQL_PASSWORD=123456
    MYSQL_ROOT_PASSWORD=123456
    
    # Mysql 可视化管理用户名称，同 MYSQL_USERNAME
    MYSQL_MANAGE_USERNAME=admin
    # Mysql 可视化管理用户密码，同 MYSQL_PASSWORD
    MYSQL_MANAGE_PASSWORD=123456
    # Mysql 可视化管理ROOT用户密码，同 MYSQL_ROOT_PASSWORD
    MYSQL_MANAGE_ROOT_PASSWORD=123456
    # Mysql 服务地址
    MYSQL_MANAGE_CONNECT_HOST=mysql
    # Mysql 服务端口号
    MYSQL_MANAGE_CONNECT_PORT=3306
    
    # Mysql 可视化管理映射宿主机端口号，可在宿主机127.0.0.1:1000访问
    MYSQL_MANAGE_PORT=1000
    #__ REDIS ##########################################
    # Redis 服务映射宿主机端口号，可在宿主机127.0.0.1:6379访问
    REDIS_PORT=6379
    
    # Redis 可视化管理用户名称
    REDIS_MANAGE_USERNAME=admin
    # Redis 可视化管理用户密码
    REDIS_MANAGE_PASSWORD=123456
    # Redis 服务地址
    REDIS_MANAGE_CONNECT_HOST=redis
    # Redis 服务端口号
    REDIS_MANAGE_CONNECT_PORT=6379
    # Redis 可视化管理映射宿主机端口号，可在宿主机127.0.0.1:2000访问
    REDIS_MANAGE_PORT=2000
    
    #__ Etcd 服务映射宿主机端口号，可在宿主机127.0.0.1:2379访问
    ETCD_PORT=2379
    
    ETCD_MANAGE_PORT=7000
    ETCD_ROOT_PASSWORD=123456
    
    #__ PROMETHEUS #####################################
    # Prometheus 服务映射宿主机端口号，可在宿主机127.0.0.1:3000访问
    PROMETHEUS_PORT=3000
    
    
    #__ GRAFANA ########################################
    # Grafana 服务映射宿主机端口号，可在宿主机127.0.0.1:4000访问
    GRAFANA_PORT=4000
    
    
    #__ JAEGER #########################################
    # Jaeger 服务映射宿主机端口号，可在宿主机127.0.0.1:5000访问
    JAEGER_PORT=5000
    
    
    #__ DTM #########################################
    # DTM HTTP 协议端口号
    DTM_HTTP_PORT=36789
    # DTM gRPC 协议端口号
    DTM_GRPC_PORT=36790
~~~
2.启动方式
~~~Start
    docker compose up -d
~~~
3.项目存放路径 `CODE_PATH_HOST` go-zero代码

4.数据库信息统一存放于`data`目录下