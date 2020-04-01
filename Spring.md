# Spring
## IOC控制反转
### Spring 核心容器： *BeanFatory*和*ApplicatoinContext*

- `BeanFatory`为基础类型的Ioc容器,简单的说就是一个管理Bean的工厂,它主要负责初始化各种Bean,并调用它们的生命周期方法.

- <kbd>ApplicationContext</kbd>是BeanFactory的子接口,也称为应用上下文,不仅包含了BeanFactory的所有功能,还添加了对国际化,资源访问,事件传播等方面的支持.有两种创建ApplicatoinContext接口实例的方法：

     <kbd>ClassPathXmlApplicationContext</kbd>：通过类路径classPath中寻找指定的XML配置文件,找到并装载完成ApplicationContext的实例化工作.

     <kbd>FileSystemXmlApplicatoinContext</kbd>：通过指定的文件系统路径(绝对路径)中寻找指定的XML配置文件,找到并装载完成ApplicationContext的实例化工作.


### 依赖注入
依赖注入的作用就是在使用Spring框架创建对象时,动态地将其所依赖的对象注入Bean组件中,其实现方式通常有两种,一种是属性*setter方法*注入,另一种是*构造方法*注入.


### 程序示例

配置文件
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">
	
	<!--
	id: IOC容器中Bean的唯一标识
	class: 通过反射机制在IOC容器中创建Bean(所以要求Bean中必须有无参的构造器).
	-->
	<bean id="SpringTestID" class="pers.huangyuhui.spring.bean.HiSpring5">
		<!-- 初始化HiSpring类中的属性名为name的值 -->
		<property name="name" value="Spring"></property>
	</bean>

</beans>
```
测试类
```
public void test() {
		
        // 创建Spring的IOC对象
	ApplicationContext applicationContext = new ClassPathXmlApplicationContext("applicationContext.xml");

	// 从IOC容器中获取Bean实例
	HiSpring5 hiSpring5 = (HiSpring5) applicationContext.getBean("SpringTestID");
        
	hiSpring5.ouputName();

}

public void test2() {
		
        ApplicationContext context = new ClassPathXmlApplicationContext(
            new String[]{"applicationContext1.xml","applicationContext2.xml"})

       //可以通过调用`ApplicationContext`的`getBean`方法获得对象
       //getBean方法会查询`id`为`product`且类型为`Product`的`bean`对象.
       Product product = context.getBean("product",Product.class);

}

```	
