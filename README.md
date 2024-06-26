# interview
Java面经记录 这里仅记录最新的，历史的移步各年的md文件中查阅
    
## 2022.06.14 字节跳动 飞书 企业应用 财务
1. 算法题 蛇形打印二叉树 层序遍历变种  103二叉树的锯齿形层序遍历                                                                            
   https://wenku.baidu.com/view/e4043a3dfc00bed5b9f3f90f76c66137ef064f57.html   
2. 联合索引（a,b）生效不生效情况  
   （1、索引字段顺序不合适：联合索引的字段顺序非常重要。如果查询的条件不是按照联合索引的顺序进行查询，那么该索引就会失效。  
    2、索引列使用了函数：如果查询条件中的索引列使用了函数，例如使用了UPPER()函数将查询条件中的字段转为大写，那么该索引就会失效。  
    3、范围查询：如果查询条件中包括了范围查询，例如使用了BETWEEN、>、<等操作符，那么该索引就会失效。  
    4、索引列数据类型不匹配：如果查询条件中的数据类型与索引列的数据类型不匹配，那么该索引就会失效。  
    5、索引列存在NULL值：如果查询条件中包含了索引列的NULL值，那么该索引就会失效。  
    6、数据量太小：如果表中的数据量太小，相比于全表扫描，使用索引进行查询可能没有优势，从而导致索引失效。  
    7、索引统计信息过期：如果索引的统计信息过期，MySQL可能会不正确地选择使用索引进行查询，从而导致索引失效。  
    8、强制使用索引：如果在查询语句中强制使用了索引提示，而该索引并不适合当前查询，那么该索引就会失效。）  
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
    1.内存存储：Redis 将数据存储在内存中，这使得它能够实现非常快的读写操作。相比于磁盘 I/O，内存访问速度更快，因此 Redis 能够快速响应请求。  
    2.单线程模型：Redis 使用单线程模型来处理客户端请求，这意味着它不需要处理多线程之间的竞争和同步问题。虽然单线程模型在多核系统中可能会受到一些限制，但 Redis 通过使用非阻塞 I/O 和事件驱动的方式，有效地利用了系统资 
      源，使得它可以处理大量的并发请求。  
    3.高效的数据结构：Redis 提供了丰富的数据结构，如字符串、哈希表、列表、集合等，这些数据结构在实现上都经过了优化，使得它们能够在内存中高效地存储和操作数据。  
    4.优化的网络通信：Redis 使用了高效的网络通信协议，如 RESP（REdis Serialization Protocol），它是一种文本协议，通过将数据序列化为文本格式来减少网络传输的开销，并且支持 pipelining 和批量操作，从而减少了通信的延迟。  
    5.持久化支持：虽然 Redis 主要是一个内存数据库，但它也支持将数据持久化到磁盘上，以防止数据丢失。Redis 提供了两种持久化方式：RDB（Redis Database）快照和 AOF（Append Only File）日志，这两种方式都经过了优化，能够在 
      保证数据一致性的前提下尽可能地减少对性能的影响。  
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
增加消费者数量：  
启动更多的消费者实例来分摊负载。  
增加分区数：  
增加Topic的分区数，从而允许更多的消费者并行处理消息。  
提高消费者拉取间隔：  
通过调整max.poll.interval.ms配置，增加每次poll()调用之间的最大时间间隔，给消费者更长的处理时间。  
提高消费者并发度：  
如果使用了消费者群组机制，增加消费者的并发度，即增加同一个群组内消费者实例的数量。  
使用exactly-once语义：  
通过配置Kafka消费者为exactly-once，可以使用事务或者增加副本来确保消息只被处理一次。  
监控和调整：  
使用Kafka监控工具，如Kafka Manager或者JMX，实时监控消费者的消费速率和堆积情况，根据实际情况调整消费策略。  
优化消费者逻辑：  
优化消费者处理消息的逻辑，减少处理消息所需的时间，提高消费能力。  
使用死信队列：  
如果消费者处理消息失败，可以将失败的消息移动到死信（Dead Letter）队列以便后续处理。  
消息压缩：  
如果消息大小导致处理缓慢，考虑压缩消息以提高处理速度。  
主动拉取：  
根据业务需求，通过调用poll(long timeout)方法主动控制消息的拉取频率和时间。  
在处理消费堆积时，重要的是要根据实际情况选择合适的策略，并进行适当的调整。通常，需要结合监控和日志分析来确定最佳实践。  

