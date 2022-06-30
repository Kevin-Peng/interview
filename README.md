# interview
Java面经记录
    
## 2021.3.18 叮咚买菜
1. 分享一个比较经典的优化sql的例子，关心的是具体的case，有数据的支撑；
2. java8的新特性，stream流的使用，简单介绍一下这个功能，类似于filter的中间的操作有哪些，结果的操作有哪些reduce，collect；用stream判断两个list是否包含对方的元素；
   并行的stream用过吗？parallelSteam
3. 反射，可以用在哪些场景下；
4. spring框架用过哪些设计模式，简单说说代理模式，静态代理，动态代理；
5. 设计模式的几大原则，依赖倒转什么意思；
6. beanfactory和applicationncontext区别；
7. GC的root对象；
8. aop切面里面什么叫通知；
9. aop的实现有哪几种方式，动态代理实现方式是针对哪一种方式的aop，过程是怎么实现的；
10. 数据库隔离级别；
11. 读已提交会产生什么问题，什么是幻读；
12. mysql的执行计划explain，type字段有哪些值，优化的真实的例子；
13. 一张表里有温度和时间，怎么用一个sql查出温度比前一天高的数据；
14. 快排知道怎么排的吗；
15. 具体的技术规划，工作中遇到什么问题；
    
## 2021.4.16 字节跳动 飞书 小程序面板
算法题 判断字符串是否可以由字典中的字符串组成 动态规划 https://blog.csdn.net/summer2day/article/details/97430955
    
## 2021.4.22 阿里巴巴本地生活 一面 同事面经
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
    
## 2021.4.23 字节跳动 同事面经
1. 算法题 合并区间  排序+双指针 https://leetcode-cn.com/problems/merge-intervals/
    
## 2022.6.14 字节跳动 飞书 企业应用 财务
1. 算法题 蛇形打印二叉树 层序遍历变种  https://wenku.baidu.com/view/e4043a3dfc00bed5b9f3f90f76c66137ef064f57.html
2. 联合索引（a,b）生效不生效情况
3. 索引底层数据结构 B+树
4. java bean是多例还是单例？单例，可以多例吗？可以，什么场景多例？并发修改bean状态
5. 应用A，B分别更新数据库，如何防止脏数据  redis分布式锁 redlock 
6. 限流操作 令牌桶 漏桶 滑动窗口
7. 目前负责的项目亮点 广告发布投放解耦  xxl-job 多账号虚拟金
    
## 2022.6.23 擎朗智能 同事面经
1. JVM JMM volatile memory barrier
2. GC 方法区/元空间GC是否清理
3. 反射 代理  泛型 泛型擦除 Bean
4. ThreadPool 参数 wait/sleep 线程状态
5. synchronized reentrantlock AQS
6. mysql 索引 隔离级别 RR可重复读 MVCC 幻读 间隙锁Gap Lock
7. 常用的集合  arraylist与linkedlist区别

## 2022.6.27 顺丰 同事
1. AQS
2. MVCC 
3. 分布式锁
4. nacos与apollo的区别
5. B树与B+树
6. 线程池 线程池参数 线程状态（6种） wait和blocked的区别
7. 工作上解决的问题

## 2022.6.28 擎创 同事
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

## 2022.6.29 泛微 同事
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

## 2022.6.29 飞书深诺 同事
1. JMM
2. 跳跃表 skipList
3. hashmap concurrenthashmap
4. 如何写一个优秀的代码
5. 悲观锁 乐观锁
6. 如果让你设计架构你会考虑哪些
