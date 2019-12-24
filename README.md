XML形式初始化IOC
IOC首先是加载配置文件，然后解析XML，在把XML解析成Document对象，然后根据Document对象解析元素，然后载入元		素，再把Document对象解析封装成BeanDefinition的BeanDefinitionHold对象，最后使用BeanDefintionHold对象进行注册Bean	

注解形式初始化IOC
1）根据指定的注解Bean定义的类，创建Spring容器中对注解Bean的封装的数据结构
2）解析注解Bean的作用域
3）为注解Bean定义作用域
4）生成BeanName
5）处理注解Bean中的通用注解
6）解析Primary和Lazy注解并进行处理
7）创建BeanDefinitionHolder对象 封装注解Bean定义类的数据
8）根据@Bean定义类中的作用域创建代理
9）向IOC容器注册Bean
10）刷新容器 refresh()

扫描形式初始化IOC
1）获取容器中已经注册Bean的个数
2）启动扫描器，扫描类
3）创建了一个Set存放扫描到Bean的定义类
4）遍历包以及包下的子类
5）遍历中等同于注解形式初始化IOC的步骤
6）处理完成后注册IOC
7）刷新容器