描述一下工作中的性能优化案例，mysql  缓存，分表11张  
分表后，联表查询是如何处理的  
mysql索引b+树的树高由哪些条件决定：数据量，索引字段大小，数据库配置页的大小决定  
InnoDB引擎的行锁依赖什么实现的  通过给索引的索引项加锁来实现的  
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
  lambda表达式、流（Streams） API、日期时间 API（java.time package）、Optional 类  
jdk最新版本是多少  
博客，开源有贡献吗  
看过技术书籍吗  
简单的算法  口述一下，字符串不使用额外的堆空间，反转字符串内容  

## 2023.03.06 拼多多
1. redis过期淘汰策略  
   noeviction: 不进行淘汰，达到内存限制时，会返回错误。  
   allkeys-lru: 当内存不足以容纳更多数据时，使用最近最少使用算法进行淘汰。  
   allkeys-random: 在内存达到限制时随机淘汰键。  
   volatile-lru: 只对设置了过期时间的键进行最近最少使用算法的淘汰。  
   volatile-random: 在对设置了过期时间的键进行随机淘汰。  
   volatile-ttl: 对设置了过期时间的键根据 TTL 进行淘汰，优先淘汰 TTL 较短的键。  
2. redis基本数据结构
3. redis实现延时缓存 zset 对score分值赋予到期时间，到了时间点依次取出缓存对应的值
4. redis使用cluster模式时，一个请求过来的流程是怎么样的
5. 工作中遇到什么难点
6. 算法 完全二叉树一共有多少节点数，leetcode222 递归复杂度O(N)，要优化，使用二分查找，找到非完全二叉树的子树，其它部分按完全二叉树直接计算。

## 2023.03.25 百安居
1. hashmap存储结构，怎么判断一个key是否存在
2. sychronized和retreentlock的区别
3. spring怎么解决三级缓存问题，使用二级缓存可以吗，构造函数依赖可以解决吗
4. java事务失效的情况  
   方法没有被声明为@Transactional注解，或者注解配置错误。  
   事务方法不是public的。  
   事务方法被同一个类中的另一个非事务方法调用，导致事务不生效。  
   数据库本身不支持事务或者未配置正确。  
   事务方法抛出了RuntimeException以外的异常，导致事务回滚无效。  
   事务的传播行为配置不当。  
   事务的隔离级别配置不当。  
   资源管理器（如数据库）不可用或者网络问题导致事务无法提交或回滚。  
5. full GC的过程，可达性分析，标记整理，标记清除
6. 线程池提交的过程，核心参数
7. mybatis默认隔离级别，mybatis如何解决幻读问题
8. ThreadLocal会出现什么问题，内存泄漏
9. mysql的索引用的什么数据结构，有什么好处
10. mysql怎么优化，使用了索引并且命中了也很慢该怎么处理
11. kafka为什么吞吐量大  
    分布式架构：Kafka采用分布式架构，能够将数据分散到多个节点上进行并行处理，显著提高吞吐量。  
    零拷贝技术：通过使用零拷贝技术，Kafka在数据传输过程中避免了数据的多次复制操作，减少了内存和CPU的开销，提高了数据传输效率。  
    批量处理：支持对消息进行批量处理，允许生产者将多个消息打包成一个批次后一次性发送到服务器端，减少了网络传输的开销，并提高了吞吐量。  
    高效的文件系统：Kafka使用高效的文件系统来存储和管理数据，如Linux文件系统，提供高速的读写能力，从而提高了吞吐量。  
    顺序写磁盘：Kafka在写入数据时，消息是不断追加到文件中的，这种方式充分利用了磁盘的顺序读写性能，减少了随机写入的开销，提高了磁盘的利用率和读写性能。  
    压缩技术：支持对消息进行压缩，可以减少网络传输的数据量，提高吞吐量。  
    副本机制：通过副本机制来保证数据的可靠性和容错性，同时提高数据的可用性，也能在一定程度上提高吞吐量。  
    页缓存技术：Kafka基于操作系统的页缓存来实现写入，这样可以提升写性能，因为数据先写入到操作系统的缓存中，再由操作系统决定何时将数据刷入磁盘。  
    高效的磁盘存储：Kafka使用高效的存储格式来存储消息数据，优化了存储空间的使用，并保证了快速的数据访问速度。  
    水平扩展：Kafka集群可以通过增加更多的服务器来轻松扩展，通过增加Broker节点来增加系统的整体吞吐量。  
12. redis怎么解决数据一致性问题，延时双删，还有其他方法吗，延时双删第二次删除缓存失败怎么办  
13. 服务间调用用的什么，dubbo了解过吗
14. 注册中心用的什么，其他的了解过吗

