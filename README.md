# interview
Java面经记录
    
## 2021.03.18 叮咚买菜
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
    
## 2021.04.16 字节跳动 飞书 小程序面板
算法题 判断字符串是否可以由字典中的字符串组成 动态规划 https://blog.csdn.net/summer2day/article/details/97430955
    
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
