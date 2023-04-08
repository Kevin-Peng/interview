# interview
Java面经记录
    
## 2022.06.14 字节跳动 飞书 企业应用 财务
1. 算法题 蛇形打印二叉树 层序遍历变种  https://wenku.baidu.com/view/e4043a3dfc00bed5b9f3f90f76c66137ef064f57.html
2. 联合索引（a,b）生效不生效情况
3. 索引底层数据结构 B+树
4. java bean是多例还是单例？单例，可以多例吗？可以，什么场景多例？并发修改bean状态
5. 应用A，B分别更新数据库，如何防止脏数据  redis分布式锁 redlock 
6. 限流操作 令牌桶 漏桶 滑动窗口
7. 目前负责的项目亮点 广告发布投放解耦  xxl-job 多账号虚拟金
    
## 2022.06.23 擎朗智能 同事面经
1. JVM JMM volatile memory barrier
2. GC 方法区/元空间GC是否清理
3. 反射 代理  泛型 泛型擦除 Bean
4. ThreadPool 参数 wait/sleep 线程状态
5. synchronized reentrantlock AQS
6. mysql 索引 隔离级别 RR可重复读 MVCC 幻读 间隙锁Gap Lock
7. 常用的集合  arraylist与linkedlist区别

## 2022.06.27 顺丰 同事
1. AQS
2. MVCC 
3. 分布式锁
4. nacos与apollo的区别
5. B树与B+树
6. 线程池 线程池参数 线程状态（6种） wait和blocked的区别
7. 工作上解决的问题

## 2022.06.28 擎创 同事
1. Kafka rabbitMQ 顺序读写 零拷贝 批量拉取
2. redis RDB AOF
3. 分布式锁
4. 缓存击穿 缓存穿透 缓存雪崩
5. redis内存淘汰策略
6. mysql 索引
7. 事务
8. 数据库隔离级别 MVCC（多版本并发控制） LBCC（基于锁的并发控制）
9. kafka 使用场景
10. 幂等
11. ES

## 2022.06.29 泛微 同事
1. jre jdk
2. equals和==的区别
3. String 的hashcode和equals方法
4. redis使用场景 缓存穿透 缓存击穿
5. threadLocal
6. 双亲委派
7. 热部署
8. 分表场景 如何拓展
9. full GC场景 oom排查 死锁如何查
10. 软引用
11. nacos
12. kafka和rabbitMQ的区别，kafka的使用场景
13. kafka延迟现象 实时性比较强要如何处理

## 2022.06.29 飞书深诺 同事
1. JMM
2. 跳跃表 skipList
3. hashmap concurrenthashmap
4. 如何写一个优秀的代码
5. 悲观锁 乐观锁
6. 如果让你设计架构你会考虑哪些

## 2022.07.05 珍岛 同事
1. nacos和Apollo的区别  k8s和docker的区别
2. Spring事务实现流程
3. 数据库 乐观锁 分布式锁使用场景
4. ReentrantLock Sychronized JDK11 优化
5. hashmap和hashset的区别
6. 克隆方法
7. 下单30分钟发送短信
8. 一个表 id  科目 分数  查询每个科目最高分的id  sql语句
9. sql判断有没有走索引 索引失效的情况
10. binlog使用场景
11. redis为什么那么快 redis key失效
12. 慢接口优化
13. 换工作原因 加班的看法

## 2022.07.06 万位数字 同事
1. spring 事务传播机制及其实现原理
2. feign实现原理
3. 分布式锁实现原理
4. 死锁分析
5. mysql死锁怎么排查  怎么产生的
6. springboot与spring区别
7. springboot @enable相关注解实现机制
8. 怎么分表的
9. ck为啥这么块 适合前端页面查询场景么
10. jdk7 8 11区别  conncurrenthashmap实现原理

## 2022.07.07 前晨汽车 同事
1. spring启动流程，spring重要的注解 spring aop ,动态代理 为啥接口用jdk代理 抽象类行吗
2. 设计电商系统  秒杀系统 
3. 内存溢出 内存泄露的排查解决
4. threadlocal remove
5. mysql 死锁，limit 10000 怎么优化， hashmap
6. 算法题  x y 坐标轴 上面有很多点 求最长的直线
7. 一个int类的请求，怎么对他进行 < 10的校验
8. 注解使用, 使用场景
9. spring线程池流程  怎么保证顺序执行、两个线程i++500次 怎么保证变成1000

