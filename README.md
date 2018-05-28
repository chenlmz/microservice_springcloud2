## 第二个基于Spring Cloud搭建的微服务案例

### 环境准备

IDEA（2018）

java 8

maven 3.5

Spring Cloud：Finchley.BUILD-SNAPSHOT

Spring Boot：2.0.2.RELEASE

Git/GitHub

### 案例目的

通过第一个SP 搭建的整体案例，大家应该对SP有了一个比较整体的认识，至少是比较了解了SP 最核心的五个组件（Eureka，Feign，Ribbon，Zuul，Config），第二个案例继续在第一个案例的基础上，再一次通过从零搭建（就跟搭积木一样），回顾一个基础的微服务架构到底需要哪些组件，SP是如何一步一步实现HA，继续加深SP中核心组件的上手度

### 案例特点

基于最新的IDEA和最新版本的Spring Boot，Spring Cloud 版本，相比于第一个案例使用Eclipse 的maven构建，个人更推荐使用IDEA 自带的spring initializr 插件快速完成模块的构建

相比于第一个案例，第二个案例更加“轻量化”（去掉了Docker+Mysql+Mybatis），专注于SP构架微服务的横向实现，有助于快速上手和理解，从实际开发环境中抽离出来，以快速上手练习为主要目的

### 个人建议

不管是第一个案例还是第二个案例，都需要你至少使用过Spring Boot，具有一定的java开发经验，如果有Docker+Zookeeper的使用经验，上手分分钟搞定，本案例在搭建过程中参考了第一个案例和一些优秀的博客，如果你明白了我的第一个实现案例，那么再看这个会觉得非常熟悉和轻松，除了开发工具的不同以及部分细节，两个案例都差不多

### 案例总结

和网上其他的SP案例搭建博客不同，我使用了空白Project作为顶级目录+公共模块+其他模块的构建思路，一方面是开发起来，模块之间结构更加清晰明了，独立；一方面是也尝试过按照他人博客方式搭建，但是总是无法读取多个模块之间的各自配置文件，暂未解决

再搭建Hystrix DashBoard 组件的过程中，因为是最新的版本，需要额外设置，有点坑，不过都记录在案例构建文档里了，注意即可

相比于第一个案例，Zuul模块实现了请求过滤的实现

如果SP还不是很懂，可以参考这位老哥的博客，每个模块的搭建都写了一篇博客，[点我](https://blog.csdn.net/forezp/article/details/69696915)
