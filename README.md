# interview
Java面经记录 这里仅记录最新的，历史的移步各年的md文件中查阅

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
    最终一致性场景：组合使用Cache-Aside + 延迟双删 + 异步重试，适合大多数业务。   
    高实时性要求：结合Binlog订阅 + 快速过期缩短不一致窗口。  
    极端一致性需求：权衡性能后采用强一致性方案，但需谨慎评估。  
14. 服务间调用用的什么，dubbo了解过吗
15. 注册中心用的什么，其他的了解过吗
    ‌Zookeeper‌：Zookeeper是一个开源的分布式协调服务，它提供了诸如统一命名服务、配置管理和分布式锁等功能的实现。Zookeeper通过维护一个层次化的文件系统来存储数据，并支持大量的并发连接和访问。
    ‌Eureka‌：Eureka是Netflix开发的服务发现框架，主要用于AWS云和本地数据中心。Eureka具有自我修复的能力，当服务节点发生故障时，Eureka会自动移除失效的服务节点。
    ‌Nacos‌：Nacos是一个更动态、更易于使用的服务发现和配置管理平台。它支持多种类型的数据一致性协议，并且提供了更丰富的功能，如服务治理、动态配置管理等。
    ‌Consul‌：Consul由HashiCorp提供，支持多数据中心，具有内置的健康检查、服务发现和键值存储等功能。Consul使用Go语言开发，易于集成和使用。
    ‌Etcd‌：Etcd是一个高可用的键值存储系统，主要用于共享配置和管理小型数据。它提供了强一致性模型，适用于需要高可靠性的场景。

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