## 2023.03.31 百安居二面
1. 黑名单文件 2G手机号，怎么判断某个手机号在里面
2. 用户画像数据结构设计
3. 大数据量表分表
4. 查询数据分页
5. Java synchronized关键词 修饰一段代码时，如何优化
6. final关键词，修饰类的作用是什么  
   防止继承。当一个类被声明为final时，它不能被其他类继承。这意味着一旦将一个类定义为final，就不能创建该类的子类。  
   限制修改。使用final修饰的类、方法和变量都是不可修改的，这有助于保持代码的稳定性和一致性。  
7. 英文词典30万数据，里面兄弟单词（单词的字母组合完全一致，例如stop-pots-tops）怎么查询出来所有的兄弟单词

## 2023.09.13 蚂蚁金服 商业化广告
1. redis缓存，怎么使用redis做分布式锁，原理是什么，作为锁的key怎么设计  
   Redis 2.6.12以上版本中使用SET key value EX max-lock-time NX命令
2. redis使用分布式集群，怎么保证一致性  
  （选举主节点：集群中的主节点通过内部投票协议进行选举，保证任何时刻只有一个主节点。  
   日志复制：当客户端向主节点发送写操作时，主节点将其作为日志条目并通过gossip协议和异步复制机制发送给其他从节点。一旦大多数从节点确认接收日志条目，主节点会确认提交该写操作。  
   安全性：如果主节点失效，其他从节点会通过新的主节点选举过程来接管。在这个过程中，集群会保证数据的一致性和安全性。  
   为了保证数据的一致性，Redis Cluster还提供了如下的配置和命令：  
   min-replicas-to-write：指定写入操作在确认主节点成功之前至少需要同步到的副本数量。  
   min-replicas-max-lag：指定允许副本落后于主节点的最大时间。  
   以上配置可以在redis.conf文件中设置，并通过CLUSTER SET-CONFIG命令进行运行时的更改。  
   在实际操作中，通常不需要手动干预，因为Redis Cluster可以自动处理这些问题。但是，了解上述机制可以帮助你更好地维护和监控你的Redis集群。）  
4. mysql的查询优化  
   优化查询语句：避免全表扫描，使用索引。  
   优化数据表结构：合理设计表结构，选择合适的数据类型和索引。  
   优化服务器配置：调整缓冲区大小，增加内存等。  
   使用EXPLAIN语句分析查询：了解MySQL如何处理查询。  
   定期优化和修复表：使用OPTIMIZE TABLE和CHECK TABLE。  
5. kafka的推拉模式  
   （Push 模式是 Kafka 最初实现的默认方式。在这种模式下，生产者将消息直接推送到 Kafka 集群中的分区中，分区会自动将消息存储在磁盘上，并异步地将消息传输到消费者。使用 push 模式时，生产者主动控制消息的推送速度，而消费者则以自己的速度从 Kafka 集群中拉取可用的消息。
    优点
    实时性较高：push 模式下，消息可以即时被推送到 Kafka 集群中，而消费者也可以即时拉取消息，适用于要求实时性较高的场景。
    生产者控制消息速率：使用 push 模式时，生产者可以控制消息的推送速率，避免因过快的消息推送导致集群负载过高。
    基于时间戳的消息排序：push 模式下，Kafka 会根据消息的时间戳对消息进行排序，由此可以确保消费者按正确的顺序消费消息。
    缺点
    消费者的不确定性：在 push 模式下，消费者需要等待生产者推送消息，如果生产者没有推送新消息，消费者就不能获取新的数据，这会导致消息实时性较低。
    资源浪费：使用 push 模式时，可能会发送大量重复或无效的消息，导致资源的浪费。
    
    Pull 模式是 Kafka 新增的方式，使用该模式时，消费者可以自主选择从哪个分区开始拉取消息，并可以自主控制拉取消息的速度。Kafka 中为消费者维护着一个 offset，表示消费者已经消费的消息序号，当消费者拉取消息时，Kafka 会返回该消费者还没有消费的消息。
    优点
    消费者灵活性高：使用 pull 模式时，消费者可以自主决定拉取消息的速率和开始消费的位置。
    减少消息浪费：使用 pull 模式时，可以避免发送大量无效或重复的消息，减少资源的浪费。
    缺点
    实时性较低：使用 pull 模式时，消费者可能需要等待一定的时间才能获取到新的消息，这会导致消息实时性较低。
    需要消费者主动拉取：在 pull 模式下，消费者需要自己控制拉取消息的速率和时机，这会增加一定的操作复杂度。）