## 2022.07.18 艺星 同事
简单自我介绍～  

意思：重点介绍自己的负责领域  技术领域
架构，项目方面
项目的介绍  挑点  询价（优惠券，虚拟金，系统折扣）  下单支付

项目中用了哪些技术：
kafka用来解决什么问题
kafka速度快的原因（分区，磁盘顺序写，压缩，零拷贝，）
kafka实际运用过么，优化这方面
中间件的源码看过吗
算法题做过吗
net转到Java方向，介绍net做过哪些（net打印方面做过吗）
数据库MySQL  SqlServer，切换到MySQL，数据量大的情况下分页优化：
索引  b+树淘汰的过程

问对方
对方后端  团队情况  人员配置
3个Java  一共10个人

## 2022.07.19 维音 同事
说一说离职原因
上班距离有要求吗
加班问题怎么看待

技术：
jdk hashmap内部结构大体说一下
红黑树会比较快的原因
get方法的实现 key的hashcode异或  后面的查找是如何进行的
Java8流跟lambda表达式用过吗
reduce   累积bigdecimal  
创建一个流用什么方式

Arrays.aslist()
流里面map方法的参数类型，匿名内部类是继承哪个接口
lambda函数式接口，用哪些方法
jdk内置的方法有哪些属于lambda函数式接口
http协议  常见请求头  标准请求头，说一说

contenttype
上传一个文件，会带哪些请求头
认证相关的请求头
跨域相关的
缓存相关
响应的状态码   301跳转
未授权401  400 badrequest
标准的响应头能不能说一遍

valid  requestbody请求参数数据实体   有什么用处吗，不写会影响传参格式吗
springboot如何处理http请求的，流程大概梳理一下
mybatis预防SQL注入，参数化填充，自己有意做的功能还是别的工具来实现的
mybatis一二级缓存，mybatis拦截器（handler类型转换处理），intercept
mapper  xml自定义标签 平时自己做过吗
springboot自动装配 说一说 提示了import
自动装配过程中有一些condition注解，有没有看过源码，常见的内置的几个条件 说几个

一面过的话  二面会有少量的技术面
crm模块开发

团队成员配置大概多少  10人以下

## 2022.09.07 基煜基金 同事
1. 自我介绍
2. 生物医学专业为啥弄java
3. 为啥要离职
4. 项目主要的职责
5. 有没有带队经验
6. 职业规划
7. 怎么看待加班
8. 文档 时序图 类图
9. hashmap 结构
10. jvm优化经验
11. springboot 自动装配
12. 分布式事务
13. 事务失效场景
14. 有没有做过性能监控
15. 两个服务两个表怎么连表查询
16. mysql 优化
17. 了不了解基金
18. 期望薪资

## 2022.09.09 穗禾 同事
微服务架构  springcloud组建除了openfeign 还用了其他的组件吗  
网关  业务网关  没有  
流量入口，微服务入口数据请求聚合，耦合性太高，定制化接口  
openfeign abc三个服务，针对这3个服务做不同的配置，使用自定义注解，bean  MessageConverter转换  
openfeign重试机制有没有，如果需要重试，应该要怎么做  
服务之间的熔断，重新发起的策略  
分布式锁，用在什么场景下  
如果做分布式锁，要考虑哪些方面，重入情况，考虑安全性  
释放锁 怎么释放，key的构成  
Redis锁续期设置是多少  
Redis锁有没有什么潜在问题，  
springboot的扩展开发有哪些  
springboot读取配置的方式有哪些，jvm环境变量  
jvm启动时，怎样自定义参数进行变量配置  
springboot加载配置文件的目录，顺序不一样，原理  
springioc 创建对象方式，比如说注解扫描等，springfactories  
springboot  starter 自动化配置大概流程  
conditionOnxxxx用过哪些  
springboot基于spring进行启动的，启动过程（spring ioc）是在哪个节点上进行加载springboot的web环境  
了解spring  ioc的启动流程  
springboot  factories文件中可以配置过哪些东西  
本地事物怎么做，transaction配置过哪些字段  
事物传播，前一个事物挂起，后一个事物执行完后，  
springcloud组件用过哪些  
nacos节点之间，数据怎么同步的  
性能优化，哪方面的，分发数据分表，其他时间段  
分发表的3天热点数据有没有更好的优化策略  
数据库MySQL隔离级别，幻读在哪个隔离级别下，可重复读怎么解决幻读的，间隙锁  
MySQL锁了解吗，表锁，行锁，insert会加哪些锁  
MySQL走了索引，还能继续优化吗，知晓每一个步骤怎么  
死锁，怎么查看不用事物导致的死锁  
多线程，解决原子性，  
synchronized锁机制，获取锁里面用的数据结构，等待队列，索引等等  
读写锁  
jvm定位死锁，怎么查  
jvm优化配置做过吗  
业务方面  工作流，业务引擎用过吗  
问对方的问题  
问了薪资多少，是否在职  

