## 软件开发专题
1. 软件开发 =  代码 + 程序 + 环境 + 工程管理
2. 程序语言
    1. 分类
        1. 命令式语言
            1. 脚本式语言
        2. 函数式语言
        3. 面向对象语言
        4. 说明式语言
            1. 逻辑式语言
            2. 关系式语言
            3. 基于限制的语言
    2. 程序运行原理
        1. 过程管理
            1. 编译
            2. 链接
            3. 加载
            4. 执行
        2. 解释
        3. 高级语言虚拟机
    3. 开发
        1. 编程范型
            1. 面向过程编程
            2. 面向对象编程
            3. 函数式的编程
        2. 库和框架
        3. 设计模式
            1. 创建型模式
            2. 结构型模式
            3. 行为型模式
        4. 软件架构
            1. 架构视图
                1. 逻辑架构
                2. 运行架构
                3. 开发架构
                4. 数据架构
                5. 物理架构
            2. 架构风格
            3. 特定领域软件架构 DSSA
            4. 基于构件开发
            5. 架构评估
            6. 架构演化
        5. 软件测试
            1. 单元测试
            2. 集成测试
            3. 系统测试
            4. 测试自动化
    4. 软件自动化
        1. 软件建模
        2. 模型驱动
            1. 形式化证明
            2. 代码生成
3. 程序 = 算法 + 数据
    1. 数据结构
        1. 线性表
            1. 链表
            2. 数组
        2. 树
        3. 图
        4. 散列
    2. 数据库
        1. 数据库系统
            1. 数据库
            2. 数据库管理系统 DBMS
                1. 数据定义
                    1. 数据定义语言DDL
                2. 数据操纵 
                    1. 数据操纵语言 DML
                    2. 基本操作
                        1. 增删查改
                3. 运行管理
                    1. 安全性 完整性
                    2. 并发访问
                    3. 故障恢复
                4. 建立和维护
            3. 应用系统
            4. DBA
        2. 数据视图
            1. 数据库模式
                1. 型与值
            2. 三级模式两级映像
                1. 物理模式（存储模式，内模式）
                    1. 数据的物理结构及存储方式
                2. 逻辑模式（模式）
                    1. 数据库全体数据的全局逻辑结构和特性描述
                3. 子模式（外模式）
                    1. 用户的数据视图
                4. 外模式 / 模式映像
                5. 模式 / 内模式映像
        3. 数据模型
            1. 组成要素
                1. 数据结构
                2. 数据操作
                3. 数据的约束条件
            2. 分类
                1. 关系模型
                    1. 关系代数
                    2. 关系演算
                    3. 关系数据库设计
                        1. 数据库范式
                2. 实体-联系模型
                    1. ER图
                        1. 转换为关系模式
                3. 基于对象数据模型
                4. 半结构化数据模型
        4. SQL
        5. 事务管理
        6. 分布式数据库
    3. 数据挖掘
    4. 算法 离散数学、运筹学、概率论
        1. 算法分析
            1. 计算复杂性
        2. 算法应用
            1. 基础方法：分治、动态规划、贪心、回溯、分枝定界
            2. 高级方法：近似算法、随机化算法、启发式算法、神经网络
            3. 基础算法：表、树、图算法
            4. 关键问题：查找、排序、匹配
        3. 分布式算法
