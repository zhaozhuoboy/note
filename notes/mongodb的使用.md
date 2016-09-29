# mongoDB

---

### 1. 什么是mongodb？

  - MongoDB是一个基于分布式文件存储的开源数据库系统

  - MongoDB 将数据存储为一个文档，数据结构由键值(key=>value)对组成。MongoDB 文档类似于 JSON 对象。字段值可以包含其他文档，数组及文档数组。

### 2.mongodb启动与连接

#### 2.1启动

  ```
  mongod --dbpath=./data

  ```

- 如果出现`waiting for connections on port 27017` 表示启动成功。
- 可以在命令后面加上参数 `--port 27017` 来指定端口

> 注意： 这个命令窗口不能关闭，否则就停止了mongodb的服务进程

#### 2.2 客户端连接服务器

新开一个命令窗口


`mongo --host=127.0.0.1` 或者 `mongo` 按回车键

> 备注：--host后的值表示服务器的ip地址

### 数据库的操作

未完。。。