## 2022.09.23 未知 同事
具体描述一下零售分众直投项目业务  
数据量大概有多少  
项目架构大概描述一下  
k8s部署流程是怎样的  
订单挑点、分发大概是什么样的，描述了选点过程  
简单介绍一下订单模块的表结构设计  
利用了springcloud具体哪些组件，网关用了吗  
http请求对应的服务是怎么请求的  
负载均衡有几种策略  
Redis分布式锁用在哪些场景里，有哪几个需要注意的点  
缓存过期时间多久，有长有短  
kafka消息队列用在哪些场景  
kafka消息遇到堆积情况，如何处理  
描述一下工作中的性能优化案例，mysql  缓存，分表11张  
分表后，联表查询是如何处理的  
mysql索引b+树的树高由哪些条件决定：数据量，索引字段大小，数据库配置页的大小决定  
InnoDB引擎的行锁依赖什么实现的  
Java基础相关  
顶级类object有哪些方法hashcode  equals等  
hashmap使用注意哪些点，现程不安全，key可以为null，使用自定义对象，需要重写equals，不能在便利中修改，还有个啥来着  
多线程的使用  
线程池有哪几个参数  
sychro跟reentranlock区别，reentranlock可以唤醒，可以设置超时时刻，锁的力度更细  
volitile的解决线程的重排序  
Java启动，jvm后面会配置哪些参数，一般会配置gclog  打印gc情况，堆内存  
Java  collection下面的容器有哪些  
说说springboot自动装配  
用了设计模式，去除ifelse，模板模式，策略模式，展现模式  
谓语句是什么： 进入if后直接return  
讲一下代码review，平时关注的点  
线上如何监控，排查问题的  
服务出现问题，一般如何解决，有案例吗  
Java在开发过程中相应的缺点是什么：把基本类型作为对象处理，其中包装类作为妥协  
Linux命令，授权命令，端口占用  
jdk1.8更新了哪些新特性  
jdk最新版本是多少  
博客，开源有贡献吗  
看过技术书籍吗  
简单的算法  口述一下，字符串不使用额外的堆空间，反转字符串内容  

## 2023.03.06 拼多多
1. redis过期淘汰策略
2. redis基本数据结构
3. redis实现延时缓存 zset
4. redis使用cluster模式时，一个请求过来的流程是怎么样的
5. 工作中遇到什么难点
6. 算法 完全二叉树一共有多少节点数，递归复杂度O(N)，要优化

## 2023.03.25 百安居
1. hashmap存储结构，怎么判断一个key是否存在
2. sychronized和retreentlock的区别
3. spring怎么解决三级缓存问题，使用二级缓存可以吗，构造函数依赖可以解决吗
4. java事务失效的情况
5. full GC的过程，可达性分析，标记整理，标记清除
6. 线程池提交的过程，核心参数
7. mybatis默认隔离级别，mybatis如何解决幻读问题
8. ThreadLocal会出现什么问题，内存泄漏
9. mysql的索引用的什么数据结构，有什么好处
10. mysql怎么优化，使用了索引并且命中了也很慢该怎么处理
11. kafka为什么吞吐量大
12. redis怎么解决数据一致性问题，延时双删，还有其他方法吗，延时双删第二次删除缓存失败怎么办
13. 服务间调用用的什么，dubbo了解过吗
14. 注册中心用的什么，其他的了解过吗