4. 环境 系统软件
    1. 编译环境
        1. 编译原理
            1. 基本概念
                1. 编译与解释
            2. 编译程序的组成
                1. 源程序到目标程序
                    1. 词法分析器
                    2. 语法分析器
                    3. 语义分析器
                    4. 中间代码生成器
                    5. 代码优化器
                    6. 代码生成器
                2. 辅助组件
                    1. 符号表管理
                    2. 出错管理
            3. 语法
                1. 文法
                    1. 作用
                        1. 对语言结构的定义与描述
                    2. 定义
                        1. 终结符号集
                        2. 非终结符号集
                        3. 规则（产生式）的集合
                        4. 开始符号
                    3. 分类
                        1. 0型文法 短语结构文法
                            1. L0型语言
                                1. 图灵机接受
                        2. 1型文法 上下文有关文法
                            1. L1型语言
                                1. 线性界限自动机
                        3. 2型文法 上下文无关文法
                            1. L2型文法
                                1. 下推自动机
                        4. 3型文法 正则文法
                            1. L3型文法
                                1. 有穷自动机
                2. 语法规则
                    1. 产生式
                3. 推导
                4. 语法树
            4. 关键步骤
                1. 词法分析
                    1. 符号表
                    2. 正规文法
                    3. 有穷自动机
                2. 语法分析
                3. 语义分析
                4. 中间代码生成
                    1. 抽象语法树
                5. 代码优化
                6. 目标代码生成
    2. 运行环境
        1. 操作系统
            1. 操作系统历史
                1. 无操作系统
                2. 单道批处理系统
                3. 多道批处理系统
                4. 分时系统
                5. 实时系统
            2. 操作系统架构
                1. 分层设计
                    1. 用户态
                    2. 内核态
                        1. 服务化
                    3. 接口
                2. 高质量服务
                    1. 多路复用
                    2. 隔离
                    3. 协作
                3. 技术路线
                    1. 微内核架构
                    2. 宏内核架构
                    3. 外内核
            3. 进程管理
                1. 进程概念
                    1. PCB结构
                        1. 进程标识符
                        2. 处理器上下文
                        3. 调度信息
                            1. 进程状态
                            2. 优先级
                            3. 调度信息
                            4. 状态信息
                        4. 控制信息
                            1. 程序和数据地址
                        5. PCB组织
                            1. 链式
                            2. 索引
                    2. 进程状态
                2. 进程控制
                    1. 创建
                    2. 终止
                    3. 阻塞和唤醒
                    4. 挂起与激活
                3. 进程同步
                    1. 临界资源和临界区
                    2. 遵循规则
                        1. 空闲让进
                        2. 忙则等待
                        3. 有限等待
                        4. 让权等待
                    3. 信号量
                    4. 管程
                    5. 经典问题
                        1. 生产者-消费者问题
                        2. 哲学家就餐问题
                        3. 读者-写者问题
                4. 进程通信
                    1. 共享存储器
                        1. 共享数据结构
                        2. 共享存储区
                    2. 消息传递
                        1. 直接通信
                            1. socket
                        2. 间接通信
                            1. 邮箱
                    3. 管道
                5. 线程
                    1. 实现方式
                        1. 内核支持
                        2. 用户级线程
                        3. 组合方式
                    2. 用户线程和内核线程模型
                        1. 一对一
                        2. 多对一
                        3. 多对多
            4. 进程调度
                1. 调度组件
                    1. 进程上下文切换
                    2. 排队器
                    3. 分派器
                2. 调度算法
                3. 实时调度
                    1. 抢占
                4. 死锁
                    1. 产生死锁必要条件
                        1. 互斥
                        2. 请求和保持
                        3. 不剥夺
                        4. 环路等待
                    2. 处理方法
                        1. 预防
                        2. 避免
                            1. 银行家算法
                        3. 检测
                        4. 解除
            5. 内存管理
                1. 多级存储结构
                    1. 局部性原理
                        1. 时间局部性
                        2. 空间局部性
                2. 进程内存结构
                    1. 程序链接
                        1. 静态链接
                        2. 动态链接
                            1. 位置无关的代码
                    2. 程序装载
                3. 内存分配 物理内存
                    1. 单一连续分配
                    2. 固定分配
                    3. 动态分区分配
                        1. 空闲表
                        2. 分配算法
                        3. 内存碎片的问题
                            1. 内碎片
                            2. 外碎片
                    4. 伙伴系统
                    5. NUMA内存分配
                        1. slab
                    6. 页面交换
                4. 分页管理
                    1. 页面与页表
                    2. 地址变换
                5. 分段管理
                    1. 段页式管理
                6. 虚拟内存
                    1. 请页机制
                    2. 页面置换算法
            6. 设备管理
                1. 设备抽象
                2. 中断处理
                3. 设备驱动
                    1. 设备缓冲区
                4. 设备分配
                    1. 设备标识符和命名
                    2. 设备控制表
            7. 文件系统
                1. 文件抽象
                    1. 操作
                        1. 创建删除
                        2. 打开关闭
                        3. 读、写
                        4. 其他操作
                    2. 结构
                        1. 元数据区
                            1. 文件控制块
                                1. 索引节点
                                    1. 多级索引
                        2. 数据区
                    3. 目录结构
                        1. 目录检索
                2. 文件系统
                    1. 文件系统接口
                    2. 对象操纵和管理
                        1. 存储空间管理
                            1. 空闲表
                            2. 位图
                        2. 文件共享
                            1. 链接
                                1. 硬链接
                                2. 软链接
                    3. 对象及属性
                        1. 文件
                        2. 目录
                        3. 设备
            8. 操作系统接口
                1. 系统调用
                    1. 陷入
                    2. 系统调用向量
                    3. POSIX标准
                2. Shell
                3. 图形用户接口
            9. Linux内核编程
                1. 简单模块编写
                2. 内核基本数据结构
                3. 进程模型
                4. 内存管理
                5. 内核同步方法
                6. 中断和下半部
                    1. Linux中断体系结构
                    2. 中断上下文
                    3. 软中断
                    4. tasklet
                    5. 工作队列
                7. 设备模型和sysfs
                8. PCI总线和设备驱动
                9. 块设备和网络设备驱动
                10. 虚拟文件系统
    3. 环境配置运维
        1. 部署
            1. 系统部署
                1. PXE
                2. Cobbler
            2. 软件部署编排
                1. Heat
                2. Docker
        2. 配置
            1. 配置工具
                1. 基于代理
                    1. puppet
                    2. salt
                2. 无代理
                    1. fabric
                3. 轻代理
                    1. ansible
        3. 运维
            1. 监控告警
                1. shinken
                2. ganlia
                3. zabbix
            2. 日志
                1. ELK
                    1. ElasticSearch
                    2. Logstash
                    3. Kibana
                2. Flume Storm kafka
5. 工程管理
    1. 开发过程
        1. 开发阶段
        2. 开发模型
            1. 瀑布模型
            2. V模型
            3. 原型化模型
            4. 分阶段开发模型
                1. 增量式
                    1. 按照需求依次实现子系统
                2. 迭代式
                    1. 先提供整体框架，陆续实现子系统
            5. 螺旋模型
            6. 敏捷方法
    2. 需求管理分析
    3. 项目管理
        1. 时间进度管理
        2. 人力资源和成本管理
        3. 沟通管理
        4. 风险管理
        5. 集成管理
    4. 敏捷开发
        1. 自动化测试
        2. 持续集成
        3. 持续交付