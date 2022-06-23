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
hashmap的数据结构
hashmap你怎么实现线程安全，参考ConcurrentHashMap

synchronized  ReentrantLock
CAS  AQS
线程池的参数

jvm的内存结构
频繁full GC排查
为什么分代收集
什么时候会触发young GC
对象什么时候到老年代
用到的垃圾回收器

怎么优化慢sql
什么情况索引失效
事务隔离级别  怎么解决幻读

怎么保证消息的可靠性
消息的顺序消费


## 2021.4.23 字节跳动 同事面经
算法题 合并区间  排序+双指针 https://leetcode-cn.com/problems/merge-intervals/


## 2022.6.14 字节跳动 飞书 企业应用 财务
算法题 蛇形打印二叉树 层序遍历变种  https://wenku.baidu.com/view/e4043a3dfc00bed5b9f3f90f76c66137ef064f57.html
联合索引（a,b）生效不生效情况
索引底层数据结构 B+树
java bean是多例还是单例？单例，可以多例吗？可以，什么场景多例？并发修改bean状态
应用A，B分别更新数据库，如何防止脏数据  redis分布式锁 redlock 
限流操作 令牌桶 漏桶 滑动窗口
目前负责的项目亮点 


## 2022.6.23 擎朗科技 同事面经
JVM JMM volatile memory barrier
GC 方法区/元空间GC是否清理
反射 代理  泛型 泛型擦除 Bean
ThreadPool 参数 wait/sleep 线程状态
synchronized reentrantlock AQS
mysql 索引 隔离级别 RR可重复读 MVCC 幻读 间隙锁Gap Lock
sleep wait
kafka
