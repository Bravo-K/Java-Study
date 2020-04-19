# Spring Boot
## 简介
* 随着注解的功能增强,尤其是`Servlet 3.0`规范的提出,Web容器可以脱离`web.xml`的部署,使得Web容器完全可以基于注解开发,对于`Spring 3.x`和`Spring 4.x`的版本注解功能越来越强大,对于`XML`的依赖越来越少,到了4.x的版本后甚至可以完全脱离XML,因此在Spring中使用注解开发占据了主流的地位. 于此同时,Pivotal团队在原有Spring基础上主要通过注解的方式继续简化了Spring框架的开发,他们基于Spring框架开发了`Spring Boot`,所以Spring Boot并非是代替Spring框架,而是让Spring框架更加容易使用哟 ~*
## Spring Boot的优点
- *创建独立的Spring应用程序*
- *嵌入的Tomcat,Jetty或Undertow,无须部署WAR文件*
- *允许通过Maven来根据需要获取`starter`*
- *尽可能地自动配置Spring*
- *提供生产就绪型功能,如指标,健康检查和外部配置*
- *绝对没有代码生成,对XML没有要求配置*
- *减少开发、测试的时间和工作量，避免大量 maven 导入和各种版本冲突*
## Spring Boot 的核心注解
启动类上面的注解@SpringBootApplication是 Spring Boot 的核心注解，主要组合包含了以下 3 个注解：
- @SpringBootConfiguration：组合了 @Configuration 注解，实现配置文件的功能。
- @EnableAutoConfiguration：打开自动配置的功能，也可以关闭某个自动配置的选项，如关闭数据源自动配置功能： @SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })。
- @ComponentScan：Spring组件扫描。
