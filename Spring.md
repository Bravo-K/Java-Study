# Spring
## IOC控制反转
**Spring 核心容器**
<kbd>BeanFatory</kbd>和<kbd>ApplicatoinContext</kbd>

<kbd>BeanFatory</kbd>为基础类型的Ioc容器,简单的说就是一个管理Bean的工厂,它主要负责初始化各种Bean,并调用它们的生命周期方法.

<kbd>ApplicationContext</kbd>是BeanFactory的子接口,也称为应用上下文,不仅包含了BeanFactory的所有功能,还添加了对国际化,资源访问,事件传播等方面的支持.有两种创建ApplicatoinContext接口实例的方法：
<kbd>ClassPathXmlApplicationContext</kbd>
<kbd>FileSystemXmlApplicatoinContext</kbd>
