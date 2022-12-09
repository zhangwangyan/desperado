###  component-scan 标签解析和bean实例化初探



1、compoent-scan标签解析

2、自定义标签实战

3、bean实例化流程

![image-20221209095931949](3、component-scan 标签解析和bean实例化初探.assets/image-20221209095931949.png)

@Component

@Service

@Controller

@Repository

@Configuration



doscan:

1. 去扫描基本包的路径， 找.class文件

2. 递归找.class文件

3. 判断.class文件里面是否有注解，includeFilter里面的注解

4. 变成BeanDefinition对象

   

![image-20221209101415581](3、component-scan 标签解析和bean实例化初探.assets/image-20221209101415581.png)

------

![image-20221209102024360](3、component-scan 标签解析和bean实例化初探.assets/image-20221209102024360.png)

![image-20221209102055371](3、component-scan 标签解析和bean实例化初探.assets/image-20221209102055371.png)

------

![image-20221209103810097](3、component-scan 标签解析和bean实例化初探.assets/image-20221209103810097.png)

```
ScannedGenericBeanDefinition
```

![image-20221209104519279](3、component-scan 标签解析和bean实例化初探.assets/image-20221209104519279.png)

![image-20221209105458706](3、component-scan 标签解析和bean实例化初探.assets/image-20221209105458706.png)

![image-20221209110014224](3、component-scan 标签解析和bean实例化初探.assets/image-20221209110014224.png)

![image-20221209110059727](3、component-scan 标签解析和bean实例化初探.assets/image-20221209110059727.png)

------

![image-20221209110413168](3、component-scan 标签解析和bean实例化初探.assets/image-20221209110413168.png)

```
ConfigurationClassPostProcessor
```

```
AutowiredAnnotationBeanPostProcessor
```

```
CommonAnnotationBeanPostProcessor
```

![image-20221209112001399](3、component-scan 标签解析和bean实例化初探.assets/image-20221209112001399.png)

![image-20221209112711935](3、component-scan 标签解析和bean实例化初探.assets/image-20221209112711935.png)

![image-20221209113541328](3、component-scan 标签解析和bean实例化初探.assets/image-20221209113541328.png)

![image-20221209113604132](3、component-scan 标签解析和bean实例化初探.assets/image-20221209113604132.png)

scan-bean



可以自定义注解，也可以借助spring方法、



registtry  beanfactory

https://blog.csdn.net/luoyang_java/article/details/105835112
