# Spring
## IOC控制反转
**Spring 核心容器**： ==BeanFatory==和ApplicatoinContext ==标记文本==

- <kbd>BeanFatory</kbd>为基础类型的Ioc容器,简单的说就是一个管理Bean的工厂,它主要负责初始化各种Bean,并调用它们的生命周期方法.

- <kbd>ApplicationContext</kbd>是BeanFactory的子接口,也称为应用上下文,不仅包含了BeanFactory的所有功能,还添加了对国际化,资源访问,事件传播等方面的支持.有两种创建ApplicatoinContext接口实例的方法：

<kbd>ClassPathXmlApplicationContext</kbd>：通过类路径classPath中寻找指定的XML配置文件,找到并装载完成ApplicationContext的实例化工作.

<kbd>FileSystemXmlApplicatoinContext</kbd>：通过指定的文件系统路径(绝对路径)中寻找指定的XML配置文件,找到并装载完成ApplicationContext的实例化工作.

```javascript
// An highlighted block
var foo = 'bar';
```
