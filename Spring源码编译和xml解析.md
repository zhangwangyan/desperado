### 12-07 Spring源码编译和xml解析

#### 1、spring为什么学  

1. 其他框架用到了，比如：如果使用netty,会使用到spring
2. 代码更加优雅，体现程序员功力，不喜欢屎山
3. 面试需要

#### 2、编译-代码

​     spring源码工程中也用到了 命令 bat

​       <spring.version>5.2.8.RELEASE</spring.version> ------源码版本

#### 3、代码分析

http://117.33.237.52:20070/desperado-image/xml%E8%A7%A3%E6%9E%90%E5%92%8CBeanDefinition%E5%B0%81%E8%A3%85%E6%A0%B8%E5%BF%83%E6%96%B9%E6%B3%95%20refreshBeanFactory().jpg

![image-20221207180841940](Spring源码编译和xml解析.assets/image-20221207180841940.png)

![image-20221207181411718](Spring源码编译和xml解析.assets/image-20221207181411718.png)

```
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>${spring.version}</version>
</dependency>
```

=========================

模板设计模式

​       钩子方法。com.enjoy.jack.designPattern.template

![image-20221207185745347](Spring源码编译和xml解析.assets/image-20221207185745347.png)

![image-20221207185849066](Spring源码编译和xml解析.assets/image-20221207185849066.png)

委托设计模式 

​          com/enjoy/jack/designPattern/entrust

![image-20221207190915224](Spring源码编译和xml解析.assets/image-20221207190915224.png)

![image-20221207191056603](Spring源码编译和xml解析.assets/image-20221207191056603.png)

上下文接口实现资源加载接口

![image-20221207191649598](Spring源码编译和xml解析.assets/image-20221207191649598.png)

![image-20221207191745264](Spring源码编译和xml解析.assets/image-20221207191745264.png)

![image-20221207191909742](Spring源码编译和xml解析.assets/image-20221207191909742.png)

![image-20221207192016930](Spring源码编译和xml解析.assets/image-20221207192016930.png)

![image-20221207193232175](Spring源码编译和xml解析.assets/image-20221207193232175.png)

http://117.33.237.52:20070/desperado-image/GenericBeanDefinition.jpg