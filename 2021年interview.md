## 2021.03.18 叮咚买菜
1. 分享一个比较经典的优化sql的例子，关心的是具体的case，有数据的支撑；
2. java8的新特性，stream流的使用，简单介绍一下这个功能，类似于filter的中间的操作有哪些，结果的操作有哪些reduce，collect；用stream判断两个list是否包含对方的元素；
   并行的stream用过吗？parallelSteam
3. 反射，可以用在哪些场景下；
4. spring框架用过哪些设计模式，简单说说代理模式，静态代理，动态代理；
5. 设计模式的几大原则，依赖倒转什么意思；
6. beanfactory和applicationncontext区别；
7. GC的root对象；  
   虚拟机栈中引用的对象  
   本地方法栈中引用的对象  
   方法区中类静态属性引用的对象  
   方法区中常量引用的对象 
8. aop切面里面什么叫通知；
9. aop的实现有哪几种方式，动态代理实现方式是针对哪一种方式的aop，过程是怎么实现的；
10. 数据库隔离级别；
11. 读已提交会产生什么问题，什么是幻读；
12. mysql的执行计划explain，type字段有哪些值，优化的真实的例子；
13. 一张表里有温度和时间，怎么用一个sql查出温度比前一天高的数据；
14. 快排知道怎么排的吗；
15. 具体的技术规划，工作中遇到什么问题；
    
## 2021.04.16 字节跳动 飞书 小程序面板
算法题 判断字符串是否可以由字典中的字符串组成 动态规划  Leetcode 139  
https://blog.csdn.net/summer2day/article/details/97430955

## 2021.04.14 阿里巴巴本地生活 同事
1. rabbitmq怎么实现顺序消费，事务
2. java基础数据类型 float是怎么存储的  
   八种（byte,short,int,long,float,double,char,boolean）
   float通常4个字节，由底数m和指数e组成，
   底数m部分：占用24bit(3个字节)的二进制数来表示此浮点数的实际值，最高位始终为1，不用来储存。
   指数e部分：占用8bit(1个字节)的二进制数，可表示数值范围为0-255。此处算出的次方必须减去127才是真正的指数。  
   所以，float类型的指数可从-126到128。
4. 线程池的参数 线程池的流程 使用线程池时考虑什么  
   corePoolSize：线程池中的常驻核心线程数。  
   maximumPoolSize：线程池允许的最大线程数。  
   keepAliveTime：非核心线程没有任务时的存活时间。  
   unit：keepAliveTime的时间单位。  
   workQueue：用来保存等待执行任务的队列。  
   threadFactory：创建线程的工厂。  
   handler：拒绝策略。  
5. Set有几种实现  
   HashSet。基于哈希表实现，提供快速的插入、删除和查找操作，但元素顺序不确定。  
   LinkedHashSet。是HashSet的升级版，不仅保证元素不重复，还按插入顺序维护元素，内部使用双向链表来保持插入顺序。  
   TreeSet。基于红黑树实现，可以保证元素有序，其插入、删除、查询等操作的时间复杂度为O(logn)，但要求元素实现Comparable接口或提供Comparator进行排序。  
   EnumSet。专门为枚举类型设计的Set集合，使用位向量存储，高效地支持枚举类型的插入、删除和查询操作。  
   CopyOnWriteArraySet。一个线程安全的Set集合，基于Copy-On-Write技术实现，适用于读多写少的场景，但在修改时需要复制数组，可能会影响性能。  
6. HashMap是怎么扩容的
   HashMap默认初始容量为16，负载因子为0.75。当元素数量超过当前容量与负载因子的乘积（即size > capacity * loadFactor）时触发扩容‌12。  
   例如，默认情况下当元素数量达到12（16×0.75）时开始扩容。
   当链表长度超过8且数组容量≥64时，链表会转为红黑树，但若扩容后链表长度减少到6以下，红黑树会退化为链表‌4。    
8. JVM用的什么垃圾回收器  
   java9开始使用G1，之前老年代使用cms，年轻代是用parallNew，java17开始使用ZGC，特点是使用了染色指针和读屏障技术*，空间换时间，大幅缩短大内存（最高16TB）下垃圾回收时间   
      *染色指针是ZGC的核心技术，通过‌在指针地址中直接存储元数据‌（如对象状态标记），无需额外内存空间即可实现并发标记、移动和内存管理优化‌。  
