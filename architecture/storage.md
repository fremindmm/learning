## 存储专题
1. 存储系统必然涉及多个系统，而且是多个C/S模式的串联
    1. 拓扑
        1. S的最后端
            1. 介质
        2. C的最前端
            1. 应用
                1. 文件
                    1. 块文件
                    2. 普通文件
                2. 对象
                3. 定制化客户端
        3. 中间层
            1. 往往身兼多个角色
    2. 关系
        1. 服务型
            1. Customer-Waiter
                1. 主机使用存储服务
                2. 虚拟机使用存储服务
        2. 控制型
            1. Master-Slave Slave依然是为Master提供服务
                1. 主机控制磁盘
                2. 存储控制磁盘
2. 存储系统
    1. 组件
        1. 服务端技术 如何提供服务
            1. 介质 如何表示0和1
                1. 基于磁 HD
                2. 基于光 CD
                3. 基于电气 NAND
                4. 基于相变 PCM
            2. 磁盘级封装
                1. 介质编址
                2. 接口
                    1. 协议端点
                        1. 驱动器
                        2. 控制器
                    2. 协议内容
                        1. 通用协议指令
                            1. ATA
                            2. SCSI
                            3. VIRTIO
                        2. 定制协议指令
                    3. 传输链路
                        1. 磁盘线缆
                            1. SAS
                            2. SATA
                        2. 虚拟总线
                        3. 其他
                            1. 无线？
                    4. 控制流和数据流合一
            3. 半虚拟化级封装
                1. 按照格式编制
                2. 接口
                    1. 协议端点
                        1. 半虚拟化前端
                            1. Hypercall
                            2. IO指令陷入模拟
                        2. 半虚拟化后端
                    2. 协议内容
                        1. virtio协议
                        2. xenblk协议
                    3. 传输链路
                        1. 环形共享内存缓冲区
                    4. 控制流和数据流合一
            4. 服务级封装
                1. 设备编址
                2. 接口
                    1. 协议端点
                        1. HBA
                        2. HTTP
                        3. 自有协议
                    2. 协议内容
                        1. 存储指令封包
                        2. 控制协议封包
                    3. 传输链路
                        1. 存储网络
                    4. 管理方式
                        1. 带内服务，带内管理
                        2. 带内服务，带外管理
        2. 客户端技术 如何使用
            1. 物理设备抽象
                1. 线性地址LBA
                2. 块设备层
                    1. BIO接口层
                    2. IO调度框架
                    3. 具体驱动
                        1. SCSI语义
                            1. IO Handler
                            2. 设备管理发现
                                1. libata
                                2. libfc
                                3. libiscsi
                                4. libsas
                        2. NVMe语义
                            1. IO Handler
                            2. 设备管理发现
                                1. 热插拔驱动
                    4. 厂商专有硬件驱动
            2. 设备虚拟化 中间层技术
                1. 基于映射表 
                    1. 分区
                        1.  MBR和GPT
                    2. device mapper
                        1. 软RAID
                        2. 逻辑卷
                        3. 加密卷
                    3. 文件系统
                        1. VFS体系结构
                            1. 元数据组织
                            2. 页缓冲
                        2. 日志文件系统
                        3. 伪文件系统
                        4. 网络文件系统
                    4. 虚拟磁盘格式
                        1. 设备地址映射到数据文件地址
                            1. 直接映射
                                1. RAW格式
                            2. 间接映射
                                1. QCOW2格式
                2. 基于算法
                    1. RAID 5/6
                        1. 硬件实现
                3. 表和算法
                    1. rados
    2. 连接件
        1. 总线和通信
            1. 通信端点
                1. 客户端
                    1. 应用级别
                        1. 系统调用
                        2. HTTP Client
                        3. 订制Client
                            1. librbd、hdfs等
                    2. 主机级别
                        1. HBA卡
                            1. 存储协议HBA
                                1. SCSI HBA
                                2. ISCSI HBA
                                3. RAID卡
                                4. 硬盘控制器
                            2. 网络协议HBA
                                1. 以太网卡
                                2. IB卡
                                3. FC HBA
                                4. FCoE HBA
                    3. 存储设备
                        1. 磁盘驱动器
                    4. 存储服务
                        1. HBA卡
                            1. FC HBA
                            2. ISCSI HBA
                            3. FCoE HBA
                            4. 网卡
            2. 通信协议
                1. SCSI
                2. ATA
                3. NVMe
                4. FC
                5. TCP/IP
                6. Infiniband
            3. 协议分层融合
        2. 数据交换设备
            1. 网络交换机
                1. 以太网交换机
                2. FC交换机
