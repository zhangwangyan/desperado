

### 6、@Autowired @PostConstruct@PreDestroy注解.



### 6、@Autowired @PostConstruct@PreDestroy注解.

1. @Autowreid和@Resource的依赖注入
2. init-method和@PostConstruct@PreDestroy
3. 各种Aware接口的调用
4. 循环依赖详解

![image-20221212083803171](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212083803171.png)

![image-20221212084806897](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212084806897.png)

当满足条件。才会依赖注入。   依赖注入出问题了，找依赖注入相关代码。



引用数据类型的依赖注入会触发getBean操作。

![image-20221212093137904](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212093137904.png)

![image-20221212094106957](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212094106957.png)

![image-20221212094433855](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212094433855.png)

![image-20221212095923400](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212095923400.png)

![image-20221212095930573](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212095930573.png)

拿到引用类的所有注解。

------

![image-20221212101008024](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212101008024.png)

![image-20221212101501599](6、@Autowired @PostConstruct@PreDestroy注解.assets/image-20221212101501599.png)





核心流程埋点  beanpOST

