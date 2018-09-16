# 作者简介: 
Adam Lu(刘亚壮)，高级软件架构师，Java编程专家，Spring、MySQL内核专家，熟悉Android内核，开源分布式消息引擎Mysum发起者、首席架构师及开发者，Android开源消息组件Android-MQ独立作者，国内知名开源分布式数据库中间件Mycat核心架构师、开发者，精通Java, C, C++, Python, Hadoop大数据生态体系，熟悉MySQL、Redis内核，Android底层架构。多年来致力于分布式系统架构、微服务、分布式数据库、大数据技术的研究，曾主导过众多分布式系统、微服务及大数据项目的架构设计、研发和实施落地。在高并发、高可用、高可扩展性、高可维护性和大数据等领域拥有丰富的经验。对Hadoop、Spark、Storm等大数据框架源码进行过深度分析并具有丰富的实战经验。

# 作者联系方式
QQ：2711098650

# 项目简述
本项目旨在可以为Apk打上系统签名  
  
本项目中的SignApk类是从Android的源码中复制出来的系统签名程序，在Android源码中的目录为：
```
build -> tools -> signapk：SignApk.java
```
完成签名还需要另外两个文件，分别叫platform.pk8和platform.x509.pem，在源码的以下路径可以找到：
```
build -> target -> product -> security
```

# 使用说明
提供对Android Apk的签名操作，具体使用方式为：  
  
1)将项目打包成Jar  
  
2)将项目打成的Jar包、platform.pk8、platform.x509.pem和需要签名的apk放到同一目录  
  
3)执行如下命令，对需要打包的Apk进行打包  
  
java -jar mykit-android-signapk.jar platform.x509.pem platform.pk8 需要签名的apk文件 签名后生成的apk文件
