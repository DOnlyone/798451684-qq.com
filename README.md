# Kafka: The Definitive Guide </br> 

***
## chapter1：kafka的安装：

```
由于Kafka是用Scala语言开发的，运行在JVM上，因此在安装Kafka之前需要先安装JDK
# yum install java-1.8.0-openjdk* -y
kafka依赖zookeeper，所以需要先安装zookeeper (非必须，kafka中包含有zookeeper）
# wget http://mirror.bit.edu.cn/apache/zookeeper/stable/zookeeper-3.4.12.tar.gz
# tar -zxvf zookeeper-3.4.12.tar.gz
# cd zookeeper-3.4.12
# cp conf/zoo_sample.cfg conf/zoo.cfg
启动zookeeper
# bin/zkServer.sh start
# bin/zkCli.sh
kafka下载
# wget https://archive.apache.org/dist/kafka/1.1.0/kafka_2.11-1.1.0.tgz
# tar -xzf kafka_2.11-1.1.0.tgz
# cd kafka_2.11-1.1.0
启动
# kafka-server-start.sh [-daemon] server.properties
创建并验证主题
# bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
含义为：创建一个名字为 test 的Topic，这个topic只有一个partition，并且备份因子也设置为1
订阅topic
# /usr/local/kafka/bin/kafka-topics.sh --zookeeper localhost:2181 --describe --topic test
测试往主题发送消息  注 --broker后不能有空格
# /usr/local/kafka/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
消费消息
# /usr/local/kafka/bin/kafka-console-consumer.sh --zookeeper localhost:2181 --topic test --from-beginning

```

----
    helloworld
please `press` http://baidu.com
[我的博客](http://blog.csdn.net/guodongxiaren)</br>
* aaa
  * aab
    * abc
* bbb
* cc
>aaa
>>aab</br>

![baidu1](http://www.baidu.com/img/bdlogo.gif "百度logo") 

