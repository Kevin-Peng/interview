## 2021.03.18 叮咚买菜
1. 分享一个比较经典的优化sql的例子，关心的是具体的case，有数据的支撑；
2. java8的新特性，stream流的使用，简单介绍一下这个功能，类似于filter的中间的操作有哪些，结果的操作有哪些reduce，collect；用stream判断两个list是否包含对方的元素；
   并行的stream用过吗？parallelSteam
3. 反射，可以用在哪些场景下；
4. spring框架用过哪些设计模式，简单说说代理模式，静态代理，动态代理；
5. 设计模式的几大原则，依赖倒转什么意思；
6. beanfactory和applicationncontext区别；
7. GC的root对象；  
   （虚拟机栈中引用的对象  
    本地方法栈中引用的对象  
    方法区中类静态属性引用的对象  
    方法区中常量引用的对象）  
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
6. HashMap是怎么扩容的
7. JVM用的什么垃圾回收器  
   java9开始使用G1，之前老年代使用cms，年轻代是用parallNew，java17开始使用ZGC，特点是使用了染色指针和读屏障技术，空间换时间，大幅缩短大内存（最高16TB）下垃圾回收时间
8. CMS停顿几次
   两次，初始标记和重新标记两个阶段
9. ES用于什么场景
10. git rebase和git merge的区别
11. 链表判断环
12. 二叉树最大路径和
13. java.util包下用到的设计模式
14. es倒排索引 倒排索引的底层数据结构
15. AQS的原理 CAS
16. 怎么解决死锁
17. 线上频繁full GC怎么解决
18. CMS的理解 CMS的缺点
19. spring cloud的组件 为什么选择spring cloud config
20. 集群限流的策略
21. 知道的分布式解决方案
22. HashMap ConcurrentHashMap CountDownLatch CyclicBarrier
23. 创建线程的方式 线程池参数
24. 线上问题排查（CPU100%，OOM）
25. mysql索引（为什么用B+树 最左匹配原则）

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