‌      技术原理‌：在64位指针的高4位（42-45位）存储标记信息（如三色标记、对象是否被移动等），剩余46位用于实际寻址‌。  
   ‌   核心优势‌：减少内存访问开销，支持并发操作（如标记和对象移动），避免传统GC中对象头依赖的锁竞争‌  
      读屏障是ZGC实现‌并发对象访问一致性‌的机制，在‌应用线程读取对象引用时触发‌，确保访问的对象地址正确（即使对象已被移动）‌。  
‌      技术原理‌  
‌      触发时机‌：当应用线程加载对象引用时，检查指针颜色状态‌。  
‌      处理逻辑‌：若发现对象已被移动（如指针颜色为Remapped），则通过染色指针的多视图映射机制，自动重定向到新地址‌。  
‌      性能优化‌：仅需少量指令，避免传统GC中全堆遍历的停顿问题‌  
10. CMS停顿几次
   两次，初始标记和重新标记两个阶段
11. ES用于什么场景
12. git rebase和git merge的区别
13. 链表判断环
14. 二叉树最大路径和 leetcode124 困难  
15. java.util包下用到的设计模式  
    迭代器模式（Iterator Pattern）：在java.util包中，Iterator接口用于遍历元素集合。这是一个迭代器模式的例子，该模式允许顺序访问一个聚合对象的各个元素，而又不需要暴露该对象的内部表示。  
    观察者模式（Observer Pattern）：java.util.Observer接口用于观察对象状态的变化。当对象状态改变时，所有依赖它的对象都会得到通知并自动更新。这是观察者模式的一个例子，该模式定义了对象之间的一对多依赖关系，当一个对象改 
    变状态时，所有依赖于它的对象都会得到通知并自动更新。  
    工厂方法模式（Factory Method Pattern）：在java.util包中，例如Calendar类的getInstance方法，SecureRandom类的getInstance方法，以及NumberFormat类的getInstance方法都使用了工厂方法模式。该模式定义了一个用于创建对象的 
    接口，让子类决定实例化哪一个类。工厂方法使一个类的实例化延迟到其子类。  
16. es倒排索引 倒排索引的底层数据结构
17. AQS的原理 CAS
18. 怎么解决死锁  
    互斥，请求与保持，不剥夺条件，循环等待  
19. 线上频繁full GC怎么解决
20. CMS的理解 CMS的缺点
21. spring cloud的组件 为什么选择spring cloud config
22. 集群限流的策略
23. 知道的分布式解决方案
24. HashMap ConcurrentHashMap CountDownLatch CyclicBarrier
25. 创建线程的方式 线程池参数
26. 线上问题排查（CPU100%，OOM）  
   top指令查看线程占用cpu详情，jstack指令获取线程信息，jmap获取堆内存信息。  
27. mysql索引（为什么用B+树 最左匹配原则）

## 2021.04.22 阿里巴巴本地生活 一面 同事面经
1. hashmap的数据结构
2. hashmap你怎么实现线程安全，参考ConcurrentHashMap
3. synchronized  ReentrantLock
4. CAS  AQS
5. 线程池的参数
6. jvm的内存结构
7. 频繁full GC排查
8. 为什么分代收集
9. 什么时候会触发young GC
10. 对象什么时候到老年代
11. 用到的垃圾回收器
12. 怎么优化慢sql
13. 什么情况索引失效
14. 事务隔离级别  怎么解决幻读
15. 怎么保证消息的可靠性
16. 消息的顺序消费
    
## 2021.04.23 字节跳动 同事面经
1. 算法题 合并区间  排序+双指针 https://leetcode-cn.com/problems/merge-intervals/
   ```java
   class Solution {
      public int[][] merge(int[][] intervals) {
         Arrays.sort(intervals, (intervals1, intervals2) -> (intervals1[0] - intervals2[0]));
         List<int[]> merged = new ArrayList<int[]>();
         for (int i = 0; i < intervals.length; ++i) {
            int L = intervals[i][0], R = intervals[i][1];
            if (merged.size() == 0 || merged.get(merged.size() - 1)[1] < L) {
                merged.add(new int[] { L, R });
            } else {
                merged.get(merged.size() - 1)[1] = Math.max(merged.get(merged.size() - 1)[1], R);
            }
        }
        return merged.toArray(new int[merged.size()][]);
      }
   }
   ```
