### 自定义scope和factoryBean

1. factoryBean接口
1. 自定义scope
1. @PropertySource
1. @CompoentScan





![image-20221216071039130](9、自定义scope和factoryBean.assets/image-20221216071039130.png)

![image-20221216072254970](9、自定义scope和factoryBean.assets/image-20221216072254970.png)

![image-20221216072304822](9、自定义scope和factoryBean.assets/image-20221216072304822.png)

![image-20221216072412602](9、自定义scope和factoryBean.assets/image-20221216072412602.png)

![image-20221216073018637](9、自定义scope和factoryBean.assets/image-20221216073018637.png)

![image-20221216073325142](9、自定义scope和factoryBean.assets/image-20221216073325142.png)

![image-20221216073636454](9、自定义scope和factoryBean.assets/image-20221216073636454.png)

![image-20221216073908873](9、自定义scope和factoryBean.assets/image-20221216073908873.png)

![](9、自定义scope和factoryBean.assets/image-20221216073958888.png

![image-20221216074031193](9、自定义scope和factoryBean.assets/image-20221216074031193.png)

和第三章产生关系。

------

每一次调用都是新的实例。



protyoe



不管是相同线程多次调用getBean，还是多线程多次调用getBean,每次getBean拿到的实例都不一样。

------

![image-20221216080742263](9、自定义scope和factoryBean.assets/image-20221216080742263.png)

![image-20221216080856951](9、自定义scope和factoryBean.assets/image-20221216080856951.png)

```
public class CustomScope implements Scope {

    private ThreadLocal local = new ThreadLocal();

    @Override
    public Object get(String name, ObjectFactory<?> objectFactory) {
        if(local.get() != null) {
            return local.get();
        } else {
            //创建实例
            Object object = objectFactory.getObject();
            local.set(object);
            return object;
        }
    }

    @Override
    public Object remove(String name) {
        Object o = local.get();
        local.remove();
        return o;
    }

    @Override
    public void registerDestructionCallback(String name, Runnable callback) {

    }

    @Override
    public Object resolveContextualObject(String key) {
        return null;
    }

    @Override
    public String getConversationId() {
        return null;
    }
}

```

![image-20221216081527291](9、自定义scope和factoryBean.assets/image-20221216081527291.png)

![image-20221216081948890](9、自定义scope和factoryBean.assets/image-20221216081948890.png)

![image-20221216082242748](9、自定义scope和factoryBean.assets/image-20221216082242748.png)

![image-20221216082434778](9、自定义scope和factoryBean.assets/image-20221216082434778.png)

![image-20221216082606183](9、自定义scope和factoryBean.assets/image-20221216082606183.png)

什么时候注册进去的、

![image-20221216082750568](9、自定义scope和factoryBean.assets/image-20221216082750568.png)

![image-20221216083128266](9、自定义scope和factoryBean.assets/image-20221216083128266.png)

![image-20221216084350003](9、自定义scope和factoryBean.assets/image-20221216084350003.png)
