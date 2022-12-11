###  bean的实例化和注解的收集



1. factoryMethod方式实例化
2. 有参和无惨构造函数实例化
3. @Autowired@Value@Resource 等注解的收集。



![image-20221211085231314](5、bean的实例化和注解的收集.assets/image-20221211085231314.png)

![image-20221211085312587](5、bean的实例化和注解的收集.assets/image-20221211085312587.png)

![image-20221211085419425](5、bean的实例化和注解的收集.assets/image-20221211085419425.png)

![image-20221211085532003](5、bean的实例化和注解的收集.assets/image-20221211085532003.png)



1、实例化factoryMethod方法对应的实例

​        @Bean注解

​        <bean>标签里面配置了factory-method属性

![image-20221211090257221](5、bean的实例化和注解的收集.assets/image-20221211090257221.png)

2、实例化带有@Autowired注解的构造函数

3、实例化没有@Autowired的有参构造函数

4、实例化无参构造函数

![image-20221211090728978](5、bean的实例化和注解的收集.assets/image-20221211090728978.png)

![image-20221211091134268](5、bean的实例化和注解的收集.assets/image-20221211091134268.png)

非静态

![image-20221211091740714](5、bean的实例化和注解的收集.assets/image-20221211091740714.png)

![image-20221211091958767](5、bean的实例化和注解的收集.assets/image-20221211091958767.png)

![image-20221211092235173](5、bean的实例化和注解的收集.assets/image-20221211092235173.png)

![image-20221211092413359](5、bean的实例化和注解的收集.assets/image-20221211092413359.png)

![image-20221211092626230](5、bean的实例化和注解的收集.assets/image-20221211092626230.png)

------



Autowired注解的方法或者属性都会触发getBean操作。

![image-20221211140009994](5、bean的实例化和注解的收集.assets/image-20221211140009994.png)

![image-20221211140311485](5、bean的实例化和注解的收集.assets/image-20221211140311485.png)

![image-20221211141142014](5、bean的实例化和注解的收集.assets/image-20221211141142014.png)

![image-20221211141433406](5、bean的实例化和注解的收集.assets/image-20221211141433406.png)

------

![image-20221211143142975](5、bean的实例化和注解的收集.assets/image-20221211143142975.png)
