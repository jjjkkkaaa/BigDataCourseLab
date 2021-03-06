## MongoDB实验

#### 一、实验目的

1. 学会使用mongo shell对文档数据库MongoDB进行增删改查（CRUD）


#### 二、实验要求

1. Centos 7.5

2. JDK 1.8


#### 三、预备知识

MongoDB 是由 C++ 语言编写的一个面向文档存储的数据库，操作起来比较简单和容易。MongoDB旨在为 WEB 应用提供可扩展的高性能数据存储解决方案。  

#### 四、实验内容

1.  利用MongoDB官网上的安装指南完成最新版本MongoDB的安装部署。
    
    *root用户的密码为zkpk
    
    参考链接 https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/
    
2.  开启mongodb服务

3.  使用数据导入组件mongoimport，读入mongo_test.txt文件，到名为student的数据库中名为score的collection中。
    *mongo_test.txt文件内容如下，需自行创建

    ```
    {"name":"zhangsan","age":18,"sex":"man","transcript":{"yuwen":50,"shuxue":100,"yingyu":90}}
    
    {"name":"lisi","age":21,"sex":"woman","transcript":{"yuwen":10,"shuxue":100,"yingyu":90}}
    
    {"name":"wangwu","age":31,"sex":"man","transcript":{"yuwen":12,"shuxue":4356,"yingyu":45}}
    
    {"name":"zhaoliu","age":12,"sex":"woman","transcript":{"yuwen":50,"shuxue":56,"yingyu":12}}
    
    {"name":"yanqi","age":56,"sex":"man","transcript":{"yuwen":78,"shuxue":100,"yingyu":90}}
    
    {"name":"shenba","age":67,"sex":"woman","transcript":{"yuwen":78,"shuxue":34,"yingyu":1}}
    ```

    参考链接 https://docs.mongodb.com/manual/reference/program/mongoimport/

4.  在mongo shell中实现以下需求。
    参考链接 https://docs.mongodb.com/manual/tutorial/getting-started/
    https://docs.mongodb.com/manual/crud/

    1.  进入mongo shell后切换到student数据库
    2.  利用db.collection.insert( )命令在集合中插入一条样例 `{"name":"shenba","age":67,"sex":"woman","transcript":	      {"yuwen":78,"shuxue":34,"yingyu":1}}`
    3.  利用db.collection.find( )命令查询集合中性别男的样例
    4.  利用db.collection.find( )命令查询集合中年龄大于20的样例
    5.  利用db.collection.find( )命令查询集合中语文和数学都达到60分及格线的样例
    6.  利用db.collection.deleteMany()命令删除上一条需求中查询到的样例