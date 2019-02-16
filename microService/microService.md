# 微服务概述
## 什么是微服务
引用Martin Fowler在他[博客](https://martinfowler.com/articles/microservices.html)上的表述，微服务是一种将单一应用开发为一组小型服务的架构风格，每个服务运行在单独的进程中，服务间使用轻量级协议进行通信。各个微服务专注于自己的业务逻辑，可以使用自动化部署机制进行独立部署。此外，应该有一个独立的集群来集中管理所有的服务。
## 为什么使用微服务
区别于单一应用将所有功能打包进一个包进行部署，个人理解微服务最大的特点是各个服务进行独立部署。这可以带来如下好处:

* 增加系统的稳定性：单个服务的bug如OOM不至于拖垮整个系统
* 灵活扩展：可以根据各个服务的不同水位进行灵活的扩展
* 技术栈的灵活选型：可以根据各个服务的特点选择最适合的技术栈
* 硬件资源的灵活选择：不同服务可以根据各自的特点选择最适合的硬件资源，例如CPU密集型服务和IO密集型服务
* 增加开发效率: 不同的服务可以由不同的团队进行维护，开发人员可以真正专注在一块功能上。
## 常用组件
以Spring Cloud为参考，可以一窥微服务架构中的常用组件,以下内容参考[Spring Cloud第二代](http://springcloud.cn/view/415)

|  | SpringCloud一代 | SpringCloud二代 |
| ------ | ------ | ------ |
| 网关 | Spring Cloud Zuul	 | Spring Cloud Gateway|
| 注册中心 | eureka(不再更新)，Consul,ZK	 | 阿里Nacos，拍拍贷radar等可选|
| 配置中心 | spring cloud config		 | 阿里Nacos，携程Apollo，随行付Config Keeper|
| 客户端软负载均衡	 | Ribbon		 | spring-cloud-loadbalancer|
| 容错处理	 | Hystrix(不再更新)	 | spring-cloud-r4j(Resilience4J)，阿里Sentinel|
| 服务监控	 | spring-cloud-sleuth	 |  |

## 相关开源项目链接
+ [Sentinel](https://github.com/alibaba/Sentinel)

+ [spring-cloud-circuitbreaker](https://github.com/spring-cloud-incubator/spring-cloud-circuitbreaker)

+ [resilience4j](https://github.com/resilience4j/resilience4j)

+ [nacos](https://github.com/alibaba/nacos)

+ [config-keeper](https://github.com/sxfad/config-keeper)

+ [spring-cloud-loadbalancer](https://github.com/spring-cloud-incubator/spring-cloud-loadbalancer)

+ [apollo](https://github.com/ctripcorp/apollo)

+ [spring-cloud-gateway](https://github.com/spring-cloud/spring-cloud-gateway)

+ [spring-cloud-sleuth](https://github.com/spring-cloud/spring-cloud-sleuth)