6. 做过的广告系统，数据转化，曝光点击数据链路上报以及采集的流程，今天广告有多少曝光，点击从何而来。  
   （分众属于线下广告，一般以品牌广告为主，销售广告为辅，点击率转换率其实没有直接的数值，但是通常我们可以给客户提供百度指数以及电商平台店铺搜索及访问量的一个后续的参考，以便展示我们广告带来的曝光效果）
7. JVM调优  
   （堆内存调优：调整堆内存的大小，包括初始堆大小（-Xms参数）和最大堆大小（-Xmx参数），以适应应用程序的内存需求。这有助于避免内存溢出和提高垃圾回收的效率。  
     垃圾回收器选择和调优：选择合适的垃圾回收器，如G1垃圾回收器，并调整其参数，以减少垃圾回收的停顿时间和提高吞吐量。例如，使用-XX:+UseG1GC参数启用G1垃圾回收器。  
     线程堆栈大小调优：合理设置线程堆栈大小（-Xss参数），以提高线程创建和管理的效率，并避免频繁的线程栈溢出。  
     类加载调优：优化类加载器的配置，包括设置适当的类加载器层次结构和减少类加载的次数，以提高加载速度和减少内存消耗。  
     JIT编译器调优：调整即时编译器（JIT）的相关参数，如编译级别和内联策略，以获得更好的性能。  
     I/O调优：对输入输出操作进行优化，包括使用合适的缓冲区大小、选择高效的I/O操作方式（如NIO），以及优化文件和网络操作等。  
     监控和分析：使用工具如jps、jstat、jinfo、jstack等命令行工具监控JVM的运行情况，如内存使用情况、垃圾回收情况、线程状态等，并进行性能分析，以找出性能瓶颈和优化的潜在点。  
     生成GC日志和dump文件：通过配置JVM参数生成GC日志和堆转储文件，这些文件可以帮助分析内存使用情况和性能瓶颈。） 
8. 垃圾回收算法，G1和CMS的区别  
   （设计目标不同。CMS主要关注减少老年代的垃圾收集停顿时间，而G1旨在减少整体垃圾收集的停顿时间，包括新生代和老年代。  
    垃圾回收算法不同。CMS采用标记清除算法，这可能导致大量的内存碎片；G1使用标记整理算法，能够减少内存碎片的产生。  
    解决漏标的方式不同。CMS通过增量更新来解决漏标问题；G1采用原始快照的方式。  
    内存碎片不同。CMS可能导致内存碎片；G1不会产生内存碎片。  
    STW（停止世界）时长不同。CMS无法预测STW时长；G1可以预测STW时长。  
    堆内存适用大小不同。CMS一般建议使用4至8GB的堆内存；G1建议使用8GB以上的堆内存。  
    收集器的默认配置不同。在JDK9发布之前，CMS被视为默认的垃圾收集器；从JDK9开始，G1成为服务端模式下的默认收集器。  
    性能影响不同。G1使用更多的内存和CPU负载，适合用于大堆的应用；CMS相对资源消耗较少，但可能在某些场景中被G1取代。  
    此外，G1引入了分区概念，会将内存分成2048个region，可以动态调整新生代和老年代的占比，而CMS则没有这些特性。）  
9. 算法题 459重复的子字符串

## 2024.05.09 蚂蚁金服 内容技术 
1. 自我介绍  
2. 笔试，反转链表 双指针 递归双方法 时间复杂度O(n)，注意双指针空间复杂度O(1)，递归空间复杂度O(n)， 除此以外头插法会更好理解一点。  
    ```java
    class Solution {  
        public ListNode reverseList(ListNode head) {  
            return recur(head, null);    // 调用递归并返回  
        }  
        private ListNode recur(ListNode cur, ListNode pre) {  
            if (cur == null) return pre; // 终止条件  
                ListNode res = recur(cur.next, cur);  // 递归后继节点  
                cur.next = pre;              // 修改节点引用指向  
                return res;                  // 返回反转链表的头节点  
        }  
    }
    ``` 
3. 项目介绍，使用了kafka，qps，数据量大小，kafka完整性检查  
4. 项目里使用了redis，redis怎么使用来提升用户的访问效率， redis集群几种模式
5. 线程池 参数 什么时候会进入等待队列
6. 有三个线程t1，t2，t3，怎么确保顺序执行，java里现有的工具可以实现的知道吗  
   在子线程中通过join()方法指定顺序  
   在主线程中通过join()方法指定顺序  
   通过倒数计时器CountDownLatch实现  
   通过创建单一化线程池newSingleThreadExecutor()实现  
   https://www.jb51.net/article/246666.htm
7. 项目讲解思路是背景-目的-架构和技术-难点和解决-如何评估项目优势。这样展开个人感觉非常值得借鉴   