3. 联成系统
    1. 网络拓扑
        1. 点对点
            1. ATA、virtio
        2. 总线型
            1. PCI
        3. 星型 交换
            1. SAS、PCI
        4. 链式
            1. SCSI
        5. 环状
            1. FC
        6. 网状
            1. IP
    2. 数据分布
        1. 系统级存储虚拟化
            1. 改变IO路径
                1. 数据分片 分
                2. 数据放置 布
                    1. 基于表
                        1. HDFS
                    2. 基于算法
                        1. 一致性哈希
                        2. EC
    3. 复制
        1. 目的
            1. 可靠性
                1. 主备
            2. 性能
                1. 负载均衡
        2. 方式
            1. 数据级别
                1. 多副本
            2. 盘级别
                1. RAID
            3. 链路级别
                1. 多路径
            4. 设备级别
                1. 多存储控制器
                2. 多卡
                3. 多交换机
            5. 应用级别
                1. 备份
            6. 系统级别
                1. 容灾
        3.  一致性
            1. 一致性协议
                1. CAP原理
            2. 分布式事务
                1. 2PC
                2. 3PC
                3. Paxos
4. 系统中几个关键问题
    1. 存储虚拟化
        1. 空间上的重新表示
            1. 对存储上的位置进行重新的分配，这样就需要用数据去表示数据，称为元数据
                1. 以文件或卷的形式抽象一组位置
                2. 进行多机存储资源的合并
                3. 利用分布式技术提高访问性能和可靠性
        2. 时间上的重新表示
            1. 业务场景下对数据一致性的放松
                1. Consistency，多副本弱一致性提高响应能力
                2. Coherence，对读写重排序来提高性能
            2. 记录一个时间点上，空间内所有位置的状态
                1. 基于日志重放实现容错
                2. 存储资源应当具有快照或者录像（CDP）的能力
            3. 重删和压缩
    2. 可靠性
        1. 空间
            1. 复制
            2. 分布
        2. 时间
    3. 性能
        1. 性能提高机制
            1. 缓存
            2. 复制
            3. 路径优化
            4. 硬件加速
        2. 性能排查和调优
            1. 性能指标
            2. 性能测试
    4. 版本管理
        1. 快照
            1. 写时复制技术
                1. 写前复制
                2. 写时复制
        2. 连续数据保护 CDP
    5. 容错
        1. 故障分类
            1. 瞬时故障
                1. 断电
                2. 断网
                3. 误操作
            2. 永久故障
                1. 损坏
                2. 灾难
        2. 故障处理
            1. 故障隔离
            2. 故障修复
                1. 可修复
                    1. 不修复
                    2. 日志重放
                    3. 回退快照
                2. 不可修复
                    1. 置为废弃
                    2. 启用副本
    6. IO路径分析调试
        1. 主机路径
        2. 虚拟化路径
5. 存储系统分类
    1. DAS
    2. SAN
        1. IP-SAN
        2. FC-SAN
            1. 高端存储阵列
                1. 细粒度软硬件解耦
    3. NAS
        1. NFS
        2. CIFS
    4. 对象存储架构
    5. 分布式文件系统
