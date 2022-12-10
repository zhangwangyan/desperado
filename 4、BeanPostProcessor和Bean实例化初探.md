###  **BeanPostProcessor 实例化、事件源码和Bean实例化初探**

1. BeanPostProcessor实例化
2. 事件源码
3. Bean实例化初探



把之前用JFInal框架的工程，改变成一个spring框架的工程，意味着每一个需要实例化的类都要加上一个

@Service注解



![image-20221210160149931](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210160149931.png)

------

![image-20221210161139775](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210161139775.png)

```
把实现了BeanPostProcessor接口的类实例化，并且加入到BeanFactory中
```

![image-20221210161554946](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210161554946.png)

------

![image-20221210162111272](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210162111272.png)

![image-20221210162428534](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210162428534.png)

![image-20221210162620987](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210162620987.png)

![image-20221210163308806](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210163308806.png)

作为观察者来说。

![image-20221210165750175](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210165750175.png)

![image-20221210171307391](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210171307391.png)



有些代码阻塞容器启动。

![image-20221210171537168](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210171537168.png)



容器启动后，触发事件

![image-20221210172329677](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210172329677.png)

------

![image-20221210180030670](4、BeanPostProcessor和Bean实例化初探.assets/image-20221210180030670.png)



实例化----dependon  底层的支持。